FROM jatayu99/my-tomcat:latest
ADD prometheus-jmx-config.yml /prometheus-jmx-config.yml
ADD jmx_prometheus_javaagent-0.13.0.jar /jmx_prometheus_javaagent-0.13.0.jar
COPY ConferenceRoomCapstoneB35.war /usr/local/tomcat/webapps
ENV JAVA_OPTS="-javaagent:/jmx_prometheus_javaagent-0.13.0.jar=9830:/prometheus-jmx-config.yml"
EXPOSE 8080 9830
CMD ["/usr/local/tomcat/bin/catalina.sh", "run"]
