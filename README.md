# CICD
##  安装jdk
    # tar解压jdk安装包 
    mkdir -p /opt/jdk17
    tar zxvf jdk-8u211-linux-x64.tar.gz -C /opt/jdk17 --strip-components 1
    
    # vi /etc/profile
    export JAVA_HOME=/opt/jdk17
    export JRE_HOMR=${JAVA_HOME}/jre
    export CLASSPATH=.:${JAVA_HOME}/lib:${JRE_HOME}/lib
    export PATH=${JAVA_HOME}/bin:$PATH

## 安装jenkins
    下载jenkins最新的war包: latest
    mkdir -p jenkins && /opt/jenkins
    wget -O /opt/jenkins/jenkins.war http://mirrors/jenkins.io/war-stable/latest/jenkins.war
    java -jar jenkins.war --httpPort=8080
   
   
