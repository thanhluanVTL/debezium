ARG DEBEZIUM_VERSION
FROM debezium/connect:$DEBEZIUM_VERSION
ENV KAFKA_CONNECT_JDBC_DIR=$KAFKA_CONNECT_PLUGINS_DIR/kafka-connect-jdbc

# # These should point to the driver version to be used
# ENV MAVEN_DEP_DESTINATION=$KAFKA_HOME/libs \
#     ORACLE_JDBC_REPO="com/oracle/database/jdbc" \
#     ORACLE_JDBC_GROUP="ojdbc8" \
#     ORACLE_JDBC_VERSION="21.6.0.0" \
#     ORACLE_JDBC_MD5=312e6f4ec9932bbf74a4461669970c4b

# RUN docker-maven-download central "$ORACLE_JDBC_REPO" "$ORACLE_JDBC_GROUP" "$ORACLE_JDBC_VERSION" "$ORACLE_JDBC_MD5"

# Deploy PostgreSQL JDBC Driver
RUN cd /kafka/libs && curl -sO https://jdbc.postgresql.org/download/postgresql-42.7.1.jar

USER kafka
