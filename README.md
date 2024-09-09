# SKN01-4th-4Team
Vue + Django + FastAPI + Deep Learning Local Server 서비스

### 🧑🏻‍🌾 TextFarmers(TF)

# 1. Introduction Team (팀 소개)
<table align="center">
  <tbody>
    <tr>
      <td align="center">
        <div>
          <img src="https://github.com/user-attachments/assets/7cbbcc77-39de-4dc6-be12-a2879ce15a0b"width="100px;"height="100px;" alt=""/>
          <a href="https://github.com/yhoon3002"><div align=center>팀장 임영훈</div></a>
        </div>
      </td>
      <td align="center">
        <div>
          <img src="https://github.com/user-attachments/assets/c7df2eb9-d897-4acc-87a9-3cdbca2863a6"width="100px;"height="100px;"" alt=""/>
          <a href="https://github.com/2kilometer"><div align=center>이경민</div></a>
        </div>
      </td>
      <td align="center">
        <div>
          <img src="https://github.com/user-attachments/assets/4d97616d-34b6-4495-aa18-dc1bb2733d4a"width="100px;"height="100px;" alt=""/>
          <a href="https://github.com/JUNGUIHEON"><div align=center>정의헌</div></a>
        </div>
      </td>
    </tr>
  </tbody>
</table>

<br><br>

# 2. Introduction Project (프로젝트 개요)
### 🧡 소개 🧡
**의료 데이터를 활용한 챗봇 서비스**  <br><br>
### 💚 필요성 💚
![image](https://github.com/user-attachments/assets/7e8e6655-ef8e-47b0-a836-afbee9a00fa9)
현대 사회에서 의료 데이터의 중요성이 점점 커지고 있습니다.</br>
2024년 의료 정책 추진 반대 집단 행동(aka. 의사 파업)과 같은 사건으로 인해</br>
우리가 언제든지 원할 때 필요한 진료를 받을 수 있다는 안정성이 떨어지며,</br>
우리 스스로 최소한의 의료 지식을 습득해야 할 필요성이 생겼습니다.</br>
하지만 복잡한 의료 정보와 데이터는 일반 대중에게는 접근하기 어렵고</br>
의료계에 지인이 있는 것이 아니라면  물어볼 곳 역시 마땅치 않습니다.</br>
이를 해결하기 위해 딥러닝 기술로 의료 데이터를 학습하여 접근하기 어려웠던 의료 데이터를</br>
모두가 쉽게 접근할 수 있도록 사용자 친화적인 챗봇 서비스를 개발하고자 합니다.


<br><br>
### 💛 주요 서비스 💛
- 건강 진단 챗봇 서비스
- 의료 정보 제공
- 성격유형검사(MBTI) T형과 F형 응답을 선택

 <br><br>
 

# 3. ERD 구성
![image](https://github.com/user-attachments/assets/cb79aba5-ca4c-4cdd-88ec-a622608aba62)


<br><br><br>

# 4. Backend 애자일 보드 - 요구사항 정의서
### ℹ️ 애자일 보드를 사용하는 이유
```
과거 정의서들을 일일히 작성하였지만 빠른 속도로 무언가를 개발하는데 한계가 있습니다.
처음부터 많은 것들을 빌드업하면서 빠른 생산성을 기반으로 움직이려면 반드시 애자일해야합니다.
고로 폭포수 설계 방식이 아닌 애자일 프로세스 방식으로 애자일 보드를 작성하면서 진행했습니다.

애자일 보드는 자체적으로 제목이 요구 사항을 내포하며 각 카드 내부에는 정의한 Domain의 세부 사항이 기록됩니다.
고로 빠르게 팀원들과 협업 할 수 있고 소통 비용을 최소화시킬 수 있습니다.
작은 것 같지만 이와 같은 것들이 쌓여서 아주 기민하고 민첩한 조직을 만들어 냅니다.
```

<br><br><br>

# 5. Frontend 애자일 보드 - 화면 설계서
![image](https://github.com/user-attachments/assets/6e391887-b9a4-4cb7-aa13-71ec49599455)


<br><br><br>

# 6. FastAPI 애자일 보드 - AI 서빙 설계서
![image](https://github.com/user-attachments/assets/25db9a4a-a01c-4199-8dba-96f37b90066e)


<br><br><br>

# 7. Ai-Client 애자일 보드 - AI 서빙 설계서
![image](https://github.com/user-attachments/assets/9ad8b650-2fc2-4aa9-a132-44e20ab309c8)


<br><br><br>

# 7. 시스템 구성도
![image](https://github.com/user-attachments/assets/d7c59ec3-6f89-4948-aea5-40ab30ee0854)
![image](https://github.com/user-attachments/assets/43f264a9-b2fc-4405-9a4a-e235cb9da50d)


<br><br><br>

# 8. ChatBot Service
## 📍 Ai-Client
### 사용자의 질문 의도 파악 모델 학습
- OpenAI API의 "gpt-3.5-turbo"모델에 프롬프트 엔지니어링을 통한 구현</br>
-> 분당 요청수 제한으로 인해 불가능</br>
- BioBERT, KoBERT 모델 사용</br>
-> 정확도가 너무 낮아 사용이 불가능</br>
- 최종적으로 BERT 모델의 다국적 버전을 사용함.</br>
Accuracy: 0.9724</br>
Precision: 0.9725</br>
Recall: 0.9724</br>
F1 Score: 0.9724</br>
97%의 정확도로 프로젝트에 사용하기로 결정</br>
</br>

### 사용자의 질문 & 답변 데이터를 임베딩하고 유사도 비교
- 단어의 빈도를 기준으로 벡터화시키고 cosine유사도 비교</br>
-> 단어의 시제와 조사등이 완전히 동일해야 유사도가 있다고 판단하여 정확도가 떨어짐.</br>
- 형태소를 분석하고 어간을 추출하여 벡터화시키고 cosine유사도 비교</br>
-> 정확도가 조금은 상승했지만 여전히 문장의 문맥을 이해하지 못하고 단순히 같은 단어의 존재유무만으로 유사도를 비교</br>
- BioBERT모델을 사용하여 임베딩</br>
-> 라이브러리 충돌이슈와 임베딩에 소요되는 시간이 너무 길어 사용하기 어려움</br>
- OpenAI API을 이용항 임베딩 및 faiss를 통한 유사도 비교</br>
-> 문맥을 이해하는 고차원 벡터로 임베딩이 가능하고 대규모의 고차원 벡터 데이터셋에 유리한 faiss를 사용해 정확도 상승</br>

### 답변을 MBTI 검사 T성향과 F성향에 맞추어 문체 변환
- OpenAI API를 사용하여 "gpt-3.5-turbo"모델을 통해 프롬프트 엔지니어링을 사용하여 기능 구현
```
    내가 "문체 변환 <INTENTION> <TYPE> <PHASE>"라는 문단을 줄거야. 
    <INTENTION>에는 헬스케어 질문 목적 데이터가, <TYPE>에는 아래에서 정의한 변환 조건의 값이, <PHASE>에는 너가 변환해야하는 문체의 단락이 들어가 있어.
    <INTENTION> 목적에 맞게, <TYPE> 조건에 맞게 <PHASE>의 문체를 바꿔줘.
    최종 출력은 출력 조건에 맞게 출력해줘.
    
    변환 조건: 
    - 만약 TYPE이 "F"라면:
        1. 아픔에 공감하는 방식으로 시작해.
        2. 2인칭으로 지칭해.
        3. 친한 지인과 나누는 구어체에 가깝게 작성해.
        4. 단락 당 안부와 걱정의 말을 한 문장 이상 넣어줘.
        5. 마지막 문장에서는 회복과 극복의 긍정 멘트를 넣어줘.
    
    - 만약 TYPE이 "T"라면:
        1. 정보 전달이 명확하게 가도록 가독성 있게 작성해.
        2. 정보가 나열되어 있다면 <ul style="list-style-position:inside;">로 나열해.
        3. 마지막을 결론 한 문장으로 작성해.
    
    출력 조건:
    - 만약 문단이 나눠졌다면:
        1. <p>태그로 분리해서 출력
        2. 띄어쓰기, \n 없이 출력
```




<br><br><br>

# 9. Autonomous Deploy (자동 배포 진행 절차)
수동 배포는 개발자가 직접 로컬 환경에서 빌드하고 클라우드로 배포하는 과정을 수행하는 반면, 자동 배포는 코드 변경이 감지되면 CI/CD 파이프라인을 통해 자동으로 빌드, 테스트, 배포되어 개발 생산성과 안정성을 높입니다.

#### CI/CD 전체 흐름
  - **개발자 작업 및 테스트** <br>
    : 각 도메인에 맞춰 백로그 작업을 진행합니다. 테스트가 CI(Continuous Integration)를 통과하면 PR(Pull Request)을 승인합니다.
  - **CI에서의 빌드** <br>
    : CI가 통과되면 CD(Continuous Deployment)로 넘어가서 배포가 시작됩니다. 이때 npm build를 실행하여 프로젝트를 빌드합니다.
  - **빌드 결과물 생성** <br>
    : 빌드 후에는 HTML, CSS, JavaScript, 그리고 이미지 등의 리소스가 생성됩니다.
  - **AWS로의 전송** <br>
    : 생성된 정보는 SCP(Secure Copy Protocol)를 사용하여 AWS EC2 인스턴스로 전송됩니다.
  - **Nginx 설정 및 구동** <br>
    : 전송된 파일은 EC2 인스턴스에서 Nginx를 사용하여 호스팅됩니다. 이때 docker-compose.yml 파일을 사용하여 Nginx를 구성합니다.
      Nginx는 어떤 파일들을 서빙할지 설정하며, 이 정보들은 conf 폴더에 저장됩니다.
  - **배포** <br>
    : docker-compose up -d 명령을 통해 Nginx가 설정된 후, Frontend 코드가 EC2 인스턴스에서 동작합니다.

<br><br>

## 📍 Frontend
### CI 구성
### 1. Git 저장소의 Actions 탭에서 ci.yml 파일 생성하기
<img src="https://github.com/user-attachments/assets/b2b8eda5-9f59-497d-9595-b9c0b909e96c"/>

### 2️. CI 설정
```yaml
name: CI (Continuous Integration)

on:
  push:
    branches: ["main"]

jobs:
  build:
    name: Frontend CI
    runs-on: ubuntu-latest
    steps:
    - name: Checkout repository
      uses: actions/checkout@v3

    - name: Set up Node.js
      uses: actions/setup-node@v2
      with:
        node-version: '20'

    - name: Cache dependencies
      id: cache
      uses: actions/cache@v3
      with:
        path: '**/node_modules'
        key: ${{ runner.os }}-node-${{ hashFiles('**/package-lock.json') }}
        restore-keys: |
          ${{ runner.os }}-node-

    - name: Install Dependencies
      if: steps.cache.outputs.cache-hit != 'true'
      run: |
        npm ci

    - name: Create .env development for CI
      run: |
        pwd
        echo "${{ secrets.ENV_DEVELOPMENT }}" > .env.development
        cat .env.development

    - name: Real Test
      run: |
        npm run test:unit

    - name: send FRONTEND_TEST_FINISH_TRIGGER
      run: |
        curl -S -X POST https://api.github.com/repos/${{ github.repository }}/dispatches \
          -H 'Accept: application/vnd.github.v3+json' \
          -u ${{ secrets.GHCR_TOKEN }} \
          -d '{"event_type": "FRONTEND_TEST_FINISH_TRIGGER", "client_payload": { "repository": "'"$GITHUB_REPOSITORY"'" }}'
```

### 4. Actions에서 CI 구동 확인하기
<img src="https://github.com/user-attachments/assets/91ff498e-c28f-4062-9f38-593936610521"/>


### CD 구성
### 1. CI 구성의 1번 과정과 동일
### 2. CD 설정
```yaml
name: CD (Continuous Deploy)

on:
  repository_dispatch:
    types: [FRONTEND_TEST_FINISH_TRIGGER]

jobs:
  build:
    name: build-app
    runs-on: ubuntu-latest
    steps:
    - name: Get Github Actions IP
      id: ip
      uses: haythem/public-ip@v1.2

    - name: Configure AWS IAM Credentials
      uses: aws-actions/configure-aws-credentials@v1
      with:
        aws-access-key-id: ${{ secrets.AWS_ACCESS_KEY_ID }}
        aws-secret-access-key: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
        aws-region: ap-northeast-2

    - name: Checkout repository
      uses: actions/checkout@v3

    - name: Setup node.js
      uses: actions/setup-node@v2
      with:
        node-version: '20'

    - name: Cache dependencies
      id: cache
      uses: actions/cache@v3
      with:
        path: '**/node_modules'
        key: ${{ runner.os }}-node-${{ hashFiles('**/package-lock.json') }}
        restore-keys: |
          ${{ runner.os }}-node-

    - name: Install Dependencies
      if: steps.cache.outputs.cache-hit != 'true'
      run: |
        npm ci --legacy-peer-deps

    - name: Create .env.production for Continuous Deploy
      run: |
        echo "${{ secrets.ENV_PRODUCTION }}" > .env.production
        cat .env.production

    - name: Build
      run: |
        npm run build
        ls

    - name: Setup SSH
      uses: webfactory/ssh-agent@v0.5.0
      with:
        ssh-private-key: ${{ secrets.PRIVATE_KEY }}

    - name: Add Github Actions IP to Security Group
      run: |
        aws ec2 authorize-security-group-ingress --group-id ${{ secrets.AWS_SG_ID }} --protocol tcp --port 22 --cidr ${{ steps.ip.outputs.ipv4 }}/32

    - name: SCP Action
      uses: appleboy/scp-action@master
      with:
        host: ${{ secrets.HOST_IP }}
        username: ec2-user
        key: ${{ secrets.PRIVATE_KEY }}
        source: "./dist/**"
        target: "/home/ec2-user/text-farmer/actions-frontend"

    - name: Remove Github Actions IP From Security Group
      run: |
        aws ec2 revoke-security-group-ingress --group-id ${{ secrets.AWS_SG_ID }} --protocol tcp --port 22 --cidr ${{ steps.ip.outputs.ipv4 }}/32

    - name: SSH Agent Cleanup
      if: ${{ always() }}
      uses: webfactory/ssh-agent@v0.5.0
      with:
        ssh-private-key: ${{ secrets.PRIVATE_KEY }}

  deploy:
    name: Deploy to Production
    needs: build
    runs-on: [ self-hosted, deploy-text-farmer-frontend ]
    steps:
      - name: Get Github Actions IP
        id: ip
        uses: haythem/public-ip@v1.2
        
      - name: Configure AWS IAM Credentials
        uses: aws-actions/configure-aws-credentials@v1
        with:
          aws-access-key-id: ${{ secrets.AWS_ACCESS_KEY_ID }}
          aws-secret-access-key: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
          aws-region: ap-northeast-2

      - name: Add Github Actions IP to Security Group
        run: |
          aws ec2 authorize-security-group-ingress --group-id ${{ secrets.AWS_SG_ID }} --protocol tcp --port 22 --cidr ${{ steps.ip.outputs.ipv4 }}/32
    
      - name: Deploy to Production
        uses: appleboy/ssh-action@v0.1.10
        with:
          host: ${{ secrets.HOST_IP }}
          username: ec2-user
          key: ${{ secrets.PRIVATE_KEY }}
          script_stop: true
          script: |
            pwd
            cd /home/ec2-user/text-farmer/vue-frontend
            cp -r /home/ec2-user/text-farmer/actions-frontend/dist/* ./html/

            docker image prune -f
            docker logout

            docker-compose up -d

      - name: Remove Github Actions IP From Security Group
        run: |
          aws ec2 revoke-security-group-ingress --group-id ${{ secrets.AWS_SG_ID }} --protocol tcp --port 22 --cidr ${{ steps.ip.outputs.ipv4 }}/32
```

### 3. Github에서 Actions Secrets 추가
![image](https://github.com/user-attachments/assets/2b7ca3e8-fcc7-4923-b4c6-54e56b666bca)


### 4. Github Actions Runner 연결
- Github에서 작업
  - Github Actions Runner를 설정 (ARM64 Linux)
<img src="https://github.com/user-attachments/assets/45af381a-97ce-4104-b5fd-3226fbf9cb47"/>
<img src="https://github.com/user-attachments/assets/08e78c76-2d55-4cc5-bc98-fda319631720"/>

- AWS, Gitbash에서 작업
  - AWS 접속
    ```bash
    ssh -i "pem" ec2-user@퍼블릭IPv4주소
    ```
  - frontend용 action runner 디렉토리 생성
    ```bash
    mkdir frontend-action-runner
    cd frontend-action-runner
    ```
  - curl 명령어 입력
    ```bash
    curl -o actions-runner-linux-arm64-2.317.0.tar.gz -L https://github.com/actions/runner/releases/download/v2.317.0/actions-runner-linux-arm64-2.317.0.tar.gz

    tar xzf ./actions-runner-linux-arm64-2.317.0.tar.gz
    ```
    성공
    <img src="https://github.com/user-attachments/assets/c88291d6-d8af-45a5-801f-4d7152a8aa01"/>

  - curl 명령어 입력 Github의 runners 명령어 실행
  - 레이블 설정
    <img src="https://github.com/user-attachments/assets/400a577a-f6ea-4bc4-84df-82b252d90fa0"/>
    <img src="https://github.com/user-attachments/assets/94c7a2f9-c89a-4af9-a729-a1230064cd07"/>
    <img src="https://github.com/user-attachments/assets/ff71d1cb-93cb-445d-97dc-ba0ea5b439fc"/>
    <img src="https://github.com/user-attachments/assets/785a3687-a5ec-493e-9aab-8474ae2f1880"/>
    <img src="https://github.com/user-attachments/assets/edd7b035-84fc-47d0-a399-3c8f08de07d8"/>
  - 구동
    ```bash
    nohup ./run.sh > run.log 2>&1 &
    ```

## 📍 Backend (Server)
- Django CI 설정
  GitHub Actions를 이용하여 Django 프로젝트의 CI를 설정합니다. main 브랜치에서 작업을 수행하며, 파일 형식은 YAML을 사용합니다.

- Django 테스트 자동화
  개발 초기 단계에서 Django 테스트를 자동화하여 CI 파이프라인에 통합합니다. 이를 위해 find_test.sh 스크립트를 사용하여 모든 테스트 파일을 자동으로 인식합니다.
  ```bash
  #!/usr/bin/env bash
  
  TEST_DIRS=$(find . -path ./.venv -prune -o -type d -name 'tests' -print)
  
  APP_TESTS=()
  
  for TEST_DIR in $TEST_DIRS; do
    APP_NAME=$(basename $(dirname $TEST_DIR))
    TEST_FILES=$(find $TEST_DIR -type f -name 'test*.py')
  
    if [ -z "$TEST_FILES" ]; then
      continue
    fi
  
    APP_TESTS+=("${APP_NAME}.tests")
  done
  
  echo "${APP_TESTS[@]}"
```

- Django CD 설정
  CI와 유사하게 GitHub Actions를 활용하여 Django 프로젝트의 CD를 설정합니다.

- Docker 이미지 빌드 및 배포
  빌드 단계에서 다중 환경을 지원하기 위해 Docker Buildx를 사용하여 ARM64 아키텍처의 Docker 이미지를 빌드하고 GitHub Container Registry(GHCR)에 푸시합니다.
  ```yaml
  - name: Build and push Docker image
    run: |
      cd <프로젝트 이름>
      docker buildx build --platform linux/arm64 -f Dockerfile -t ghcr.io/${{ github.actor }}/<빌드하고자 하는 환경 이름>:latest --push .
  ```

- GitHub Actions Runner 설정
  GitHub Actions Runner를 설정하여 Docker 컨테이너와 호환되는 Linux 환경에서 프로젝트를 실행합니다. ARM64 아키텍처를 선택하여 다양한 환경에서 동작하도록 합니다.

- 실행 및 배경 실행
  GitHub Actions Runner를 배경에서 실행하도록 설정하여 지속적으로 프로젝트의 상태를 모니터링합니다.
  ```bash
  ./run.sh
  nohup ./run.sh > run.log 2>&1 &
  ```

- Docker Compose 설정
  프로젝트의 복잡성을 관리하기 위해 Docker Compose를 사용하여 Django 애플리케이션과 필수 백엔드 서비스를 구성합니다.

  ```yaml
  version: '3'
  services:
    django:
      container_name: django
      image: ghcr.io/${GITHUB_ACTOR}/tf-django-server:latest
      command: /app/wait-for-it.sh db:3306 -t 15 -- sh -c "python manage.py migrate && python manage.py runserver 0.0.0.0:8000"
      restart: always
      ports:
        - "8000:8000"
      depends_on:
        - db
        - redis
      environment:
        - DJANGO_SETTINGS_MODULE=config.settings
        # 환경 변수들
      networks:
        - app-network
  
    # 다른 서비스들
  networks:
    app-network:
      driver: bridge
  ```

<br><br><br>

# 10. Result (수행 결과)

**사이트 화면**
![image](https://github.com/user-attachments/assets/59c1f86d-b49f-4abe-aaf3-9c2b8a934d6f)
![image](https://github.com/user-attachments/assets/7cebbc41-d857-40f0-91b3-03a5564e7fd6)
![image](https://github.com/user-attachments/assets/77fe7200-c15c-4e1f-acc0-c67adb8b4e6e)
![image](https://github.com/user-attachments/assets/33070908-7837-488f-945e-887606ea4734)
![image](https://github.com/user-attachments/assets/8bbaab13-781f-4f1f-8f81-6fdbc901fe75)


**회원 예측**

<br><br><br>

# 11. Tech Stack (기술 스택)
<div align=left><h3>🕹️ Frontend</div>
<div align=left>
  <img src="https://img.shields.io/badge/Vue.js-4FC08D?style=for-the-badge&logo=Vue.js&logoColor=white">
  <img src="https://img.shields.io/badge/Vuetify-1867C0?style=for-the-badge&logo=Vuetify&logoColor=white">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=JavaScript&logoColor=white">
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=TypeScript&logoColor=white">
  <img src="https://img.shields.io/badge/D3.js-F9A03C?style=for-the-badge&logo=D3.js&logoColor=white">
  <img src="https://img.shields.io/badge/Axios-5A29E4?style=for-the-badge&logo=Axios&logoColor=white">
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=CSS3&logoColor=white">
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=HTML5&logoColor=white">
</div>

<div align=left><h3>🕹️ Backend</div>
<div aling=left>
  <img src="https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=Django&logoColor=white">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=Python&logoColor=white">
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=Pandas&logoColor=white">
  <img src="https://img.shields.io/badge/Redis-FF4438?style=for-the-badge&logo=Redis&logoColor=white">
  <img src="https://img.shields.io/badge/KakaoDev-221E68?style=for-the-badge&logo=Kakao&logoColor=white">
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=FastAPI&logoColor=white">
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=MySQL&logoColor=white">
</div>

<div align=left><h3>🕹️ AI Core</div>
<div align=left>
  <img src="https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=OpenAI&logoColor=white">
  <img src="https://img.shields.io/badge/Transformer-131622?style=for-the-badge&logo=Transformer&logoColor=white">
  <img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=TensorFlow&logoColor=white">
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=Pandas&logoColor=white">
  <img src="https://img.shields.io/badge/Numpy-013243?style=for-the-badge&logo=Numpy&logoColor=white">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=Python&logoColor=white">
</div>

<div align=left><h3>🕹️ Deploy & Infra</div>
<div align="left">
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=Docker&logoColor=white">
  <img src="https://img.shields.io/badge/GitHub Runner-2088FF?style=for-the-badge&logo=GitHub Runner&logoColor=white">
  <img src="https://img.shields.io/badge/GitHub Actions-2088FF?style=for-the-badge&logo=GitHub Actions&logoColor=white">
  <img src="https://img.shields.io/badge/Amazon Web Services-232F3E?style=for-the-badge&logo=Amazon Web Services&logoColor=white">
  <img src="https://img.shields.io/badge/NGINX-009639?style=for-the-badge&logo=NGINX&logoColor=white">
</div>

<div align=left><h3>🕹️ Dev Tool </div>
<div align="left">
  <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=GitHub&logoColor=white">
  <img src="https://img.shields.io/badge/Slack-4A154B?style=for-the-badge&logo=Slack&logoColor=white">
  <img src="https://img.shields.io/badge/Visual Studio Code-008CFF?style=for-the-badge&logo=Visual Studio Code&logoColor=white">
  <img src="https://img.shields.io/badge/Notion-000000?style=for-the-badge&logo=Notion&logoColor=white">
  <img src="https://img.shields.io/badge/Pycharm-000000?style=for-the-badge&logo=Pycharm&logoColor=white">
  <img src="https://img.shields.io/badge/git-F05032?style=for-the-badge&logo=git&logoColor=white">
</div>

                                                                                                       
<br><br><br>

# 12. Deploy Issue (배포 이슈)
- **FastAPI 수동 배포 중 Docker Image 오류**
  ![image](https://github.com/user-attachments/assets/aacbbebb-578a-4baf-94a9-1de2f7199b89)
  - **오류** : "Error response from daemon: mainfest unknown"
  - **오류 원인** : 진행할 Docker Image가 없거나 사용이 불가한 상황
  - **오류 해결** : Docker Build 과정에서 사용한 Github 계정은 Login할 때도 동일하게 사용
    - Docker Build를 진행하는 프로젝트에서도 Docker Login <br>
      ```bash
      echo "GHCR토큰" | docker login ghcr.io -u 계정 --password-stdin
      ```
    - AWS 접속 후 docker-compose.yml 파일 구동 시에도 Docker Login <br>
      ```bash
      echo "GHCR토큰" | docker login ghcr.io -u 계정 --password-stdin
      ```
    - .env로 관리하는 정보에 Github 계정은 docker build 구성할 때 사용한 계정


<br><br><br>

# 13. 테스트 보고서 (CI 테스트 결과)
<table align="center">
  <tbody>
    <tr>
      <td align="center"><b>Frontend</b></td>
      <td align="center"><b>Backend</b></td>
      <td align="center"><b>FastAPI</b></td>
    </tr>
    <tr>
      <td><img src="https://github.com/user-attachments/assets/4b2b88ff-7832-4bf1-9733-dea2ea70a4a0"/></td>
      <td><img src="https://github.com/user-attachments/assets/dbc03d11-ea42-4556-8793-0a2628a2964c"/></td>
      <td><img src="https://github.com/user-attachments/assets/e0b19c9b-31e6-429a-8668-fc1d7d605854"/></td>
    </tr>
  </tbody>
</table>

<br><br><br>

# 14. 한 줄 회고
### 🌊 이경민

### 😈 임영훈

### 🌋 정의헌



