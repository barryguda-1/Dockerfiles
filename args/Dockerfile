#Create an image for the weather-app
FROM node
LABEL org.label-schema.version=v1.1
ARG SRC_DIR=/var/node

RUN mkdir -p $SRC_DIR
ADD src/ $SRC_DIR
WORKDIR $SRC_DIR
RUN npm install
EXPOSE 3000
CMD ./bin/www

#Use the --build-arg flag when building an image:
#--build-arg [NAME]=[VALUE]
#docker image build -t linuxacademy/weather-app:v3 --build-arg SRC_DIR=/var/code 
