## Generate ssh key
ssh-keygen -b 4096 -f ${name_key} -t rsa -C "${email}"

## add key to ssh-agent
eval "$(ssh-agent -s)"  
ssh-add ${path_key} 

## Config
Host ${name} 
  HostName ${hostname} 
  User ${user} 
  IdentityFile ${file.key} 

## copy key on remote serve
ssh-copy-id -i ${file} ${user}@${host} 

## create ssl certificate
openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/nginx/ssl/nginx.key -out /etc/nginx/ssl/nginx.crt 
