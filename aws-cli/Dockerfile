FROM ubuntu:latest

# Aws cli install on ubuntu
ENV AWSCLI_VERSION='2.11.19'


RUN command  curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o /tmp/awscliv2.zip
RUN  unzip -q /tmp/awscliv2.zip -d /tmp
RUN command  rm /tmp/awscliv2.zip
RUN  sudo /tmp/aws/install --update
RUN  rm -rf /tmp/aws/

ENTRYPOINT ["aws"]