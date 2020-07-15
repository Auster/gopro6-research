```
# /opt/gp/gpNet 2> /dev/null
gpNet:
Starting gpNet daemon
gpNet: version 6.0.0.0  built on Oct 24 2017 16:58:55 by jenkins at 0d7a4b6


gpNet: Test for debug cable shorted to RTOS console input:
gpNet: t api system beep_blink beep_blink_error

gpNet: t api system beep_blink beep_blink_error

gpNet: reboot yes

gpNet: ERROR - Invalid "/tmp/fuse_b/wifi_mac.bin" file

gpNet: ERROR - Invalid "/tmp/fuse_b/mfg.json" file

gpNet: READING "/tmp/fuse_b/conf.json" file

gpNet: ERROR - Invalid "/tmp/fuse_b/conf.json" file (reading backup)

gpNet: ERROR - Invalid "/tmp/fuse_b/conf.json.bak" file (reading safety)

gpNet: ERROR - Invalid "/tmp/fuse_a/conf.json.bak" file

gpNet: [   gpMbox_txopen:  91] target Mbox="/to_pla" errno="No such file or directory"

gpNet: ASSERT:/home/jenkins/workspace/chopes-banzai-link/BANZAILINK_EP/smarty-camera-support/libgpCommon/src/gpMsg.c/gpmsg_send:48:gpMbox_txopen(via, &txq) == 0
```
