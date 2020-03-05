FROM httpd:2.4

WORKDIR /home/app
USER root:root
RUN apt-get update \
    && apt-get install -y git vim make gcc curl wget\
    && ln -s /usr/local/apache2/bin/apxs /usr/sbin/apxs \
    && git clone https://github.com/stanaka/mod_dosdetector \
    && cd mod_dosdetector \
    && wget https://techblog.raccoon.ne.jp/wp-content/uploads/2018/04/mod_dosdetector.patch \
    && patch < mod_dosdetector.patch \
    && make install
