# Android Studio Issues

### CMake Error: CMAKE_C_COMPILER not set, after EnableLanguage
Removed '-DANDROID_STL=gnustl_static' from
```
 externalNativeBuild {
    cmake {
        arguments '-DANDROID_PLATFORM=android-16', '-DANDROID_TOOLCHAIN=clang',
                '-DANDROID_ARM_NEON=TRUE'
    }
}
```
### No toolchains found in the NDK toolchains folder for ABI with prefix: mips64el-linux-android

| AStudio Version | NDK Version | Solution |
| --------------- | ----------- | -------- |
| 3.2.1 | 18.0.5002713 | Updated NDK to 18.1.5063045 and gradle to 3.2.1 |


### Unable to find method 'org.gradle.api.internal.artifacts.ivyservice.projectmodule.DefaultProjectPublication.<init(Lorg/gradle/api/artifacts/ModuleVersionIdentifier;)V'.

Updated android-maven-gradle-plugin from 1.7.3 to 2.1

``` 
classpath 'com.github.dcendents:android-maven-gradle-plugin:2.1'
```
### Program type already present: android.support.design.widget.CoordinatorLayout$Behavior

Updated all android support library version from 27.0.2 to 28.0.0

### Program type already present: com.google.android.gms.internal.zzbh
```
   implementation(project(path: ':module_name')){
        exclude group: 'com.google.android.gms' //exclude particular dependency
        //exclude module: 'some_other_module_name' //exclude particular module
    }
```
or
```
   implementation(project(path: ':module_name')){
        transitive false
    }
```
    
