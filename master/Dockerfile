FROM ruizhizhong058/spark-base:3.5.1-hadoop3.3.6

LABEL maintainer="Ruizhi Zhong <ruizhi.zhong@zoom.us>"

COPY master.sh /

ENV SPARK_MASTER_PORT 7077
ENV SPARK_MASTER_WEBUI_PORT 8080
ENV SPARK_MASTER_LOG /spark/logs

EXPOSE 8080 7077 6066

CMD ["/bin/bash", "/master.sh"]
