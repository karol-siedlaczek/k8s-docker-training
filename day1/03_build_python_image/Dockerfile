FROM python:3-alpine
WORKDIR /usr/src/app
EXPOSE 5002

COPY main.py ./
COPY requirements.txt ./

RUN pip install --no-cache-dir -r requirements.txt
ENV LOG_LEVEL="INFO" REDIS_HOST=redis REDIS_PORT=6379
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "5002"]
