* dry run

```bash
*DRYRUN* [For Hellow World/Hello] 🚀  Start image=catthehacker/ubuntu:act-latest
*DRYRUN* [For Hellow World/Hello]   🐳  docker pull image=catthehacker/ubuntu:act-latest platform= username= forcePull=false
*DRYRUN* [For Hellow World/Hello]   🐳  docker create image=catthehacker/ubuntu:act-latest platform= entrypoint=["/usr/bin/tail" "-f" "/dev/null"] cmd=[]
*DRYRUN* [For Hellow World/Hello]   🐳  docker run image=catthehacker/ubuntu:act-latest platform= entrypoint=["/usr/bin/tail" "-f" "/dev/null"] cmd=[]
*DRYRUN* [For Hellow World/Hello] ⭐ Run Main Checkout
*DRYRUN* [For Hellow World/Hello]   ✅  Success - Main Checkout
*DRYRUN* [For Hellow World/Hello] ⭐ Run Main run hello action
*DRYRUN* [For Hellow World/Hello]   ✅  Success - Main run hello action
*DRYRUN* [For Hellow World/Hello] ⭐ Run Main echo eviroments KEY1
*DRYRUN* [For Hellow World/Hello]   ✅  Success - Main echo eviroments KEY1
*DRYRUN* [For Hellow World/Hello] ⭐ Run Main echo eviroments KEY2
*DRYRUN* [For Hellow World/Hello]   ✅  Success - Main echo eviroments KEY2
*DRYRUN* [For Hellow World/Hello] ⭐ Run Main echo event head commit message1
*DRYRUN* [For Hellow World/Hello]   ✅  Success - Main echo event head commit message1
*DRYRUN* [For Hellow World/Hello] ⭐ Run Main echo event head commit message2
*DRYRUN* [For Hellow World/Hello]   ✅  Success - Main echo event head commit message2
*DRYRUN* [For Hellow World/Hello] ⭐ Run Main echo github reference1
*DRYRUN* [For Hellow World/Hello]   ✅  Success - Main echo github reference1
*DRYRUN* [For Hellow World/Hello] ⭐ Run Main echo github reference2
*DRYRUN* [For Hellow World/Hello]   ✅  Success - Main echo github reference2
*DRYRUN* [For Hellow World/Hello] 🏁  Job succeeded
```

* run

```bash
$ act --secret-file=".secrets"

[For Hellow World/Hello] 🚀  Start image=catthehacker/ubuntu:act-latest
[For Hellow World/Hello]   🐳  docker pull image=catthehacker/ubuntu:act-latest platform= username= forcePull=false
[For Hellow World/Hello]   🐳  docker create image=catthehacker/ubuntu:act-latest platform= entrypoint=["/usr/bin/tail" "-f" "/dev/null"] cmd=[]
[For Hellow World/Hello]   🐳  docker run image=catthehacker/ubuntu:act-latest platform= entrypoint=["/usr/bin/tail" "-f" "/dev/null"] cmd=[]
[For Hellow World/Hello] ⭐ Run Main Checkout
[For Hellow World/Hello]   🐳  docker cp src=/Users/jeongtaepark/Desktop/act-practice/. dst=/Users/jeongtaepark/Desktop/act-practice
[For Hellow World/Hello]   ✅  Success - Main Checkout
[For Hellow World/Hello] ⭐ Run Main run hello action
[For Hellow World/Hello]   🐳  docker exec cmd=[bash --noprofile --norc -e -o pipefail /var/run/act/workflow/hello-action] user= workdir=
| 멍개는 잘 생겼다
| 멍개는 코딩을 못한다.
| 멍개는 그림을 못 그린다.
[For Hellow World/Hello]   ✅  Success - Main run hello action
[For Hellow World/Hello] ⭐ Run Main echo eviroments KEY1
[For Hellow World/Hello]   🐳  docker exec cmd=[bash --noprofile --norc -e -o pipefail /var/run/act/workflow/2] user= workdir=
| ***
[For Hellow World/Hello]   ✅  Success - Main echo eviroments KEY1
[For Hellow World/Hello] ⭐ Run Main echo eviroments KEY2
[For Hellow World/Hello]   🐳  docker exec cmd=[bash --noprofile --norc -e -o pipefail /var/run/act/workflow/3] user= workdir=
| ***
[For Hellow World/Hello]   ✅  Success - Main echo eviroments KEY2
[For Hellow World/Hello] ⭐ Run Main echo event head commit message1
[For Hellow World/Hello]   🐳  docker exec cmd=[bash --noprofile --norc -e -o pipefail /var/run/act/workflow/4] user= workdir=
| c1b87d90e87e77e38cebeaa08dd9e0f0f69302d3
[For Hellow World/Hello]   ✅  Success - Main echo event head commit message1
[For Hellow World/Hello] ⭐ Run Main echo event head commit message2
[For Hellow World/Hello]   🐳  docker exec cmd=[bash --noprofile --norc -e -o pipefail /var/run/act/workflow/5] user= workdir=
| c1b87d9
[For Hellow World/Hello]   ✅  Success - Main echo event head commit message2
[For Hellow World/Hello] ⭐ Run Main echo github reference1
[For Hellow World/Hello]   🐳  docker exec cmd=[bash --noprofile --norc -e -o pipefail /var/run/act/workflow/6] user= workdir=
| refs/heads/main
[For Hellow World/Hello]   ✅  Success - Main echo github reference1
[For Hellow World/Hello] ⭐ Run Main echo github reference2
[For Hellow World/Hello]   🐳  docker exec cmd=[bash --noprofile --norc -e -o pipefail /var/run/act/workflow/7] user= workdir=
| refs/heads/main
[For Hellow World/Hello]   ✅  Success - Main echo github reference2
[For Hellow World/Hello] 🏁  Job succeeded
```

**`--secret-file`**: [github] - [setting] - [secrets]에 등록된 환경변수 역할을 한다.

* workflow list

```bash
$ act -l

Stage  Job ID  Job name  Workflow name     Workflow file  Events
0      build   Hello     For Hellow World  test.yaml      push
```