FROM java:8-jre

MAINTAINER 125720240@qq.com

ENV TZ=Asia/Shanghai

RUN ln -sf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone \
    && mkdir -p /black-shop-gateway

WORKDIR /black-shop-auth

EXPOSE 3000

ADD ./target/black-shop-auth.jar ./

CMD  java -Xms300m -Xm300m -Djava.security.egd=file:/dev/./urandom -jar black-shop-auth.jar
