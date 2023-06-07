This note writes how to change https to ssh.
```sh
# check user setting
git config --global user.name
git config --global user.name
# check now connection method
git remote -v
# how to change
git remote set-url origin git@github.com:taogya/YourRepository.git
echo -n 'Host github.com
  HostName github.com
  User git
  Port 22
  IdentityFile ~/.ssh/id_rsa
  PreferredAuthentications publickey
  TCPKeepAlive yes 
  IdentitiesOnly yes' >> ~/.ssh/config
```
