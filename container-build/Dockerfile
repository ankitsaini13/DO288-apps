# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent

EXPOSE 8080

LABEL io.openshift.expose-service="8080:http" \
	io.k8s.description="bacis" \
	io.k8s.display-name="Apache http server" \
	io.openshift.tags="apache, httpd"

RUN sed -i "s/Listen 80/Listen 8080/g" /etc/httpd/config/httpd.config

RUN chgrp -R 0 /var/logs/httpd /var/run/httpd && \
	chmod -R g=u /var/logs/httpd /var/run/httpd

USER 1001 	 
