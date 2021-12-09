FROM python:3.8
# 컨테이너 내에서 코드가 실행될 경로 설정
WORKDIR /usr/src/emotion-server
# requirements.txt에 명시된 필요한 packages 설치
COPY requirements.txt ./
RUN pip install --upgrade pip
RUN pip install -r requirements.txt

COPY . .

EXPOSE 8000

# CMD ["python3", "manage.py", "runserver", "0.0.0.0:8084"]
CMD ["./manage.py", "runserver", "8000"]