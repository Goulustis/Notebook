### SSH best practices
Create a public-private keypair instead of typing your password each time:  
On your local machine (linux/cygwin...):  

```bash
> ssh-keygen -t rsa
I stick with the defaults there. Then copy the public key with
> ssh-copy-id -i ~/.ssh/id_rsa.pub user@server
```
