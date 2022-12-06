

idea/vscode 打开,找到main方法执行就行.
jdk是1.6. 在idea/vscode中使用高版本,指定语言级别就行.
源地址： https://gitee.com/gsls200808/JrebelLicenseServerforJava
# Jrebel & Jet Brains License Server for Java

A license server for Jrebel & JetBrains products, it also support JRebel for Android and XRebel.

***
Thank ilanyu

NOTE: This is provided for educational purposes only. Please support genuine.
***
## Setup
Run:
```
cd /path/to/project
mvn compile 
mvn exec:java -Dexec.mainClass="com.vvvtimes.server.MainServer" -Dexec.args="-p 8081"
```
Packing a runnable jar:
```
mvn package
```
then
```
java -jar JrebelBrainsLicenseServerforJava-1.0-SNAPSHOT-jar-with-dependencies.jar -p 8081
```
default port is 8081.

Or use gradle
```
gradle shadowJar

java -jar JrebelBrainsLicenseServerforJava-1.0-SNAPSHOT-all.jar -p 8081
```
## Docker
Build image
```
mvn package 
docker build -t jrebel-ls .
```

start container
```
docker run -d --name jrebel-ls --restart always -e PORT=9001 -p 9001:9001 jrebel-ls
```
default port is 8081,you can modify it
## Support

Jrebel

JRebel for Android

XRebel

JetBrains Products

## Feedback




