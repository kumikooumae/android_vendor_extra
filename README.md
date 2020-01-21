# SystemUIWithLegacyRecents Makefile

Bring back legacy recents (vertical recents view) in Android 10. 

This Makefile will replace SystemUI module with SystemUIWithLegacyRecents, and whitelisting the corresponding priv-app permissions when building your ROM. 

## Usage

Create a new .xml file (in arbitrary name) in .repo/local_manifests/:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<manifest>
  <project name="kumikooumae/android_vendor_extra" path="vendor/extra" remote="github" />
</manifest>
```

If you are building LineageOS or its forked ROMs, it should automatically include the Makefile vendor/extra/product.mk in this repository. (see https://github.com/LineageOS/android_vendor_lineage/blob/e40c31887d92035151cb480d063a617804b9f76c/config/common.mk#L2)

If not, add this line in your makefile:

```
$(call inherit-product-if-exists, vendor/extra/product.mk)
```
