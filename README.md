# A simple guide to extract super images

### Initial
* Clone that repo with ```git clone https://github.com/YuMiGSIs/Super_Guide```
* Get the super.img file and put it in the same folder as the binary named 'lpunpack'

### Reqs
* Linux machine and patience + brain

### It's extract time
* Note: Some devices have only: system, odm, vendor and product. Oppo/Realme devices can have oppo_product, then use imjtool binary!
* Shell time:
```
# simg2img the super (Do it only if the Super have Sparse)
$ ./imjtool super.img extract

# Get the extracted super
$ mv super.img super.img-old ; mv extracted/* .

# Rename the extracted file to: super.img

# Extract system partition
$ ./lpunpack --partition=system super.img .

# Extract system_ext partition
$ ./lpunpack --partition=system_ext super.img .

# Extract odm partition
$ ./lpunpack --partition=odm super.img .

# Extract product partition
$ ./lpunpack --partition=product super.img .

# Extract vendor partition
$ ./lpunpack --partition=vendor super.img .
```
