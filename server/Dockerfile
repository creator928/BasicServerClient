# Python 3.10 슬림 버전을 기본 이미지로 사용
FROM python:3.10-slim

# 작업 디렉토리를 /app으로 설정
WORKDIR /app

# requirements.txt 파일을 컨테이너에 복사
COPY requirements.txt .
# pip를 사용하여 필요한 패키지 설치
RUN pip install -r requirements.txt

# 현재 디렉토리의 모든 파일을 컨테이너의 /app에 복사
COPY . .

# uvicorn을 사용하여 FastAPI 애플리케이션 실행
# --host "0.0.0.0": 모든 IP에서 접근 가능하도록 설정
# --port "8000": 8000번 포트로 서비스 실행
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]