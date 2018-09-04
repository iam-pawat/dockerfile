FROM pawatiamsupa/s2i-base 

VOLUME [ "/report" ]
ENV TZ="Asia/Bangkok"

USER root
# Necessary to permit running with a randomised UID
RUN mkdir /usr/lib/jvm/java-1.8.0-openjdk/lib/fonts \
    && chmod -R "g+rwX" /usr/lib/jvm/java-1.8.0-openjdk/lib/fonts \
    && chown -R jboss:root /usr/lib/jvm/java-1.8.0-openjdk/lib/fonts \
    && mkdir /rpt \
    && chmod -R "g+rwX" /rpt \
    && chown -R jboss:root /rpt

ADD fonts /usr/lib/jvm/java-1.8.0-openjdk/lib/fonts
ADD src/main/resources/ /rpt

USER 1000