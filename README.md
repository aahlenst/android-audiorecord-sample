# Android AudioRecord Sample

This is a sample project that demonstrates how to record audio on an Android device using the [`AudioRecord`](https://developer.android.com/reference/android/media/AudioRecord.html) class.

## Details

The sample contains multiple Activities, each demonstrating a different scenario to keep the code easily digestable:

* `AudioRecordActivity`: Records PCM using the internal microphones
* `BluetoothRecordActivity`: Records PCM using a Bluetooth HFP device

To launch the desired Activity, change the `AndroidManifest.xml` accordingly.

The output is written to the device's SD card and can be downloaded from there using `adb`:

```shell
adb pull /sdcard/recording.pcm ~/Desktop/recording.pcm
```

To listen to the PCM use [Audacity](http://www.audacityteam.org) or a similar software. To import a PCM into Audacity use the menu *File* > *Import* > *RAW data*. The endianness of the PCM is usually Little Endian on Android devices (x86, ARM).

## License

This software is licensed under the terms of the Apache License, Version 2.0.
