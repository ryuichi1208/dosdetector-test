FROM httpd:2.4

WORKDIR /home/app
USER root:root
RUN apt-get update \
    && apt-get install -y git vim make gcc \
    && ln -s /usr/local/apache2/bin/apxs /usr/sbin/apxs \
    && git clone https://github.com/stanaka/mod_dosdetector \
    && cd mod_dosdetector && make install
