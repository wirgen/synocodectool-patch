# synocodectool-patch

![GitHub last commit](https://img.shields.io/github/last-commit/wirgen/synocodectool-patch)

This patch enables transcoding on Synologys DiskStation Manager 6+ without a valid serial number.
The structure is loosely based on https://github.com/keylase/nvidia-patch

### Requirements:
- DiskStation Manager 6 or higher
- Your serial number ***must*** be in the proper format (e.g. XXXXPDNXXXXXX for DS918+, XXXXODNXXXXXX for DS3617xs, XXXXLWNXXXXXX for 3615xs)
- x86-64 based
- SSH/Terminal Access
- sudo/root

## Version Table

| Version | Patch supported | Original SHA1 / Patched SHA1 | Original | Patch |
|:--------|:---------------:|:----------------------------:|:--------:|:-----:|
|6.0 7321-0 -<br>6.0.3 8754-8| :heavy_check_mark: | cde88ed8fdb2bfeda8de52ef3adede87a72326ef <br> e5c1a65b3967968560476fcda5071fd37db40223 | [Link](../../raw/master/synocodectool/original/synocodectool.6.0-7321-0_6.0.3-8754-8.original) | [Link](../../raw/master/synocodectool/patch/synocodectool.6.0-7321-0_6.0.3-8754-8.patch) |
|6.1 15047-0 -<br>6.1.1 15101-4| :heavy_check_mark: | ec0c3f5bbb857fa84f5d1153545d30d7b408520b <br> d58f5b33ff2b6f2141036837ddf15dd5188384c6 | [Link](../../raw/master/synocodectool/original/synocodectool.6.1-15047-0_6.1.1-15101-4.original) | [Link](../../raw/master/synocodectool/patch/synocodectool.6.1-15047-0_6.1.1-15101-4.patch) |
|6.1.2 15132-0 -<br>6.1.3 15152-8| :heavy_check_mark: | 1473d6ad6ff6e5b8419c6b0bc41006b72fd777dd <br> 56ca9adaf117e8aae9a3a2e29bbcebf0d8903a99 | [Link](../../raw/master/synocodectool/original/synocodectool.6.1.2-15132-0_6.1.3-15152-8.original) | [Link](../../raw/master/synocodectool/patch/synocodectool.6.1.2-15132-0_6.1.3-15152-8.patch) |
|6.1.4 15217-0 -<br>6.2 23739-2| :heavy_check_mark: | 26e42e43b393811c176dac651efc5d61e4569305 <br> 511dec657daa60b0f11da20295e2c665ba2c749c | [Link](../../raw/master/synocodectool/original/synocodectool.6.1.4-15217-0_6.2-23739-2.original) | [Link](../../raw/master/synocodectool/patch/synocodectool.6.1.4-15217-0_6.2-23739-2.patch) |
|6.2.1 23824-0 -<br>6.2.3 25426-3| :heavy_check_mark: | 1d01ee38211f21c67a4311f90315568b3fa530e6 <br> 93067026c251b100e27805a8b4b9d8f0ae8e291c | [Link](../../raw/master/synocodectool/original/synocodectool.6.2.1-23824-0_6.2.3-25426-3.original) | [Link](../../raw/master/synocodectool/patch/synocodectool.6.2.1-23824-0_6.2.3-25426-3.patch) |
|7.0.1 42216-0 -<br>7.0.1 42218-3| :heavy_check_mark: | c2f07f4cebf0bfb63e3ca38f811fd5b6112a797e <br> 873749b00e1624df4b01335e0b69102acc185eb9 | [Link](../../raw/master/synocodectool/original/synocodectool.7.0.1-42216-0_7.0.1-42218-3.original) | [Link](../../raw/master/synocodectool/patch/synocodectool.7.0.1-42216-0_7.0.1-42218-3.patch) |
|7.1 42661-0 -<br>7.1 42661-4| :heavy_check_mark: | 796ac7fab2dcad7978a0e8ae48abc9150aba916c <br> 06d543b2aab5ea73600ca96497febdad96dc7864 | [Link](../../raw/master/synocodectool/original/synocodectool.7.1-42661-0_7.1-42661-0.original) | [Link](../../raw/master/synocodectool/patch/synocodectool.7.1-42661-0_7.1-42661-0.patch) |
|7.1 42661-0 -<br>7.1 42661-4<br>(CodecPack)| :heavy_check_mark: | 22445f5b0d8b6714954b50930c47b8805cf32b98 <br> 3a5ed18dc41ff243f3481b6e3cf4770651df0b54 | [Link](../../raw/master/synocodectool/original/synocodectool.7.1-42661-0_7.1-42661-0.CodecPack.original) | [Link](../../raw/master/synocodectool/patch/synocodectool.7.1-42661-0_7.1-42661-0.CodecPack.patch) |
|7.1.1 42962-0 -<br>7.1.1 42962-6| :heavy_check_mark: | 18461b62813166652fd64a96e06237fde81925f7 <br> 4bfa2a72da607752435e432545f98f1a0b3815a8 | [Link](../../raw/master/synocodectool/original/synocodectool.7.1.1-42962-2.original) | [Link](../../raw/master/synocodectool/patch/synocodectool.7.1.1-42962-2.patch) |
|7.2 64570-0 -<br>7.2 64570-1| :heavy_check_mark: | d316d5b2b080346b4bc197ad5ad7994ac043a15d <br> 8ffe49d91dc0fcd3268ff1afcbc9132d1ae634d1 | [Link](../../raw/master/synocodectool/original/synocodectool.7.2-64570-0.original) | [Link](../../raw/master/synocodectool/patch/synocodectool.7.2-64570-0.patch) |
|7.2.1 69057-0 -<br>7.2.1 69057-3| :heavy_check_mark: | a205aa337d808213cf6d4d839b035cde0237b424 <br> 1f4491bf5f27f0719ddebdcab6ff4eff56c64b2c | [Link](../../raw/master/synocodectool/original/synocodectool.7.2.1-69057-0.original) | [Link](../../raw/master/synocodectool/patch/synocodectool.7.2.1-69057-0.patch) |

:warning: : Not tested yet

## Synopsis

```
# sudo ./patch.sh -h

SYNOPSIS
    patch.sh [-h] [-p|-r|-l]
DESCRIPTION
    Patch to enable transcoding without a valid serial in DSM 6+
    	-h      Print this help message
        -p      Patch synocodectool
        -r      Restore original from backup        
        -l      List supported DSM versions

```

## Manual

### Downloading and making script executable

```bash
wget https://raw.githubusercontent.com/wirgen/synocodectool-patch/master/patch.sh
chmod +x patch.sh
```

### Patching synocodectool

This patch performs a backup of the original file prior to making changes.

```bash
sudo ./patch.sh -p
```

### Restoring original file

If something goes horribly wrong restoring the original file is possible

```bash
sudo ./patch.sh -r
```
