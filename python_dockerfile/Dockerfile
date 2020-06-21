FROM centos

RUN yum install python36 -y

RUN mkdir /python/
COPY hello.py /python/

ENTRYPOINT [ "python3" ]


CMD [ "/python/" ]




