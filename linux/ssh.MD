

### SSH Config for Azure

`~/.ssh/config`:
```
Host azuredevops.company.co.il
  IdentityFile ~/.ssh/id_rsa
  IdentitiesOnly yes
  HostKeyAlgorithms +ssh-rsa
  PubkeyAcceptedAlgorithms +ssh-rsa

Host github.com
  User git
  IdentityFile ~/.ssh/id_rsa_github
```

`IdentitiesOnly yes` - try only this identity file for authentication. And don't try others
`User git` - Should be used for github. Otherwise premission will be denied for a local user name

## SSH keys

C|A
-|-
ssh-keygen | Generate new RSA key
ssh-keygen  -C "comment" -f ~/.ssh/id_rsa_github | Generate new RSA key, give a comment and keyname
ssh-keygen -t ed25519 -C "comment" -f ~/.ssh/id_ed25519 | Generate new ED25519 key
ssh-keygen -t rsa -b 4096 -m PEM -f ~/.ssh/id_rsa_4096	| Generate strong RSA key. -m PEM ensures compativility (produces a key starting with ssh-rsa)
```


C|A
-|-
ssh -T git@github.com | ssh auth check
ssh -vT git@github.com | verbose ssh auth check
who -u | Show connected SSH users to this machine
sudo kill -9 \<PID\> | Kill user by PID
ssh user@ip "\<cmd\>" | Execute command on remote machine