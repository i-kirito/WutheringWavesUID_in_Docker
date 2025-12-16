FROM --platform=linux/amd64 python:3.12-slim

WORKDIR /app
COPY ./app /app

RUN pip install --no-cache-dir --upgrade pip

RUN pip install --no-cache-dir \
    nb-cli \
    "nonebot2[fastapi]" \
    nonebot-adapter-onebot

RUN nb plugin install nonebot-plugin-genshinuid

ENV TZ=Asia/Shanghai
CMD ["nb", "run"]
