FROM node
LABEL org.label-schema.version=v1.1
RUN mkdir -p /var/node
ADD src/ /var/node/
WORKDIR /var/node
RUN npm install
RUN npm audit fix
EXPOSE 3000
CMD ./bin/www
