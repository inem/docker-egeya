FROM progrium/busybox
RUN opkg-install curl unzip
ENV EGEYA_VERSION 2858

RUN mkdir /egeya
WORKDIR /egeya
RUN curl -O http://blogengine.ru/download/e2_distr_v${EGEYA_VERSION}.zip
RUN unzip *.zip
RUN rm -f *.zip

VOLUME ["/egeya"]
