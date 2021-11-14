# ssh-tips-tricks
SSH Tips and Tricks

![STOOIBOXY](https://user-images.githubusercontent.com/58792/141698988-76cb5889-a766-4a03-bc25-0fd02a097e23.png)

## Create SSH Keys

* Step 1: 

```
ssh-keygen -t rsa
```


* Step 2:

`cat /home/ec2-user/.ssh/id_rsa.pub`

* Step 3:

Copy to Github

* Step 4:

Clone repo

## SSH into Cloud9

1.  Open port 22 to 0.0.0.0
2.  Paste local `id_rsa.pub`
3.  `ssh -v ec2-user@<ipaddress>`

### Port forwarding remote server

1.  Create connection
```
ssh -N -L 8080:127.0.0.1:8080 ec2-user@<ipaddress>
```
2.  Launch the remote server:  `python app.py`
3.  open web browser on OS X laptop

## References

* [Setup SSH Keys Github Docs](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)
