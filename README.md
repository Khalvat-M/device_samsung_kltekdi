Copyright 2022 - The Khalvat-M project

Device configuration for Samsung Galaxy S5 Japan variants (SC-04F, SCL23).
========================================

Basic   | Specification List
-------:|:-------------------------
CPU     | Quad-core 2.5 GHz Krait 400
Chipset | Qualcomm MSM8974AC Snapdragon 801
GPU     | Adreno 330
Memory  | 2 GB
Shipped Android Version | 4.4.2
Storage | 16/32 GB
MicroSD | Up to 256 GB
Battery | Removable Li-Ion 2800 mAh
Dimensions | 142 x 72.5 x 8.1 mm (5.59 x 2.85 x 0.32 in)
Display | 1080 x 1920 pixels, 5.1"
Rear Camera  | 16 MP, f/2.2, 31mm, phase detection autofocus, LED flash
Front Camera | 2 MP, f/2.4, 22mm
Release Date | February 2014

![Galaxy S5](https://github.com/Khalvat-M/device_samsung_kltekdi/blob/12.1/information/kltekdi.gif)


# For building Android 12.1
### create `.repo/local_manifests/roomservice.xml` with the following content:

***
```xml
<?xml version="1.0" encoding="UTF-8"?>
 <manifest>
        
 <remote  name="khalvat"
    fetch="https://github.com/Khalvat-M"
    revision="12.1" />

 <remote  name="linos"
    fetch="https://github.com/LineageOS"
    revision="lineage-19.1" />

    <!--LineageOS -->
    <project name="android_hardware_samsung" path="hardware/samsung" remote="linos" />
    <project name="android_hardware_sony_timekeep" path="hardware/sony/timekeep" remote="linos"/>
        
    <!--Device -->
    <project name="device_samsung_kltekdi" path="device/samsung/kltekdi" remote="khalvat" />
    <project name="device_samsung_msm8974-common" path="device/samsung/msm8974-common" remote="khalvat" />
           
    <!--Kernel -->
    <project name="kernel_samsung_msm8974" path="kernel/samsung/msm8974" remote="khalvat" />
    
    <!--Vendor -->
    <project name="vendor_samsung" path="vendor/samsung" remote="khalvat" />
                  
 </manifest>
```
