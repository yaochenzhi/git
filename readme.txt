[auto deployment]

[root@demo hooks]# cat post-receive 
#!/usr/bin/env bash

GIT_WORK_TREE=/opt/test/deploy git checkout -f