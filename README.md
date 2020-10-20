# dimeno-collector
> 资源收集压缩工具

[![Platform](https://img.shields.io/badge/Platform-Android-00CC00.svg?style=flat)](https://www.android.com)
[![](https://jitpack.io/v/dimeno-tech/dimeno-collector.svg)](https://jitpack.io/#dimeno-tech/dimeno-collector)

根目录

``` gradle
allprojects {
	repositories {
		...
		maven { url 'https://jitpack.io' }
	}
}
```
项目目录

``` gradle
dependencies {
	implementation 'com.github.dimeno-tech:dimeno-collector:0.0.1'
}
```

### interface

``` java
public interface Collector {
    String collect(String path);
    void collect(String path, Callback callback);
}
```

### 同步压缩

``` java
AppCollector.get().collect("source path")
```

### 异步压缩

``` java
AppCollector.get().collect("source path", new AbsCallback() {
    @Override
    public void onSuccess(String path) {

    }
});
```
