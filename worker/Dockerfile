FROM ruizhizhong058/spark-base:3.5.1-hadoop3.3.6

LABEL maintainer="Ruizhi Zhong <ruizhi.zhong@zoom.us>"

COPY worker.sh /

ENV SPARK_WORKER_WEBUI_PORT 8081
ENV SPARK_WORKER_LOG /spark/logs
ENV SPARK_MASTER "spark://spark-master:7077"

EXPOSE 8081

CMD ["/bin/bash", "/worker.sh"]
