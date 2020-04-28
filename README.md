# PermissionX
PermissionX是一个用于简化运行时权限用法的开源库。是学习郭霖的《第一行代码》练手的项目

## 配置
添加如下配置将PermissionX引入到你的项目当中
```groovy
dependencies {
    ...
    implementation 'com.jsnow.permissionx:permissionx:1.0.0'
}
```


## 使用
```kotlin
    PermissionX.request(this,
    android.Manifest.permission.CALL_PHONE){
        allGranted,deniedList ->
        if (allGranted){
            call()
        }else{
            Toast.makeText(this,"you denied $deniedList",Toast.LENGTH_SHORT).show()
        }
    }
```