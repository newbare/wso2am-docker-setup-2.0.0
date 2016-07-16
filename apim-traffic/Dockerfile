FROM nuwanbando/javabase

RUN mkdir wso2 

COPY packs/wso2am-2.0.0.zip wso2/

RUN cd wso2/ && \
        unzip wso2am-2.0.0.zip

COPY apim-traffic/carbon/ /wso2/wso2am-2.0.0/
RUN rm -rf /wso2/wso2am-2.0.0/repository/deployment/server/jaggeryapps
RUN rm -rf /wso2/wso2am-2.0.0/repository/deployment/server/webapps
CMD ["sh", "/wso2/wso2am-2.0.0/bin/wso2server.sh"]

EXPOSE 9763
EXPOSE 9443
EXPOSE 5672
EXPOSE 9611
EXPOSE 9711