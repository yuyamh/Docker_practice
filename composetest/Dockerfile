FROM python:3.10-alpine
WORKDIR /code
ENV FLASK_RUN_HOST=0.0.0.0
#app.py, requirements.txtを/code配下にコピーする。
COPY . .
RUN pip install -r requirements.txt
CMD ["flask", "run"]
