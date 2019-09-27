# Create an image for the weather-app
FROM node
LABEL org.label-schema.version=v1.1
RUN useradd -ms /bin/bash node_user
USER node_user
ADD src/ /home/node_user
WORKDIR /home/node_user
RUN npm install
EXPOSE 3000
CMD ./bin/www

#Build the weather-app image using the non-privileged user node_user:

#docker image build -t linuxacademy/weather-app-nonroot:v1 .


