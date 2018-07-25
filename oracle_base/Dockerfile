FROM centos

MAINTAINER Pablo Almeida Galvez "pablo.almeida.galvez@gmail.com"

ENV	CENTOS_FRONTEND	noninteractive

ENV ORACLE_HOME		/u01/app/oracle/product/12.1.0/xe
ENV ORACLE_SID 		xe

RUN yum update -y && yum install -y libaio libaio-devel 
RUN ln -s /usr/bin/awk /bin/awk

RUN groupadd --gid 1001 dba && useradd -g dba -m --uid 1001 oracle

VOLUME /u01/app/oracle/product/12.1.0/xe/dbs
VOLUME /u01/app/oracle/oradata

ADD oracle-12c.tar.gz /
