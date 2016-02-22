FROM bigscience/biodesktop:ubuntu
MAINTAINER Fabiano Menegidio

RUN apt-get update
RUN apt-get install graphviz -y

WORKDIR /root/

### Install Java Cryptography Extension
RUN wget -c --no-cookies --no-check-certificate --header "Cookie: gpw_e24=http%3A%2F%2Fwww.oracle.com" \
    http://download.oracle.com/otn-pub/java/jce/8/jce_policy-8.zip -O jce_policy-8.zip
RUN unzip /root/jce_policy-8.zip
RUN rm /root/jce_policy-8.zip
RUN mv /root/UnlimitedJCEPolicyJDK8/* /usr/lib/jvm/java-8-opendjk-amd64/jre/lib/security/
RUN rm -rf /root/UnlimitedJCEPolicyJDK8/

### Install Taverna Workbench
RUN wget https://bitbucket.org/taverna/taverna-workbench-product/downloads/taverna-workbench-bioinformatics-2.5.0-standalone.zip
RUN gunzip taverna-workbench-bioinformatics-2.5.0-standalone.zip
RUN rm taverna-workbench-bioinformatics-2.5.0-standalone.zip

WORKDIR /root/taverna-workbench-bioinformatics-2.5.0/

CMD ['taverna.sh']
