# FROM python:3.8
# # 컨테이너 내에서 코드가 실행될 경로 설정
# WORKDIR /usr/src/emotion-server
# # requirements.txt에 명시된 필요한 packages 설치
# COPY requirements.txt ./
# RUN pip install --upgrade pip
# RUN pip install -r requirements.txt

# COPY . .

# EXPOSE 8000

# # CMD ["python3", "manage.py", "runserver", "0.0.0.0:8084"]
# CMD ["./manage.py", "runserver", "8000"]



FROM python:3.8
# 컨테이너 내에서 코드가 실행될 경로 설정
WORKDIR /usr/src/emotion
# requirements.txt에 명시된 필요한 packages 설치
COPY requirements2.txt ./
RUN pip install --upgrade pip
RUN pip install Django
RUN pip install --upgrade django
RUN python -m django --version
RUN pip install drf-yasg
RUN pip install djangorestframework
RUN pip install mxnet
RUN pip install gluonnlp pandas tqdm
RUN pip install sentencepiece
RUN pip install transformers==3.0.2
RUN pip install mysqlclient
# RUN pip install torch
RUN pip install torch==1.8.0+cpu -f https://download.pytorch.org/whl/torch_stable.html
RUN pip install git+https://git@github.com/SKTBrain/KoBERT.git@master
# RUN pip install -r requirements2.txt
# Project를 /usr/src/app으로 복사
COPY . .
# 포트 설정
EXPOSE 8000

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]