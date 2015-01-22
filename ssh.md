## Generate ssh key
ssh-keygen -b 2048 -f ${name_key} -t rsa -C "${email}"

## Config
Host ${name}
  HostName ${hostname}
  User ${user}
  IdentityFile ${file.key}
