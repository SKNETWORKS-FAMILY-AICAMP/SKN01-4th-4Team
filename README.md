# SKN01-4th-4Team

> **LLM을 활용한 챗봇 서비스 개발**
>
 → Vue + Django + FastAPI + Deep Learning Local Server 서비스

<br><br>


# 1. Introduction Team (팀 소개)

1. **팀명 : 🧑🏻‍🌾 TextFarmers(TF)**
2. 2. **구성원**
<table align="center">
  <tbody>
    <tr>
      <td align="center">
        <div>
          <img src="https://github.com/user-attachments/assets/c7df2eb9-d897-4acc-87a9-3cdbca2863a6"width="100px;"height="100px;"" alt=""/>
          <a href="https://github.com/2kilometer"><div align=center>팀장 이경민</div></a>
        </div>
      </td>
      <td align="center">
        <div>
          <img src="https://github.com/user-attachments/assets/7cbbcc77-39de-4dc6-be12-a2879ce15a0b"width="100px;"height="100px;" alt=""/>
          <a href="https://github.com/yhoon3002"><div align=center>임영훈</div></a>
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
<br>
    
3. **팀 문화**
    - **Agile Board** (with Notion)
        
        -서버별 별도의 애자일 보드 작성 및 관리

        -Task 달성률 77% (20/26 개)

        ![image](https://github.com/user-attachments/assets/9c605fb3-7a42-470a-a416-3cea43e8828d)

        🌈 ***애자일 보드를 사용하는 이유***
        ```
        과거 정의서들을 일일히 작성하였지만 빠른 속도로 무언가를 개발하는데 한계가 있습니다.
        처음부터 많은 것들을 빌드업하면서 빠른 생산성을 기반으로 움직이려면 반드시 애자일해야합니다.
        고로 폭포수 설계 방식이 아닌 애자일 프로세스 방식으로 애자일 보드를 작성하면서 진행했습니다.
        
        애자일 보드는 자체적으로 제목이 요구 사항을 내포하며 각 카드 내부에는 정의한 Domain의 세부 사항이 기록됩니다.
        고로 빠르게 팀원들과 협업 할 수 있고 소통 비용을 최소화시킬 수 있습니다.
        작은 것 같지만 이와 같은 것들이 쌓여서 아주 기민하고 민첩한 조직을 만들어 냅니다.
        ```
      
                    
    - **Weekly Review** (with Notion)
        
        -매주 회고를 진행하며, 진행사항/이슈사항/차주계획를 공유

        ![image](https://github.com/user-attachments/assets/bc82d25e-cc31-4951-b2cb-df1e60aeac6f)


    - **Issue Handling** (with Discord)

        -Discord의 Issue채널에 이슈사항 실시간 공유
        
        -Github와 Discord 연동으로 Git 커밋 및 PR 실시간 확인 가능

        ![image](https://github.com/user-attachments/assets/48eae561-bf55-4c80-b4d3-58b6120b062f)

        

      

<br><br>

# 2. Introduction Project (프로젝트 개요)

1. **서비스명** : TextFarmers
2. **서비스 소개** 

    - 의료 정보 제공 챗봇 서비스
    
    - 성격유형검사(MBTI) T형과 F형 응답을 선택, 이로 인해 심리적 안정감 제공


    
3. **기획 배경**

    - problem
    
        외부 요인(의사 파업, 팬데믹 상황, 정책 변화 등)으로 인한 보건 및 의료의 접근에 예상치 못한 불확실성 존재

        ![image](https://github.com/user-attachments/assets/7e8e6655-ef8e-47b0-a836-afbee9a00fa9)

    - solution

        **의료 데이터와 LLM을 사용**하여 의료 정보의 접근성을 높이는 사용자 친화적인 챗봇 서비스를 개발

<br><br>

# 3. 서비스 구성도
### Tech Stack (기술 스택)
<div align=left><h3>🕹️ Frontend</div>
<div align=left>
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=HTML5&logoColor=white">
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=CSS3&logoColor=white">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=JavaScript&logoColor=white">
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=TypeScript&logoColor=white">
  <img src="https://img.shields.io/badge/Vue.js-4FC08D?style=for-the-badge&logo=Vue.js&logoColor=white">
  <img src="https://img.shields.io/badge/Vuetify-1867C0?style=for-the-badge&logo=Vuetify&logoColor=white">
  <img src="https://img.shields.io/badge/GreenSock-88CE02?style=for-the-badge&logo=GreenSock&logoColor=white">
  <img src="https://img.shields.io/badge/Axios-5A29E4?style=for-the-badge&logo=Axios&logoColor=white">
  <img src="https://img.shields.io/badge/ESLint-4B32C3?style=for-the-badge&logo=ESLint&logoColor=white">
</div>

<div align=left><h3>🕹️ Backend</div>
<div aling=left>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=Python&logoColor=white">
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=Pandas&logoColor=white">
  <img src="https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=Django&logoColor=white">
  <img src="https://img.shields.io/badge/Redis-FF4438?style=for-the-badge&logo=Redis&logoColor=white">
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=FastAPI&logoColor=white">
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=MySQL&logoColor=white">
  <img src="https://img.shields.io/badge/KakaoDev-221E68?style=for-the-badge&logo=Kakao&logoColor=white">
</div>

<div align=left><h3>🕹️ AI Core</div>
<div align=left>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=Python&logoColor=white">
  <img src="https://img.shields.io/badge/Numpy-013243?style=for-the-badge&logo=Numpy&logoColor=white">
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=Pandas&logoColor=white">
  <img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=TensorFlow&logoColor=white">
  <img src="https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=OpenAI&logoColor=white">
  <img src="https://img.shields.io/badge/Transformer-131622?style=for-the-badge&logo=Transformer&logoColor=white">
</div>

<div align=left><h3>🕹️ Deploy & Infra</div>
<div align="left">
  <img src="https://img.shields.io/badge/GitHub Runner-2088FF?style=for-the-badge&logo=GitHub Runner&logoColor=white">
  <img src="https://img.shields.io/badge/GitHub Actions-2088FF?style=for-the-badge&logo=GitHub Actions&logoColor=white">
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=Docker&logoColor=white">
  <img src="https://img.shields.io/badge/NGINX-009639?style=for-the-badge&logo=NGINX&logoColor=white">
  <img src="https://img.shields.io/badge/Amazon Web Services-232F3E?style=for-the-badge&logo=Amazon Web Services&logoColor=white">
  <img src="https://img.shields.io/badge/Amazon Route 53-8C4FFF?style=for-the-badge&logo=Amazon Route 53&logoColor=white">
</div>

<div align=left><h3>🕹️ Dev Tool </div>
<div align="left">
  <img src="https://img.shields.io/badge/git-F05032?style=for-the-badge&logo=git&logoColor=white">
  <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=GitHub&logoColor=white">
  <img src="https://img.shields.io/badge/Visual Studio Code-008CFF?style=for-the-badge&logo=Visual Studio Code&logoColor=white">
  <img src="https://img.shields.io/badge/Pycharm-000000?style=for-the-badge&logo=Pycharm&logoColor=white">
  <img src="https://img.shields.io/badge/DBeaver-382923?style=for-the-badge&logo=DBeaver&logoColor=white">
  <img src="https://img.shields.io/badge/Discord-5865F2?style=for-the-badge&logo=Discord&logoColor=white">
  <img src="https://img.shields.io/badge/Notion-000000?style=for-the-badge&logo=Notion&logoColor=white">
  <img src="https://img.shields.io/badge/Slack-4A154B?style=for-the-badge&logo=Slack&logoColor=white">
</div>                                                                                             
<br><br>

### SEVER

![image](https://github.com/user-attachments/assets/5b283aa6-00e6-4787-9aad-de12cca01779)

- **AWS - HTTP 통신**
  
   - Backend (Django)
     
     - 사용자 인증 및 관리
     - redis와 MySQL에 사용자 정보 저장
       
   - Frontend (Vue)
   - FastAPI

      - 모델 서빙

- **Local - Socket 통신**

  - Deep Learning Local Server

    - 클라우드 비용 절감을 위해 LLM 로컬 서버 사용
    - TLS/SSL 보안
    - Embedding vector 저장을 위해, MongoDB 사용

<br><br>

### DEPLOY
![image](https://github.com/user-attachments/assets/aad179a6-5590-4bdb-9809-c0ff3a409866)

- **AWS EC2**
  
   - Vue/Django/FastAPI 서버 모두 하나의 EC2 인스턴스에 통합하여 배포

- **Docker & Docker-compose**
  
   - 컨테이너화하여 독립적이고 쉽게 관리

- **npm**
  
   - npm run build로 정적 파일 빌드

- **Github Actions**
  
   - CI/CD 파이프라인을 통해 자동 배포 시도
   - Github 보안 공격으로 Actions 실행되지 않아, 최종은 수동 build로 진행

- **NGINX**
  
   - 도메인 연결 및 웹 서버
   - 도메인 (http://transfarmers.kr)
 
<br><br>   

### ERD 구성
![image](https://github.com/user-attachments/assets/cb79aba5-ca4c-4cdd-88ec-a622608aba62)
<br><br>


<br><br>

# 4. ChatBot Service
## 📍 Ai-Client
### 사용자의 질문 의도 파악 모델 학습
- OpenAI API의 "gpt-3.5-turbo"모델에 프롬프트 엔지니어링을 통한 구현</br>
-> 분당 요청수 제한으로 인해 불가능</br>
- BioBERT, KoBERT 모델 사용</br>
-> 정확도가 너무 낮아 사용이 불가능</br>
- 최종적으로 BERT 모델의 다국적 버전을 사용함.</br>
**Accuracy**: 0.9724</br>
**Precision**: 0.9725</br>
**Recall**: 0.9724</br>
**F1 Score**: 0.9724</br>
97%의 정확도로 프로젝트에 사용하기로 결정

<br>

### 사용자의 질문 & 답변 데이터를 임베딩하고 유사도 비교
- 단어의 빈도를 기준으로 벡터화시키고 cosine유사도 비교</br>
-> 단어의 시제와 조사등이 완전히 동일해야 유사도가 있다고 판단하여 정확도가 떨어짐.</br>
- 형태소를 분석하고 어간을 추출하여 벡터화시키고 cosine유사도 비교</br>
-> 정확도가 조금은 상승했지만 여전히 문장의 문맥을 이해하지 못하고 단순히 같은 단어의 존재유무만으로 유사도를 비교</br>
- BioBERT모델을 사용하여 임베딩</br>
-> 라이브러리 충돌이슈와 임베딩에 소요되는 시간이 너무 길어 사용하기 어려움</br>
- OpenAI API을 이용한 임베딩 및 faiss를 통한 유사도 비교</br>
-> 문맥을 이해하는 고차원 벡터로 임베딩이 가능하고 대규모의 고차원 벡터 데이터셋에 유리한 faiss를 사용해 정확도 상승</br>

<br>

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
![image](https://github.com/user-attachments/assets/09752406-7ce2-491d-a00d-afc953464905)


<br><br>

# 5. Result (수행 결과)

**메인 화면**
<br>
<br>
![image](https://github.com/user-attachments/assets/59c1f86d-b49f-4abe-aaf3-9c2b8a934d6f)
![image](https://github.com/user-attachments/assets/7cebbc41-d857-40f0-91b3-03a5564e7fd6)
![image](https://github.com/user-attachments/assets/77fe7200-c15c-4e1f-acc0-c67adb8b4e6e)
<br>
<br>
**로그인 및 회원가입 화면**
<br>
<br>
![image](https://github.com/user-attachments/assets/33070908-7837-488f-945e-887606ea4734)
<br>
<br>
**채팅 화면**
<br>
<br>
![image](https://github.com/user-attachments/assets/6734c5a0-2e66-4818-99ce-ff31ee404cd1)
![image](https://github.com/user-attachments/assets/8bbaab13-781f-4f1f-8f81-6fdbc901fe75)
<br><br>


# 6. 한 줄 회고
### 🌊 이경민
배포와 인프라 설계를 진행하면서, 통합된 시스템의 복잡성을 이해하고 관리하는 것이 중요하다는 것을 경험함</br>
Github Actions가 다운, 외부 보안 공격 등 예기치 못한 이슈사항들이 발생하여 개발과정에서의 어려웠던 적이 많았지만, 이를 통해 예기치 못한 장애에 대한 부분도 고려 요소라는 것을 몸소 느낄 수 있었음</br>
이슈의 혼란 속에서 openAI 프롬프트 엔지니어링을 하면서 조건/기법/패턴에 따라 달라지는 답변을 보며 재미있었음

### 🌋 정의헌
구현하고자 하는 기능(채팅 데이터 저장, 구독권 판매 등)이 많았으나, 시간관계상 하지못한 기능들이 많아 아쉬움.</br>
데이터 양이 많은 만큼 정확도 높은 챗봇을 만들고 싶었지만,</br>
질문과 답변이 1:1 매칭이 되지않는 이슈로 TF-IDF 방식으로 대체하여 만족스러운 결과를 만들지는 못함.</br>
사용자의 질문의도를 파악하고 문체를 변환하는 등의 기능을 파인튜닝과 프롬프트 엔지니어링을 통해 구현한 부분은 재미있었고 만족스러움.

### 😈 임영훈

