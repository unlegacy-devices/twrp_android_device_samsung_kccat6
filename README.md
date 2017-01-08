## TWRP device tree for Galaxy S5 Plus (International)

Add to `.repo/local_manifests/kccat6.xml`:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<manifest>
  <project path="device/samsung/kccat6" name="IonKiwi/twrp_android_device_samsung_kccat6" remote="github" revision="android-6.0" />
  <project path="kernel/samsung/kccat6" name="IonKiwi/android_kernel_samsung_kccat6" remote="github" revision="cm-14.1" />
</manifest>
```

Then run `repo sync` to check it out.

To build:

```sh
. build/envsetup.sh
lunch omni_kccat6-eng
make -j5 recoveryimage
```

Kernel sources are available at: https://github.com/IonKiwi/android_kernel_samsung_kccat6

