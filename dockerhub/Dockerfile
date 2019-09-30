FROM node AS build
RUN mkdir -p /var/node/
ADD src/ /var/node/
WORKDIR /var/node
RUN npm install

FROM node:alpine
ARG VERSION=V1.1
LABEL org.label-schema.version=$VERSION
ENV NODE_ENV="production"
COPY --from=build /var/node /var/node
WORKDIR /var/node
EXPOSE 3000
ENTRYPOINT ["./bin/www"]

##Build the image:

#docker image build -t <USERNAME>/weather-app:<HASH> --build-arg VERSION=1.5 .

##Tag the image before pushing it to Docker Hub:

#docker image tag linuxacademy/weather-app:<HASH> <USERNAME>/weather-app:<HASH>

##Push the image to Docker Hub:

#docker login
#docker image push <USERNAME>/weather-app:<HASH>

##Tag the latest image:

#docker image tag <USERNAME>/weather-app:<HASH> <USERNAME>/weather-app:latest

##Push the latest image to Docker Hub:

#docker login <USERNAME>
#docker image push <USERNAME>/weather-app:latest

