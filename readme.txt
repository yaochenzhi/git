[auto deployment]

[root@demo hooks]# cat post-receive 
#!/usr/bin/env bash

GIT_WORK_TREE=/opt/test/deploy git checkout -f


[advanced practical auto deployment]
# repo host connectable
curl https://server/api/repo/update

# server host unonnectable
rsync -zcavhP --stats user@repo.host:/path/to/repo /path/to/repo/local
git clone /path/to/repo/local  /path/to/deployment
