# synocodectool-patch

![GitHub last commit](https://img.shields.io/github/last-commit/likeadoc/synocodectool-patch)

This patch enables transcoding on Synologys DiskStation Manager 6+ without a valid serial number.
The structure is loosely based on https://github.com/keylase/nvidia-patch



Requirements:
- DiskStation Manager 6 or higher
- Your serial number must be in the proper format (e.g. XXXXPDNXXXXXX for DS918+, XXXXODNXXXXXX for DS3617xs, XXXXLWNXXXXXX for 3615xs)
- x86-64 based 
- SSH/Terminal Access
- sudo/root

## Version Table

| Version | Patch supported | Original SHA1 | Patch SHA1 | Original| Patch |
|:--------|:---------------:|:-------------:|:----------:|:-------:|:-----:|
|6.0 7321-0 -<br> 6.0.3 8754-8    | :heavy_check_mark:  | cde88ed8fdb2bfeda8de5<br>2ef3adede87a72326ef | e5c1a65b396796856047<br>6fcda5071fd37db40223 | [Link](../../raw/master/synocodectool/original/synocodectool.6.0-7321-0_6.0.3-8754-8.original)| [Link](../../raw/master/synocodectool/original/synocodectool.6.0-7321-0_6.0.3-8754-8.patch) |
|6.1 15047-0 -<br> 6.1.1 15101-4  | :heavy_check_mark:  | ec0c3f5bbb857fa84f5d<br>1153545d30d7b408520b | d58f5b33ff2b6f214103<br>6837ddf15dd5188384c6 | [Link](../../raw/master/synocodectool/original/synocodectool.6.1-15047-0_6.1.1-15101-4.original) | [Link](../../raw/master/synocodectool/original/synocodectool.6.1-15047-0_6.1.1-15101-4.patch) |
|6.1.2 15132-0 -<br> 6.1.3 15152-8| :heavy_check_mark:  | 1473d6ad6ff6e5b8419c<br>6b0bc41006b72fd777dd | 56ca9adaf117e8aae9a3<br>a2e29bbcebf0d8903a99 | [Link](../../raw/master/synocodectool/original/synocodectool.6.1.2-15132-0_6.1.3-15152-8.original) | [Link](../../raw/master/synocodectool/original/synocodectool.6.1.2-15132-0_6.1.3-15152-8.patch) |
|6.1.4 15217-0 -<br> 6.2 23739-2  | :heavy_check_mark:  | 26e42e43b393811c176d<br>ac651efc5d61e4569305 | 511dec657daa60b0f11d<br>a20295e2c665ba2c749c | [Link](../../raw/master/synocodectool/original/synocodectool.6.1.4-15217-0_6.2-23739-2.original) | [Link](../../raw/master/synocodectool/original/synocodectool.6.1.4-15217-0_6.2-23739-2.patch) |
|6.2.1 23824-0 -<br> 6.2.3 25426-3| :heavy_check_mark:  | 1d01ee38211f21c67a43<br>11f90315568b3fa530e6 | 93067026c251b100e278<br>05a8b4b9d8f0ae8e291c | [Link](../../raw/master/synocodectool/original/synocodectool.6.2.1-23824-0_6.2.3-25426-3.original) | [Link](../../raw/master/synocodectool/original/synocodectool.6.2.1-23824-0_6.2.3-25426-3.patch) |

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

Examples are provided for DSM Version 6.2.2 24992-6

### Downloading and making script executable


```bash
wget https://raw.githubusercontent.com/likeadoc/synocodectool-patch/master/patch.sh
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
bash ./patch.sh -r
```
 
