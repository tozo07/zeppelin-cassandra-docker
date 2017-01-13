FROM ubuntu:16.04
RUN apt-get update \
&&  apt-get install software-properties-common -y \
&&  add-apt-repository ppa:webupd8team/java -y \
&&  echo oracle-java7-installer shared/accepted-oracle-license-v1-1 select true | /usr/bin/debconf-set-selections \
&&  apt-get update \
&&  apt-get install -y oracle-java7-installer \
&&  apt-get install wget \
&&  wget http://xenia.sote.hu/ftp/mirrors/www.apache.org/zeppelin/zeppelin-0.6.2/zeppelin-0.6.2-bin-all.tgz \
&&  tar xzvf zeppelin-0.6.2-bin-all.tgz \
&&  rm -rf zeppelin-0.6.2-bin-all.tgz \
&&  chown -R root:root /zeppelin-0.6.2-bin-all 

EXPOSE 8080
CMD ["/zeppelin-0.6.2-bin-all/bin/zeppelin.sh"]



#docker stop $(docker ps -a -q)
#docker rm $(docker ps -a -q)

#docker && -tid tozo/zeppelin /bin/bash
#docker exec -tid 32 /bin/bash
#docker && -tid -p8080:8080 tozo/zeppelin



