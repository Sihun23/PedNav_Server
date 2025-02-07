# 🚶 PedNav: 보행자 안전 네비게이션 시스템

PedNav는 보행자의 안전을 위해 **AI 기반 차량 감지 기술**을 활용하여 보행 중 사고 위험을 최소화하는 애플리케이션입니다. 스마트폰 마이크와 **Radar 센서**를 결합하여 차량 접근 여부를 실시간으로 감지하고, 사용자에게 **시각·진동·음성 알림**을 제공합니다.  

## 📌 프로젝트 개요
- **프로젝트명**: PedNav (Pedestrian Navigation)
- **개발 목적**: 보행자의 안전을 강화하고, 보행 중 사고 위험을 최소화하는 시스템 구축
- **핵심 기술**: 스마트폰 마이크 기반 음향 감지 + LiDAR 센서를 활용한 거리 측정
- **특징**: 온디바이스 AI 모델, 실시간 WebSocket 서버, 저지연(Low Latency) 차량 감지

---

## 🗂 프로젝트 구조
![프로젝트 구조](https://github.com/teamGachon/pednav_modelplusAPP/blob/main/Project%20Structure.png)

---

## 🔧 주요 기능
1. **차량 접근 감지**  
   - 스마트폰 마이크로 차량 소음을 분석해 차량 접근 여부 감지  
   - CNN 기반 AI 모델을 활용하여 차량 소리와 일반 소음을 구분  

2. **실시간 경고 시스템**  
   - 차량 감지 시 **진동·화면 점멸·음성 알림**을 통해 사용자에게 경고  
   - WebSocket을 활용한 실시간 데이터 송수신  

3. **보행자용 네비게이션**  
   - 네이버 지도 API를 활용한 보행자 경로 탐색 기능  
   - 사고 다발 지역 및 공사 구역 경고 기능 추가  

4. **사용자 맞춤 설정**  
   - GPS, 마이크, 백그라운드 실행 여부 등 설정 가능  
   - 노이즈캔슬링 사용자를 위한 최적화 모드 제공  

---

## 🔩 개발 환경

### **Back-end**
![SpringBoot](https://img.shields.io/badge/SpringBoot-%236DB33F.svg?style=for-the-badge&logo=springboot&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688.svg?style=for-the-badge&logo=fastapi&logoColor=white)
![WebSocket](https://img.shields.io/badge/WebSocket-0078D4?style=for-the-badge&logo=web&logoColor=white)

### **AI Model**
![TensorFlow](https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=for-the-badge&logo=tensorflow&logoColor=white)
![TensorFlow Lite](https://img.shields.io/badge/TensorFlow%20Lite-%23FF6F00.svg?style=for-the-badge&logo=tensorflow&logoColor=white)

### **Mobile App**
![Android Studio](https://img.shields.io/badge/Android%20Studio-3DDC84?style=for-the-badge&logo=androidstudio&logoColor=white)
![Kotlin](https://img.shields.io/badge/Kotlin-0095D5.svg?style=for-the-badge&logo=kotlin&logoColor=white)
![Java](https://img.shields.io/badge/Java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)

### **Database**
![MySQL](https://img.shields.io/badge/MySQL-4479A1.svg?style=for-the-badge&logo=mysql&logoColor=white)

### **Map & Navigation**
![Naver Maps API](https://img.shields.io/badge/Naver%20Maps%20API-03C75A.svg?style=for-the-badge&logo=naver&logoColor=white)


---

## 🏗 시스템 아키텍처
1. **온디바이스 AI 모델**  
   - 스마트폰에서 직접 AI 모델 실행 (TensorFlow Lite 활용)  
   - 평균 73ms의 낮은 레이턴시로 실시간 감지 수행  

2. **서버 기반 모델**  
   - WebSocket을 활용하여 오디오 데이터를 서버로 전송  
   - FastAPI 서버에서 AI 모델을 실행하여 감지 결과 반환  

3. **하이브리드 시스템**  
   - LiDAR 센서를 결합하여 거리 및 속도 감지 추가  
   - 온디바이스 + 서버 처리 방식을 최적화하여 배터리 소모 절감  

---

## ⏰ 개발 기간
- **2024.11.25 ~ 2024.12.01**: 아이디어 구상  
- **2024.12.02 ~ 2024.12.17**: 프로토타입 개발
- **2025.01.20 ~** : 2차 개발

---

## 📆 업데이트 계획
✔ **프로토타입 완료**  
✔ **정확도 향상**: 음향 AI 모델 개선 및 LiDAR 데이터 통합  
✔ **Radar 센서 추가**: 차량 감지 성능 향상  
✔ **배터리 최적화**: MEC (Mobile Edge Computing) 적용  
✔ **UI/UX 개선**: 사용자 피드백 반영  
✔ **지도 서비스 강화**: 사고 다발 지역 경고 기능 추가  

---

## 👨‍💻 개발자
| 이름 | 역할 |
|------|------|
| **장용근** | 프론트엔드 / UI 디자인 / Android |
| **양시훈** | 백엔드 / Android |
| **이한용** | AI 모델 / Android |
| **한수민** | 프론트엔드 |

---

## 📜 오픈소스 활용
- TensorFlow Lite (온디바이스 AI 모델)  
- FastAPI (백엔드 AI 서버)  
- Spring Boot (서버 및 WebSocket)  
- 네이버 지도 API (보행자 네비게이션)  

---
