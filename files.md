##1.60 firmware
#Unpacked
```
$ for i in `ls 1.6.unpacked/`; do file 1.6.unpacked/$i; done
1.6.unpacked/sector00.bin: data
1.6.unpacked/sector02.bin: data
1.6.unpacked/sector04.bin: big endian ispell hash file (?), and 20736 string characters
1.6.unpacked/sector07.bin: data
1.6.unpacked/sector08.bin: Linux rev 1.0 ext4 filesystem data, UUID=8998c9d3-8d3b-410f-b3ae-36317b0ac893 (extents) (large files) (huge files)
1.6.unpacked/sector09.bin: DIY-Thermocam raw data (Lepton 3.x), scale 19648-38373, spot sensor temperature -88471305153451388829696.000000, unit celsius, color scheme 4, calibration: offset 0.000000, slope 118128640.000000
1.6.unpacked/sector11.bin: data
1.6.unpacked/sector12.bin: data
1.6.unpacked/sector13.bin: data
1.6.unpacked/sector14.bin: data
```

## WiFi config
#ap.conf

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


# /tmp/fuse_b/mfg.json

```
poky-fido/meta-mlb01-rtos/recipes-sniusbtest/sniusbtest/sniusbtest-1.0/usb30dev_mtp_func.sh:#sSerialnumber=`grep "camerasn" /tmp/fuse_b/mfg.json | cut -d ":" -f 2 | cut -d "\"" -f 2`
```

---

# /tmp/fuse_b/conf.json
See conf.json

```
grep "CSI_FIRMWARE_VERSION" /tmp/fuse_b/conf.json | cut -d ":" -f 2 | cut -d "\"" -f 2^@^@[%s] gpUsb : %s:%d Unable to open config file [%s]....retrying %d
```

---

# /tmp/fuse_b/wifi_bdata.bin - "Golden bin file"
```
echo "Copying golden bin file"
cp -f ${1} /tmp/fuse_b/wifi_bdata.bin
```
