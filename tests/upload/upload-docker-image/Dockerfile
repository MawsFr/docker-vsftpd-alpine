
ARG CENTOS_FTP_IMAGE_REPOSITORY
ARG CENTOS_FTP_IMAGE_REPOSITORY_TAG
FROM $CENTOS_FTP_IMAGE_REPOSITORY:$CENTOS_FTP_IMAGE_REPOSITORY_TAG

ARG LAUNCH_SCRIPT_LOCAL_FILE
ARG APP_PATH=/app
ARG LAUNCH_SCRIPT_CONTAINER_PATH=$APP_PATH/launch.sh

ENV LAUNCH_SCRIPT_CONTAINER_PATH $LAUNCH_SCRIPT_CONTAINER_PATH

RUN mkdir -p $APP_PATH
WORKDIR $APP_PATH

COPY testfile.txt $APP_PATH/testfile.txt
COPY $LAUNCH_SCRIPT_LOCAL_FILE $LAUNCH_SCRIPT_CONTAINER_PATH

RUN chmod +x $LAUNCH_SCRIPT_CONTAINER_PATH

CMD /bin/sh $LAUNCH_SCRIPT_CONTAINER_PATH