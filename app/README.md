# Homework for lecture 2


## Level 1

Dockerfile

    FROM python:3.13
    WORKDIR /app
    COPY . .
    RUN pip install -r ./requirements.txt
    EXPOSE 8000
    CMD ["uvicorn", "app:app", "--host=0.0.0.0", "--port", "8000"]

Building

    docker build . -t hw_lec2:1.0

Running

    docker run -p 8000:8000 hw_lec2:1.0