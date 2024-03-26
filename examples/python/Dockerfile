FROM zhongruizhi/spark-python-template:3.5.1-hadoop3.3.6-aarch64
	  
COPY wordcount.py /app/

ENV SPARK_APPLICATION_PYTHON_LOCATION /app/wordcount.py
ENV SPARK_APPLICATION_ARGS "/spark/README.md"