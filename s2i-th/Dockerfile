FROM fabric8/s2i-java:2.1
EXPOSE 8080 8778 9779
USER root
ENV TZ="Asia/Bangkok"
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
USER 185