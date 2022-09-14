# 🌳 RDCE(Reduce Digtal Carbon Emission) 소개 
지저분한 메일함 📨 !! 뭘 지워야 할지 감이 안 오시죠?  
RDCE를 통해 내가 어떤 주제에 관심 있는지, 나를 귀찮게 하는 메일은 누구인지, 지워야할 메일은 누구인지 알 수 있어요!!  
그리고 하나의 중요한 사실! 메일 한개당 발생하는 탄소의 양은 4g이라고 합니다. 메일이 하나둘씩 모이게 되면 어마어마한 탄소가 배출이 되겠죠?  
우리 모두 지구를 위한 메일 지우기를 시작으로 작은 실천을 합시다.  
🌳 RDCE를 통해 나의 메일을 분석하고 디지털 탄소 배출 절감을 실천해보세요 🌳 

## 필수 설정 - IMAP을 사용해주세요!

### Naver 
메일 왼쪽 아래의 환경설정 > POP3 / IMAP 설정 > IMAP / SMTP 설정 탭에서 IMAP/SMTP 사용 옵션을 사용함으로 설정, IMAP 동기화 설정 제한 5,000통으로 설정   
![image](https://user-images.githubusercontent.com/71928522/189707903-733f1250-fde3-420f-816d-9a567a146250.png)

### Google (Gmail)
오른쪽 상단에서 설정 설정 다음 모든 설정 보기 클릭 > 전달 및 POP/IMAP 탭 클릭 > 'IMAP 액세스' 섹션에서 IMAP 사용 선택 > 변경사항 저장 클릭 

### Daum
메일 왼쪽 아래의 환경설정 > IMAP/POP3 설정에서 사용 여부 설정

## 주요 기능
### 메일 분석
Text-mining을 통해 메일을 분석해요!  
+ 나에게 가장 메일을 많이 보내는 사람은??  
+ 메일함에서 읽은 메일은? 안읽은 메일은? 
+ 내 메일함의 주요 키워드는?
+ 삭제하면 좋을 메일들은?  
### 메일 삭제
(10월 중 개발 예정)
  
## 서비스 화면

## 시스템 구성 및 아키텍처
### Back-End & Front-End
![image](https://user-images.githubusercontent.com/71928522/189708430-c80fc4c0-7318-4f8c-baf9-f3963c5e67c4.png)

### Data-Analysis

### 데이터 전처리
>Imap서버에서 메일을 읽어온 후, DataFrame 생성 

![image](https://user-images.githubusercontent.com/71928522/190174833-44b99059-cba9-4650-8d32-fc3de91f96e2.png)

### LDA 적용
![image](https://user-images.githubusercontent.com/71928522/190174870-089e2a38-3181-49ae-a9c2-c3b13b93ba37.png)


### Naive Bayes 적용
> 사전에 준비된 데이터로 나이브베이즈 모델 생성

![image](https://user-images.githubusercontent.com/71928522/190174680-fab2601a-8a69-4857-ab54-f0c7483aae41.png)  


> 생성 모델에 사용자 데이터 적용, 결과 해석 후 삭제 추천 메일 추출

![image](https://user-images.githubusercontent.com/71928522/190174121-d38eb1d9-52c8-4e48-a702-c6147896d311.png)  

## 환경 설정
Python version : 3.9.13  

### Backend
패키지
```
  pip install fastapi
  pip install "uvicorn[standard]"
  ```
  
### mail analysis
패키지
```
pip install numpy
pip install pandas
pip install gensim
pip install sklearn
pip install konlpy
pip install openpyxl 
```
-- requirements.txt를 통해 다운 받을 수 있습니다!

## Team

#### Data-Analysis
> [김태영](https://github.com/kty4119)  
> [오재호](https://github.com/roaker)
#### Back-End & Front-End
> [손재성](https://github.com/noseaj)  
> [김민교](https://github.com/minkyokyo)
