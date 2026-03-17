FROM python:3.10-alpine

WORKDIR /app

COPY . .

RUN pip install --upgrade pip
RUN pip install -r requirements.txt

ENV PORT=5000

EXPOSE 5000

CMD ["python","app.py"]
