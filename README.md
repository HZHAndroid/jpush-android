# jpush-android
【Android项目】极光推送的集成。（文档、工具包、项目）
# 说明
1. 极光推送集成/资源 目录下是极光推送中需要放进自己项目中的相关资源。
2. 极光推送集成/hzh集成的测试项目JpushTest.zip 是hzh的制作的一个可以测试的项目。解压项目后设置build.gradle中的
classpath 'com.android.tools.build:gradle:2.3.2'改为自己Android studio支持的版本。把项目中的gradle\wrapper\gradle-wrapper.properties文件
改为distributionUrl=https\://services.gradle.org/distributions/gradle-3.3-all.zip自己支持的版本。
3. 极光推送集成/集成文档-极光推送.docx 是一份集成步骤的文档。具体的可以下载参考。
# 集成（当前极光推送版本jpush-android-3.1.0，这里的描述不支持图片，如果想看图片的教程，可以下载文档查看）
1. 将“极光推送集成----资源目录”下的“libs”和“res”文件夹下的文件分别拷贝进项目相应的文件夹。
2. 将“极光推送集成----资源目录”下的“AndroidManifest.xml”里面的设置拷贝进行项目的同名文件。然后进行appkey和应用包名的覆盖，以及自定义receiver的配置。
3. 在项目的如下图所示文件，加入避免混淆编译的设置。(看图 极光推送混淆设置.png)
4. 解决极光推送找不到sdk版本问题。如图所示，进行配置。（看图 解决极光推送找不到sdk版本问题.png）
5. 集成可以参考“hzh集成的测试项目JpushTest”，其目录结构如下图所示，并且将图中的receivers和utils文件夹下文件拷贝到项目中。（看图 hzh集成的测试项目JpushTest目录结构.png）
6. 集成完成后，在继承Application的类的onCreate方法调用JPushInterface.setDebugMode(true); JPushInterface.init(this);
提示：具体的参数“hzh集成的测试项目JpushTest” 
