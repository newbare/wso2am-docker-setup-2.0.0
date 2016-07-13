FROM nuwanbando/javabase

RUN mkdir wso2 

COPY packs/wso2am-2.0.0-SNAPSHOT.zip wso2/

RUN cd wso2/ && \
        unzip wso2am-2.0.0-SNAPSHOT.zip

COPY artifacts/mysql-connector-java-5.1.34-bin.jar /wso2/wso2am-2.0.0-SNAPSHOT/repository/components/lib/
COPY apim-keymanager/carbon/ /wso2/wso2am-2.0.0-SNAPSHOT/
CMD ["sh", "/wso2/wso2am-2.0.0-SNAPSHOT/bin/wso2server.sh"]

EXPOSE 9763
EXPOSE 9443