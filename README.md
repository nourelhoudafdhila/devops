https://github.com/sadofrazer/ic-webapp/tree/master/static/images
FROM python:3.6-alpine
LABEL maintainer-"ULRICH MONJI"
WORKDIR /opt
RUN pip install flask
ADD . /opt/
VOLUME /opt
EXPOSE 8080
ENV ODOO_URL- "https://www.odoo.com/"
ENV PGADMIN_URL-"https: //www.pgadmin.org/"
ENTRYPOINT ["python"]
CMD [ "appy-py" ]
