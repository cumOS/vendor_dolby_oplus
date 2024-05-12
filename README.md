# vendor dolby

OnePlus Dolby to include in custom ROM builds.
Taken from OnePlus 9R

### How to use?

1. Clone this repo to `vendor/dolby`

2. Inherit it from `device.mk` in device tree:

```
# Vendor Dolby
$(call inherit-product, vendor/dolby/dolby.mk)
```

3. Needing to change these in BoardConfig makefile of your device tree:

```bash
DEVICE_FRAMEWORK_COMPATIBILITY_MATRIX_FILE :=

DEVICE_MANIFEST_FILE :=
```

To:

```bash
DEVICE_FRAMEWORK_COMPATIBILITY_MATRIX_FILE +=

DEVICE_MANIFEST_FILE +=
```

Changing the := to += in the device tree, will make, so manifests wont be overwritten

If you face any issues, please report them with proper logs

Credits:
@someone5678
@33bca
@Woomymy
for their work on A14 Dolby bringup

EDIT:
Apparently some users pointed out that this is silimar to HELLBOY017's implementation
and its certainly true, but when I made this repo, I  didnt know that existed.
