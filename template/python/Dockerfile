FROM ruizhizhong058/spark-submit:3.5.1-hadoop3.3.6

LABEL maintainer="Ruizhi Zhong <ruizhi.zhong@zoom.us>"

COPY template.sh /

# Copy the requirements.txt first, for separate dependency resolving and downloading
ONBUILD COPY requirements.txt /app/
ONBUILD RUN cd /app \
      && pip3 install -r requirements.txt --break-system-packages

# Copy the source code
ONBUILD COPY . /app

CMD ["/bin/bash", "/template.sh"]
