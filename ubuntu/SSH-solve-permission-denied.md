# [SSH-solve-permission-denied](https://www.digitalocean.com/community/questions/ssh-copy-id-not-working-permission-denied-publickey?answer=34396)

> This describes cases when You have a chance to manage the server via web console (like DO droplet).

## Add Your PC's pub key

> using `ssh-copy-id` (better than editing the the `authorized_keys` using a text editor).

```shell
ssh_copy_id example.com
```

### If `ssh-copy-id` public key denied

In the server:

```shell
sudo nano /etc/ssh/sshd_config
```

Change this line:
`PasswordAuthentication no` to `PasswordAuthentication yes`

#### Restart daemon:

```shell
sudo systemctl restart sshd
```

Now try to connect again. A password should be asked.

> Remember to change back to ``PasswordAuthentication no`.

## If loggin-in as `root`

Make sure that in the `ssh_config` the `PermitRootLogin` is set to `yes`.
