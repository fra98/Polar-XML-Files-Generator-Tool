# Polar XML Files Generator Tool

Polar XML Files Generator Tool is a simple tool developed in Java, that generate for you appmap.xml and theme_resources.xml files, starting from an appfilter.xml file.
It works only with appfilter file generated by Polar Dashboard.

# How it works

You just need to put the .jar file in the same folder where is located the appfilter.xml file. Then just double click on the file and wait for some seconds. The time could change according to the amount of strings located in the file.
I suggest to put the .jar file in 
```
YourProjectDirectory/app/src/main/res/xml
```
which is the correct folder for all three files. The last thing you have to do is to modify some strings at the top of the theme_resources.xml file.
Don't forget to copy and paste appfilter and generated files also in
```
YourProjectDirectory/app/src/main/assets
```

# Download

You can download this repository directly from Github. You will fint the .jar file and the NetBeans Project.
If you want just the .jar file you can download it from [here](https://drive.google.com/file/d/0B4hnOJ-bhWxFbWtKSlVpM2ctaFk/view?usp=sharing).

The code is simple and fully commented. I'm not a developer but I did my best. Feel free to improve it ;)

# Note

**Note that this tool won't work with all appfilter.xml files but only with files generated with Polar (from the in-app icon request generator).
Your appfilter file has to have this formatting if you want that the tool will work
```
<?xml version="1.0" encoding="UTF-8"?>
<resources>
    <iconback img1="iconback" />
    <iconmask img1="iconmask" />
    <iconupon img1="iconupon" />
    <scale factor="1.0" />

    <!-- Polar -->
    <item
        component="ComponentInfo{com.afollestad.polar/com.afollestad.polar.ui.MainActivity}"
        drawable="polar" />
        
</resources>
```
Is not required to have some strings like
```
<?xml version="1.0" encoding="UTF-8"?>

<resources>

<iconback img1="iconback" />

<iconmask img1="iconmask" />

<iconupon img1="iconupon" />

<scale factor="1.0" />

</resources>
```

But it's very important to have this formatting for other strings
```
<!-- Polar -->
<item
    component="ComponentInfo{com.afollestad.polar/com.afollestad.polar.ui.MainActivity}"
    drawable="polar" />
```

