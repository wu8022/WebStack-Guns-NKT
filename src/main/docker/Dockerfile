#使用基础镜像
FROM java:8

#作者
MAINTAINER wuzhu

# 指定临时文件目录为/tmp
# 其效果是在主机 /var/lib/docker 目录下创建了一个临时文件,并连接到容器的/tmp
VOLUME /tmp

#将jar 包添加到容器中并更名为 ap.jar
ADD webstack-nav-1.0.jar app.jar

#运行jar包
RUN bash -c 'touch /app.jar'
ENTRYPOINT ["java","-Djava.security.edg=file:/dev/./urandom","-jar","/app.jar"]