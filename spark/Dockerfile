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

# install ld-linux-x86-64.so.2
RUN apk add gcompat libc6-compat
