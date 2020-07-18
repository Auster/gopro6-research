## DATA.bin unpack
Please use script provided by [hypoxic](https://github.com/hypoxic/GoProHERO8/tree/master/tools/unpackh6)
~You can find my MacOS version [here]()~

## File structure

```
$ file ./*
./sector00.bin: data
./sector02.bin: data
./sector04.bin: big endian ispell hash file (?), and 20736 string characters
./sector05.bin: data
./sector07.bin: data
./sector08.bin: Linux rev 1.0 ext4 filesystem data, UUID=2affdb0d-3948-49fe-9eb9-27b0d7068d83 (extents) (large files) (huge files)
./sector09.bin: DIY-Thermocam raw data (Lepton 3.x), scale 19648-38373, spot sensor temperature -88471305153451388829696.000000, unit celsius, color scheme 4, calibration: offset 0.000000, slope 118128640.000000
./sector11.bin: data
./sector12.bin: data
./sector13.bin: data
./sector14.bin: data
```_fileCRC
```

GoPro 6 DATA.bin unpacked

```
(master)$ md5 ../1.6.unpacked/* | sort
MD5 (../1.6.unpacked/sector00.bin) = 05f9f3e4fe3b5faa1c56337b18cdbd61
MD5 (../1.6.unpacked/sector02.bin) = f6b281858f91106e9a180e8cdfb45ac4
MD5 (../1.6.unpacked/sector04.bin) = fca5302db3c7180dacf1ebe69bec474e
MD5 (../1.6.unpacked/sector07.bin) = a845417a4194cfc945f692514f0c9f3e
MD5 (../1.6.unpacked/sector08.bin) = b91d1921253fefb5391e13ba528dd31a
MD5 (../1.6.unpacked/sector09.bin) = 1a13703276e1e185149cbd10ac0bbc89
MD5 (../1.6.unpacked/sector11.bin) = 8553db7a557e63b52f73c17831cf9b0b
MD5 (../1.6.unpacked/sector12.bin) = 4d03b76b9900da09d5e717ceef7db410
MD5 (../1.6.unpacked/sector13.bin) = bc2ffc8587fc61ef00b4b0b04fc41f43
MD5 (../1.6.unpacked/sector14.bin) = 5958150951eff98cdf168dd2332a373d
```


GoPro 7 DATA.bin unpacked
```
(master)$ md5 ../gp7.unpacked/* | sort
MD5 (../gp7.unpacked/sector00.bin) = c0689c7e0a7ffc5826fc4a14bec0bf40
MD5 (../gp7.unpacked/sector02.bin) = 04f75a747247a48288b3147bd8ca2fbc
MD5 (../gp7.unpacked/sector04.bin) = 3ed32cf889491c5fbb7230af7da7a91d
MD5 (../gp7.unpacked/sector05.bin) = 21e45eb1435fec71c5b8450cea6789ab
MD5 (../gp7.unpacked/sector07.bin) = 2d275dbee53ee88a685e48d7187b2134
MD5 (../gp7.unpacked/sector08.bin) = 606181821aefc4bd018ff72f14b83735
MD5 (../gp7.unpacked/sector09.bin) = 1a13703276e1e185149cbd10ac0bbc89
MD5 (../gp7.unpacked/sector11.bin) = 8553db7a557e63b52f73c17831cf9b0b
MD5 (../gp7.unpacked/sector12.bin) = 4d03b76b9900da09d5e717ceef7db410
MD5 (../gp7.unpacked/sector13.bin) = 6053558b95e5dc95a4448601f60dd9a8
MD5 (../gp7.unpacked/sector14.bin) = 737b780561a8583178939c2cf24c2e90
```

Same sectors: 9, 11, 12

## Sectors destiny:
# Sector 4
Description: FreeRTOS image

# Sector 8
Desctiption: Linux root (ext4)

Tips&Tricks:
MacOS:
```sh
mkdir ./sector8
ext4fuse ./sector8.bin ./sector8 -o allow_other

```