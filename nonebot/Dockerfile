FROM --platform=linux/amd64 python:3.12-slim

WORKDIR /app
COPY ./app /app

RUN pip install --no-cache-dir --upgrade pip

RUN pip install --no-cache-dir \
    nb-cli==1.4.2 \
    nonebot2==2.3.3 \
    nonebot-adapter-onebot==2.4.5 \
    "nonebot2[fastapi]==2.3.3"

RUN nb plugin install nonebot-plugin-genshinuid

ENV TZ=Asia/Shanghai
CMD ["nb", "run"]
