FROM python:3.12.2-alpine3.18

ENV CURRENT_ENVIRONMENT=development

COPY ./ /app
WORKDIR /app

EXPOSE 5000

RUN pip install -r requirements.txt

CMD ["python3", "-m", "flask", "run", "--host=0.0.0.0"]