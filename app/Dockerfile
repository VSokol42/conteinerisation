ARG IMAGE_VERSION="3.13"

FROM python:${IMAGE_VERSION}

WORKDIR /app

COPY requirements.txt .

RUN pip install --no-cache-dir --upgrade -r ./requirements.txt

COPY . .

EXPOSE 8000

CMD ["uvicorn", "app:app", "--host=0.0.0.0", "--port", "8000"]