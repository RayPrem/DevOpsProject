FROM ubuntu:22.04
ENV TZ=Asia/Dubai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
RUN apt-get update && apt-get install unzip nginx -y
WORKDIR /var/www/html
COPY 2137_barista_cafe.zip /var/www/html
RUN unzip 2137_barista_cafe.zip
RUN mv 2137_barista_cafe/* .
RUN rm -r 2137_barista_cafe.zip 2137_barista_cafe
CMD ["nginx", "-g", "daemon off;"]

