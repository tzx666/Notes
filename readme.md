# 小米便签2012款moudle包
这个开源项目太老了。老到网络请求和一堆api都废弃掉了，也没有提供编译项
为了方便开发，特意做了一个moudle包，同时这也是一个完整的可以跑起来的工程，只要在清单文件里声明启动activity即可
做的改动：注释掉了网络请求，注释掉了隐式跳转功能
## 使用方式
### 以模块形式依赖
（推荐读懂之后在模块的基础上继承修改，api太老了还不如自己写一个）
第一步：minote-release.aar复制到libs目录下，如果没有就新建一个，在app下的build.gradle下

android{
    ...
    repositories {
    flatDir {
        dirs 'libs'
    }
    ...
}
}


第二步：在dependencies 中这么添加进去就好了。


dependencies {
    implementation(name: 'minote-release', ext: 'aar')
}
### 在项目基础上开发
在清单文件里声明启动activity，重新build即可