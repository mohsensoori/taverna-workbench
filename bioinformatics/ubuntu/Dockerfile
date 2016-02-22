FROM bigscience/biodesktop:ubuntu
MAINTAINER Fabiano Menegidio

RUN apt-get update
RUN apt-get install graphviz -y

WORKDIR /root/

### Install Java Cryptography Extension
RUN curl -v -j -k -L -H "Cookie:oraclelicense=accept-securebackup-cookie" \
    http://download.oracle.com/otn-pub/java/jce/8/jce_policy-8.zip  > jce_policy-8.zip
RUN unzip /root/jce_policy-8.zip
RUN rm /root/jce_policy-8.zip
RUN cp -R /root/UnlimitedJCEPolicyJDK8/* /usr/lib/jvm/java-8-openjdk-amd64/jre/lib/security/
RUN rm -rf /root/UnlimitedJCEPolicyJDK8/

### Install Taverna Workbench
RUN wget https://bitbucket.org/taverna/taverna-workbench-product/downloads/taverna-workbench-bioinformatics-2.5.0-standalone.zip
RUN unzip taverna-workbench-bioinformatics-2.5.0-standalone.zip
RUN rm taverna-workbench-bioinformatics-2.5.0-standalone.zip

WORKDIR /root/taverna-workbench-bioinformatics-2.5.0/

# Clean up APT when done.
RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

CMD ['taverna.sh']

ENTRYPOINT ["/root/scripts/vnc_startup.sh"]
CMD ["--tail-log"]
