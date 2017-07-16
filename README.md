# JarClassLoader
Dynamically load class from jar at runtime from anywhere on android

How-to-use:

Import JarClassLoader.aar into your project (File->new->import module->import .aar)

After that import the following class

```
    import com.mordred.jarclassloader.Loader;
```

and then use the following method

```
    Loader.getClassFromJar(Context ctx,String jarLocation,String classPath);

    ctx = use getApplicationContext();

    jarLocation = /storage/emulated... or /storage/sdcard.. or File.getAbsolutePath()
    (note that you need READ_PERMISSION to read that jar)
    
    classPath = inside your jar, choose which class you want to get/instantiate (with package name) (e.g com.xyz.FooClass)

```

It'll return ```Class<?>``` type object

voila.... you get your class object from your jar file and you can use that object to invoke methods or get/set variables etc. (i assume you know basics of reflection)

Happy coding guys...

source will be released when i get some time, stay tuned ;)
