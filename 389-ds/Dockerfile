FROM centos

RUN yum -y update && yum clean all
#RUN yum -y remove fakesystemd && yum clean all
#RUN yum -y install systemd && yum clean all
RUN yum install -y epel-release
RUN yum install -y 389-ds-base 389-admin && yum clean all

ADD run.sh /run.sh
ADD ds-setup.inf /tmp/ds-setup.inf

EXPOSE 389 9830

CMD ["/run.sh"]
