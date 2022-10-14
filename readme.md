## Mac M1 running gitlab locally

### how to register runner inside mac shell

1. install runner on mac if not yet
2. start runner service
3. register runner with gitlab service

### how to register runner inside docker (not working so far)?

Inside runner container, execute the register command.

#### edit runner container /etc/hosts file

`docker exec -it gitlab-runner bash`

`echo 172.18.0.3 gitlab.local >> /etc/hosts`

echo '127.0.0.1 localhost
::1 localhost ip6-localhost ip6-loopback
fe00::0 ip6-localnet
ff00::0 ip6-mcastprefix
ff02::1 ip6-allnodes
ff02::2 ip6-allrouters
172.18.0.4 b164bd764811
172.18.0.3 gitlab.local' > /etc/hosts
