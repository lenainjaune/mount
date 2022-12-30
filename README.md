RO en attente de la fin de migration















































# mount
All relative to mount

# sshfs
Nécessite [SSH sans mot de passe](https://github.com/lenainjaune/tips/blob/master/%23_ssh_%23) et avoir activé allow_other dans /etc/fuse.conf (https://carmagnole.ovh/fr/posts/fstab-sshfs/)

Nota : **\_netdev** sert à monter le partage [dès que le réseau est disponible](http://codingberg.com/linux/systemd_when_to_use_netdev_mount_option)
```sh
user1@host1:~$ cat /etc/fstab | grep ^sshfs
sshfs#user2@host2:path/to/share/from/host2 /path/to/mount/from/host1 fuse defaults,allow_other,_netdev 0 0
```
