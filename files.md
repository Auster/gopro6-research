# WiFi config
##ap.conf

```
$ cat ap.conf

ctrl_interface=/var/run/wpa_supplicant
ctrl_interface_group=0

ap_scan=2

network={
   ssid="Australia-AP"
   mode=2
   auth_alg=OPEN
   key_mgmt=NONE
   frequency=1
}
```


## /tmp/fuse_b/mfg.json
See [mfg.json](mfg.json)

```
poky-fido/meta-mlb01-rtos/recipes-sniusbtest/sniusbtest/sniusbtest-1.0/usb30dev_mtp_func.sh:#sSerialnumber=`grep "camerasn" /tmp/fuse_b/mfg.json | cut -d ":" -f 2 | cut -d "\"" -f 2`
```

---

## /tmp/fuse_b/conf.json
See [conf.json](conf.json)

```
grep "CSI_FIRMWARE_VERSION" /tmp/fuse_b/conf.json | cut -d ":" -f 2 | cut -d "\"" -f 2^@^@[%s] gpUsb : %s:%d Unable to open config file [%s]....retrying %d
```

---

## /tmp/fuse_b/wifi_bdata.bin - "Golden bin file"
```
echo "Copying golden bin file"
cp -f ${1} /tmp/fuse_b/wifi_bdata.bin
```
