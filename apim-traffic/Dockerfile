FROM nuwanbando/javabase

RUN mkdir wso2 

COPY packs/wso2am-2.0.0-SNAPSHOT.zip wso2/

RUN cd wso2/ && \
        unzip wso2am-2.0.0-SNAPSHOT.zip

COPY apim-traffic/carbon/ /wso2/wso2am-2.0.0-SNAPSHOT/
RUN rm -rf /wso2/wso2am-2.0.0-SNAPSHOT/repository/deployment/server/jaggeryapps
RUN rm -rf /wso2/wso2am-2.0.0-SNAPSHOT/repository/deployment/server/webapps
CMD ["sh", "/wso2/wso2am-2.0.0-SNAPSHOT/bin/wso2server.sh"]

EXPOSE 9763
EXPOSE 9443
EXPOSE 5672
EXPOSE 9611
EXPOSE 9711