FROM ruizhizhong058/spark-base:3.5.1-hadoop3.3.6

LABEL maintainer="Ruizhi Zhong <ruizhi.zhong@zoom.us>"

ENV SPARK_MASTER_NAME spark-master
ENV SPARK_MASTER_PORT 7077

COPY submit.sh /

CMD ["/bin/bash", "/submit.sh"]
