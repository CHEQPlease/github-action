FROM ubuntu:latest

# Aws cli install on ubuntu

RUN command  curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o /tmp/awscliv2.zip
RUN  unzip -q /tmp/awscliv2.zip -d /tmp
RUN command  rm /tmp/awscliv2.zip
RUN  sudo /tmp/aws/install --update
RUN  rm -rf /tmp/aws/

# helm packages install on ubuntu

RUN  curl https://baltocdn.com/helm/signing.asc | gpg --dearmor | sudo tee /usr/share/keyrings/helm.gpg > /dev/null
RUN  sudo apt-get install apt-transport-https --yes
RUN  echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/helm.gpg] https://baltocdn.com/helm/stable/debian/ all main" | sudo tee /etc/apt/sources.list.d/helm-stable-debian.list
RUN  sudo apt-get update
RUN  sudo apt-get install helm

ENTRYPOINT ["aws", "helm"]