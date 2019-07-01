#-----------------------------------------------------------
# Image Setup
#-----------------------------------------------------------
#
# To edit the 'big-data-europe/docker-spark' base Image
# Github: https://github.com/big-data-europe/docker-spark
#
#

ARG SPARK_VERSION

FROM bde2020/spark-master:${SPARK_VERSION}

LABEL maintainer="kangell <leikou@163.com>"

# snappy must mount on a execution directory
ENV JVM_OPTS=-Dorg.xerial.snappy.tempdir=/tmp

###############
# echo "http://dl-8.alpinelinux.org/alpine/edge/community" >> /etc/apk/repositories
# apk --no-cache --update-cache add gcc gfortran python python-dev py-pip build-base wget freetype-dev libpng-dev openblas-dev
# ln -s /usr/include/locale.h /usr/include/xlocale.h
# pip install numpy scipy pandas matplotlib

# install ld-linux-x86-64.so.2
RUN apk add gcompat libc6-compat \
    && echo "http://dl-8.alpinelinux.org/alpine/edge/community" >> /etc/apk/repositories \
    && apk --no-cache --update-cache add gcc gfortran python python-dev py-pip build-base wget freetype-dev libpng-dev openblas-dev \
    && ln -s /usr/include/locale.h /usr/include/xlocale.h \
    && python -m pip install --upgrade pip \
    && python -m pip install numpy scipy pandas matplotlib
