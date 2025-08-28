

`~/.ssh/config` for Azure

```
Host azuredevops.company.co.il
  HostName azuredevops.company.co.il
  User git
  IdentityFile ~/.ssh/id_rsa
  HostKeyAlgorithms +ssh-rsa
  PubkeyAcceptedAlgorithms +ssh-rsa
```
