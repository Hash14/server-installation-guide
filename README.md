# Use this guide to setup a new server with Ruby on Rails and Node

For new user
```
adduser user_name 
```

add sudo permission to the user
```
adduser user_name sudo
```

For generate key(local)
```
ssh-keygen -b 4096
```

copy key to server (ubuntu)
```
ssh-copy-id example_user@203.0.113.10
```

(MAC)
```
mkdir -p ~/.ssh && sudo chmod -R 700 ~/.ssh/ (server)
scp ~/.ssh/id_rsa.pub example_user@203.0.113.10:~/.ssh/authorized_keys (local)
```

Install RVM with RUBY AND RAILS
```
gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3
\curl -sSL https://get.rvm.io | bash -s stable --rails
source ~/.rvm/scripts/rvm
```

Install NPM
```
sudo apt-get update
sudo apt-get install nodejs
sudo apt-get install npm
```

Disable root login
```
sudo vim /etc/ssh/sshd_config
```

set PermitRootLogin no
```
set PasswordAuthentication no
```

```
sudo systemctl restart sshd
```

or
```
sudo service ssh restart
```
