# Device descriptor Setting
```
bcd_usb=0x0310
id_vendor=0x2672
id_product=0x0037
bcd_device=0x0001
language_id=0x0409
sManufacture="GoPro"
sProduct="HERO 6 BLACK"
sSerialnumber=$1
```

# Device descriptor Setting
```
bcd_usb=0x0200
id_vendor=0x2672
id_product=0x0038
bcd_device=0x0001
language_id=0x0409
sManufacture="GoPro"
sProduct="HERO 6 BLACK"
sSerialnumber=$1
#sSerialnumber=`grep "camerasn" /tmp/fuse_b/mfg.json | cut -d ":" -f 2 | cut -d "\"" -f 2`
sConfiguration="Config ACM"
```

# Device descriptor Setting
```
bcd_usb=0x0200
id_vendor=0x2B88
id_product=0x0003
bcd_device=0x0001
language_id=0x0409
sManufacture="Socionext Inc"
sProduct="SN-MTP+ACM"
sSerialnumber="01234567890123"
sConfiguration="Config MTP+ACM"
```

# Device descriptor Setting
```
bcd_usb=0x0200
id_vendor=0x2B88
id_product=0x0002
bcd_device=0x0001
language_id=0x0409
sManufacture="Socionext Inc"
sProduct="SN-ACM"
sSerialnumber="01234567890123"
sConfiguration="Config ACM"
```

# Device descriptor Setting
```
bcd_usb=0x0200
id_vendor=0x2B88
id_product=0x0001
bcd_device=0x0001
language_id=0x0409
sManufacture="Socionext Inc"
sProduct="SN-MTP"
sSerialnumber="01234567890123"
sConfiguration="Config MTP"
```

# Device descriptor Setting
```
bcd_usb=0x0200
id_vendor=0x2B88
id_product=0x0004
bcd_device=0x0001
language_id=0x0409
sManufacture="Socionext Inc"
sProduct="SN-Dev"
sSerialnumber="01234567890123"
sConfiguration="Config FSG"
```

# Device descriptor Setting
```
# http://isticktoit.net/?p=1383
bcd_usb=0x0200          # USB 2.0
id_vendor=0x1d6b        # Linux Foundation
id_product=0x0104       # Multifunction Composite Gadget
bcd_device=0x0090       # v 0.9
language_id=0x0409
sManufacture="Socionext Inc"
sProduct="SN-UVC"
sSerialnumber="01234567890123"
sConfiguration="Config YUV"
```