#I used open source image which dosen't include X-pack features 
FROM docker.elastic.co/logstash/logstash-oss:6.2.3
RUN rm -f /usr/share/logstash/pipeline/logstash.conf
ADD pipeline/ /usr/share/logstash/pipeline/
ADD patterns/ /usr/share/logstash/patterns/
RUN logstash-plugin install --no-verify logstash-input-beats

