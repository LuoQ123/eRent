FROM openjdk:8-jdk-alpine
VOLUME /tmp
# ARG：指定一些镜像内使用的参数(例如版本号)，在执行docker build命令时以–build-arg< varname>=< value>的格式传入。
ARG JAR_FILE
COPY ${JAR_FILE} app.jar
# EXPOSE：声明镜像内服务所监听的端口
EXPOSE 9000
# ENTRYPOINT：指定镜像的默认入口命令。该命令会在容器启动时作为根命令执行，所有传入值作为该命令的参数。
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]