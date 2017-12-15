## TWRP device tree for Razer Phone (1st generation 'cheryl')

Add to `.repo/local_manifests/cheryl.xml`:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<manifest>
	<project path="device/razer/cheryl" name="android_device_razer_cheryl" remote="TeamWin" revision="android-7.1" />
</manifest>
```

Then run `repo sync` to check it out.

To build:

```sh
. build/envsetup.sh
lunch omni_cheryl-eng
make -j5 recoveryimage
```

Kernel sources are available at: https://github.com/jcadduono/android_kernel_razer_msm8998/tree/twrp-7.1
