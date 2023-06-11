# 제4회 2023 연구개발특구 AI SPARK 챌린지 - 공기압축기 이상 판단
## **최종결과: 4위 (353팀 참가)**
산업용 공기압축기의 이상 유무를 비지도학습 방식을 이용하여 판정
<br><br>

## 🎈 대회 주제 소개
■ 범천(주)은 ESG 가치를 담아 산업용 공기압축기를 개발하는 대덕연구개발특구 소재 기업입니다.

제4회 연구개발특구 AI SPARK 챌린지는 산업기기 피로도를 예측하는 문제입니다.<br>
산업용 공기압축기 및 회전기기에서 모터 및 심부 온도, 진동, 노이즈 등은 기기 피로도에 영향을 주는 요소이며, 피로도 증가는 장비가 고장에 이르는 원인이 됩니다.<br>
피로도 증가 시 데이터 학습을 통해 산업기기 이상 전조증상을 예측하여 기기 고장을 예방하고 그로 인한 사고를 예방하는 모델을 개발하는 것이 이번 대회의 목표입니다.
<br><br>

## 🎓모델 조건 (중요)
1. 본 대회의 모델링은 비지도학습 방식으로 진행됩니다.

2. 향후 실시간 판정에 활용될 수 있도록, 개발된 모델은 다음의 조건을 충족하여야 합니다.

- 입력된 데이터를 정상(0), 이상(1)로 구분하는 이진 분류 모델이어야 합니다.
- 시간 단위로 생성되는 입력 데이터에 대하여 판정을 수행할 수 있는 모델이어야 합니다.
- 신규 데이터로 학습/개선이 가능한 모델이어야 합니다.
- 총 8개의 대상 설비를 모델링하면서, 설비별로 별도의 모델을 학습하는 것은 허용되나 모두 동일한 아키텍처를 사용해야 합니다.<br>
(예: 설비 1에 사용한 모델 구조를 나머지 설비에도 사용하여야 함)
<br><br>

## 데이터 셋 설명
```
📁 dataset.zip
 ├--- 📃 train_data.csv     --- 학습용 데이터 파일 
 ├--- 📃 test_data.csv      --- 평가용 데이터 파일 
 └--- 📃 answer_sample.csv  --- 정답 양식 파일
 ```
- train_data: 학습용 데이터로 모두 정상 case로 이루어진 데이터입니다.<br>
- test_data: 평가용 데이터로 정상 case와 이상 case가 함께 포함되어 있는 데이터로, 예측 대상에 해당됩니다.<br>
- answer_sample: test_data에 대하여 작성할 제출용 레이블 파일 양식입니다.<br>
<br><br>

## 📈 데이터 구성
### 1. 데이터 구성 항목
- air_inflow: 공기 흡입 유량 (^3/min)
- air_end_temp: 공기 말단 온도 (°C)
- out_pressure: 토출 압력 (Mpa)
- motor_current: 모터 전류 (A)
- motor_rpm: 모터 회전수 (rpm)
- motor_temp: 모터 온도 (°C)
- motor_vibe: 모터 진동 (mm/s)
- type: 설비 번호

### 2. 설비별 특성
- 설비 번호 [0, 4, 5, 6, 7]: 30HP(마력)
- 설비 번호 1: 20HP
- 설비 번호 2: 10HP
- 설비 번호 3: 50HP
<br><br>

## 🧑‍🤝‍🧑 팀원 및 역할
<table>
  <tbody>
    <tr>
      <td align="center">
        <a href="https://github.com/jian1114">
          <img src="https://avatars.githubusercontent.com/u/77630266?v=4" width="100px;">  <br>
          <sub><b>이지안</b></sub>
        </a>
      </td>
      <td align="center">
        <a href="https://github.com/brojoon1">
          <img src="https://avatars.githubusercontent.com/u/81418195?v=4" width="100px;">  <br>
          <sub><b>김형준</b></sub>
        </a>
      </td>
      <td align="center">
        <a href="https://github.com/ayocado">
          <img src="https://avatars.githubusercontent.com/u/89889583?v=4" width="100px;">  <br>
          <sub><b>윤용완</b></sub>
        </a>
      </td>
      <td align="center">
        <a href="https://github.com/JunePark-00">
          <img src="https://avatars.githubusercontent.com/u/81201633?v=4" width="100px;">  <br>
          <sub><b>박주은</b></sub>
        </a>
      </td>
    </tr>
    <tr>
      <td align="center">팀장, 데이터분석, 모델링</td>
      <td align="center">데이터분석, 모델링</td>
      <td align="center">데이터분석, 모델링</td>
      <td align="center">데이터분석, 모델링</td>
    </tr>
  </tbody>
</table>

<br>

## 💻 기술 스택
<b> 언어 </b><br>
<span><img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=Python&logoColor=white"></span><br>

<b> 라이브러리 </b><br>
<span><img src="https://img.shields.io/badge/numpy-013243?style=for-the-badge&logo=numpy&logoColor=white"></span>
<span><img src="https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white"></span>

<b> 프로그래밍 인터페이스 </b><br>
<span><img src="https://img.shields.io/badge/jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white"></span><br>

<b> 협업툴 </b><br>
<span><img src="https://img.shields.io/badge/notion-000000?style=for-the-badge&logo=notion&logoColor=white"></span>
<span><img src="https://img.shields.io/badge/discord-5865F2?style=for-the-badge&logo=discord&logoColor=white"></span>


