FROM nuwanbando/javabase

RUN mkdir wso2 

COPY packs/wso2am-2.0.0.zip wso2/

RUN cd wso2/ && \
        unzip wso2am-2.0.0.zip

COPY artifacts/mysql-connector-java-5.1.34-bin.jar /wso2/wso2am-2.0.0/repository/components/lib/
COPY apim-gateway/carbon/ /wso2/wso2am-2.0.0/
CMD ["sh", "/wso2/wso2am-2.0.0/bin/wso2server.sh"]

EXPOSE 8280
EXPOSE 8243
EXPOSE 9763
EXPOSE 9443