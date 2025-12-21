<div align="center">

# 🤖 Glaisser

### GLaDOS Artificial Intelligence Security Robot

*Portal의 GLaDOS를 모티브로 한 학교 경비 로봇 시스템*

![CSS](https://img.shields.io/badge/CSS-26.4%25-1572B6?style=flat&logo=css3&logoColor=white)
![EJS](https://img.shields.io/badge/EJS-18.7%25-B4CA65?style=flat)
![SCSS](https://img.shields.io/badge/SCSS-17.1%25-CC6699?style=flat&logo=sass&logoColor=white)
![C++](https://img.shields.io/badge/C++-16.2%25-00599C?style=flat&logo=cplusplus&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-15%25-F7DF1E?style=flat&logo=javascript&logoColor=black)
![Python](https://img.shields.io/badge/Python-6.6%25-3776AB?style=flat&logo=python&logoColor=white)

![GitHub Stars](https://img.shields.io/github/stars/Deamonio/Glaisser?style=social)
![GitHub Forks](https://img.shields.io/github/forks/Deamonio/Glaisser?style=social)
![GitHub Issues](https://img.shields.io/github/issues/Deamonio/Glaisser)
![Topics](https://img.shields.io/badge/topics-14-blue)

**🏫 미래산업과학고등학교 메이커창작과 Geekble 프로젝트**

[English](#english) | [한국어](#korean)

---

### 🎥 Demo Video

[![Glaisser Demo Video](https://img.youtube.com/vi/lbPWybNbxP8/maxresdefault.jpg)](https://www.youtube.com/watch?v=lbPWybNbxP8)

**▶️ 클릭하여 전체 시연 영상 보기**

*학교 복도를 순찰하며 사람을 인식하는 경비 로봇 Glaisser*

---

### 📸 프로젝트 갤러리

<img src="https://github.com/hyun0810d/2023_Geekble_Project-Glaisser/assets/84117112/fdaa14c3-3bab-4185-89e1-f17258067645" alt="Glaisser Robot" width="600">

*실제 학교에서 경비 중인 Glaisser*

</div>

---

## 📋 목차

- [프로젝트 소개](#-프로젝트-소개)
- [주요 기능](#-주요-기능)
- [시스템 아키텍처](#-시스템-아키텍처)
- [기술 스택](#-기술-스택)
- [프로젝트 구조](#-프로젝트-구조)
- [설치 및 실행](#-설치-및-실행)
- [핵심 기술 구현](#-핵심-기술-구현)
- [프로젝트 성과](#-프로젝트-성과)
- [팀 소개](#-팀-소개)
- [라이선스](#-라이선스)

---

## 🎯 프로젝트 소개

**Glaisser**는 2023년 미래산업과학고등학교 메이커창작과에서 제작한 **AI 기반 학교 경비 로봇**입니다.  

Valve의 Portal 게임 시리즈에 등장하는 GLaDOS에서 영감을 받아 이름을 지었으며, 학교 건물을 자율 순찰하며 사람을 인식하고 웹을 통해 실시간으로 경비 상황을 모니터링할 수 있는 시스템입니다.  

### 💡 프로젝트 목표

- 🏫 **학교 경비 자동화**: 야간 및 주말 학교 건물 자동 순찰
- 👁️ **AI 사람 인식**:  Roboflow 기반 AI 모델로 정확한 사람 감지
- 🌐 **웹 기반 모니터링**: 실시간 경비 상황 확인 및 원격 제어
- 📊 **경비 기록 관리**: 과거 경비 이력 조회 및 데이터 분석

### 📅 개발 기간

**2023년 9월 ~ 2023년 10월** (약 2개월)

### 🌐 웹사이트

- **www. Glaisser.com** (현재 운영 종료)
- **www.po-glos.com** (현재 운영 종료)
- AWS EC2 호스팅으로 운영
- Google Analytics 분석 결과 **약 150~200명 방문**

---

## ✨ 주요 기능

### 1. 🤖 AI 기반 사람 인식

**Roboflow를 활용한 YOLOv5 모델**

```
카메라 입력 → AI 모델 추론 → 사람 감지 → 웹서버 전송 → 실시간 표시
```

**특징:**
- ✅ **커스텀 데이터셋**:  직접 촬영한 이미지 + Roboflow Public 데이터
- ✅ **어두운 환경 최적화**: 야간 순찰을 위한 저조도 데이터 포함
- ✅ **Bounding Box 라벨링**: 정확한 사람 영역 인식
- ✅ **실시간 감지**: 순찰 중 즉시 사람 감지 및 알림

**AI 모델 학습 과정:**
1. 데이터 수집 (학교 복도, 계단, 교실 등)
2. Roboflow에서 라벨링 (Bounding Box)
3. YOLOv5 모델 학습
4. 추론 최적화 및 Arduino 연동

---

### 2. 🌐 웹 기반 제어 및 모니터링

**실시간 경비 상황 웹 인터페이스**

| 기능 | 설명 |
|---|---|
| 🎥 **실시간 사진** | 로봇이 촬영한 사진을 반별로 웹에서 확인 |
| 📜 **History** | 과거 경비 기록 조회 (날짜, 시간, 위치, 감지 이미지) |
| 🎮 **원격 제어** | 웹에서 로봇 이동 방향 제어 |
| 📊 **통계** | 경비 데이터 분석 (시간대별 인원 수 등) |

**웹 기술 스택:**
- **Backend**: Node.js + Express. js
- **Template Engine**: EJS (18.7%)
- **Styling**: CSS (26.4%) + SCSS (17.1%)
- **Server**: AWS EC2
- **Domain**: 가비아 도메인 연결

---

### 3. 🚗 자율 주행 및 순찰

**학교 건물 자동 순찰 시스템**

```
[1층] → [2층] → [구름다리] → [다시 1층] (순환)
```

**Arduino 기반 모터 제어:**
- DC 모터 × 4 (바퀴 구동)
- 초음파 센서 (장애물 감지)
- 라인 트레이서 (경로 추적)
- Serial 통신 (Python 중간 매체와 연동)

---

### 4. 📡 Socket 통신 시스템

**3단계 통신 구조**

```
[웹 브라우저] ←→ [AWS 웹서버] ←→ [중간 매체(노트북)] ←→ [Arduino 로봇]
    (HTTP)         (Socket. io)        (PySerial)
```

**통신 방식:**
- **웹 ↔ 서버**: HTTP REST API
- **서버 ↔ 중간매체**: Socket.io (실시간 양방향)
- **중간매체 ↔ Arduino**: PySerial (Serial 통신)

**이미지 전송:**
- SCP (Secure Copy Protocol)로 이미지 파일 전송
- Polling 기술로 웹에서 실시간 업데이트

---

## 🏗️ 시스템 아키텍처

```
┌─────────────────────────────────────────────────┐
│  사용자 (웹 브라우저)                            │
│  • Chrome, Safari, Edge 등                      │
└─────────────────────────────────────────────────┘
                ↓ HTTP/WebSocket
┌─────────────────────────────────────────────────┐
│  AWS EC2 웹서버 (Node.js + Express)             │
│  • EJS 템플릿 렌더링                            │
│  • Socket.io 서버                               │
│  • 이미지 관리 (filesystem)                     │
│  • JSON 데이터 저장                             │
└─────────────────────────────────────────────────┘
                ↓ Socket.io
┌─────────────────────────────────────────────────┐
│  중간 매체 (노트북 - Python)                    │
│  • Socket 클라이언트                            │
│  • PySerial 통신                                │
│  • 명령 변환 (Web → Arduino)                    │
│  • 이미지 수신 및 SCP 전송                      │
└─────────────────────────────────────────────────┐
                ↓ Serial (PySerial)
┌─────────────────────────────────────────────────┐
│  Arduino 로봇 (C++)                             │
│  • 모터 제어 (4 DC Motors)                      │
│  • 초음파 센서 (장애물 감지)                    │
│  • 라인 트레이서                                │
│  • 카메라 모듈 (AI 추론용)                      │
└─────────────────────────────────────────────────┘
                ↓
┌─────────────────────────────────────────────────┐
│  AI 추론 (Python - YOLOv5)                      │
│  • Roboflow 학습 모델                           │
│  • 사람 감지 (Bounding Box)                     │
│  • 결과 이미지 생성                             │
└─────────────────────────────────────────────────┘
```

---

## 🛠️ 기술 스택

### Frontend (62.2%)

| Technology | Usage | Description |
|---|---|---|
| ![CSS](https://img.shields.io/badge/CSS-26.4%25-1572B6) | 26.4% | 웹 페이지 스타일링 |
| ![EJS](https://img.shields.io/badge/EJS-18.7%25-B4CA65) | 18.7% | 서버 사이드 템플릿 엔진 |
| ![SCSS](https://img.shields.io/badge/SCSS-17.1%25-CC6699) | 17.1% | CSS 전처리기 (변수, 믹스인) |

### Backend (37.8%)

| Technology | Usage | Description |
|---|---|---|
| ![C++](https://img.shields.io/badge/C++-16.2%25-00599C) | 16.2% | Arduino 펌웨어 (로봇 제어) |
| ![JavaScript](https://img.shields.io/badge/JavaScript-15%25-F7DF1E) | 15% | Node.js 웹서버 로직 |
| ![Python](https://img.shields.io/badge/Python-6.6%25-3776AB) | 6.6% | 중간 매체, AI 추론 |

### 주요 기술

**웹 서버:**
- **Node.js** + **Express. js**:  웹 프레임워크
- **EJS**: 동적 HTML 생성
- **Socket.io**: 실시간 양방향 통신
- **AWS EC2**: 클라우드 호스팅

**AI/ML:**
- **Roboflow**: 데이터 라벨링 및 관리
- **YOLOv5**: 객체 감지 모델
- **Python**: AI 추론 스크립트

**로봇 제어:**
- **Arduino**: 마이크로컨트롤러
- **C++**: 펌웨어 개발
- **PySerial**: Python ↔ Arduino 통신

**통신:**
- **Socket.io**: 웹 ↔ 중간매체
- **Serial**: 중간매체 ↔ Arduino
- **SCP**: 이미지 파일 전송

---

## 📁 프로젝트 구조

```
Glaisser/
├── 📂 Web/                          # 웹 서버 (Node.js + Express)
│   ├── 📄 app.js                    # 메인 서버 파일
│   ├── 📄 package.json              # 의존성 관리
│   ├── 📄 data.json                 # 경비 데이터 저장
│   ├── 📂 routes/                   # API 라우트
│   ├── 📂 views/                    # EJS 템플릿
│   │   ├── index.ejs                # 메인 페이지
│   │   ├── history.ejs              # 경비 기록 페이지
│   │   └── monitor.ejs              # 실시간 모니터링
│   ├── 📂 public/                   # 정적 파일
│   │   ├── 📂 css/                  # CSS 파일 (26.4%)
│   │   ├── 📂 scss/                 # SCSS 파일 (17.1%)
│   │   ├── 📂 js/                   # 클라이언트 JavaScript
│   │   └── 📂 images/               # 이미지 리소스
│   └── 📂 사진/                     # 로봇이 촬영한 사진 저장
│
├── 📂 Arduino_Glados Robot/         # Arduino 펌웨어 (C++ 16.2%)
│   ├── 📂 1층/                      # 1층 순찰 코드
│   ├── 📂 2층/                      # 2층 순찰 코드
│   ├── 📂 구름다리/                 # 구름다리 순찰 코드
│   ├── 📂 공통/                     # 공통 함수 및 라이브러리
│   └── 📂 홍보 전시/                # 전시용 데모 코드
│
├── 📂 middle_medium(client)/        # 중간 매체 (Python 6.6%)
│   ├── 📄 socket_client.py          # Socket. io 클라이언트
│   ├── 📄 serial_comm.py            # PySerial 통신
│   └── 📄 ai_inference.py           # AI 추론 스크립트
│
├── 📄 README.md                     # 프로젝트 설명
└── 📄 .gitignore
```

---

## 🚀 설치 및 실행

### 사전 요구사항

**소프트웨어:**
- ✅ Node.js 14.x 이상
- ✅ Python 3.7 이상
- ✅ Arduino IDE
- ✅ AWS 계정 (배포용)

**하드웨어:**
- 🤖 Arduino 보드 (Mega 또는 Uno)
- 🚗 DC 모터 × 4
- 📡 초음파 센서
- 📹 카메라 모듈
- 🔋 배터리
- 💻 중간 매체용 노트북

### 설치 단계

#### 1. 저장소 클론

```bash
git clone https://github.com/Deamonio/Glaisser.git
cd Glaisser
```

#### 2. 웹 서버 설정

```bash
cd Web
npm install
```

**package.json 의존성:**
```json
{
  "name": "glaisser-web",
  "version": "1.0.0",
  "dependencies": {
    "express": "^4.18.0",
    "ejs": "^3.1.0",
    "socket.io":  "^4.5.0",
    "body-parser": "^1.20.0"
  }
}
```

#### 3. Python 환경 설정

```bash
cd ../middle_medium(client)
pip install -r requirements.txt
```

**requirements.txt:**
```txt
pyserial>=3.5
python-socketio>=5.0.0
opencv-python>=4.6.0
# Roboflow / YOLOv5 의존성 추가
```

#### 4. Arduino 펌웨어 업로드

```bash
# Arduino IDE에서 열기
# Arduino_Glados Robot/공통/main. ino

# 보드 선택:  Arduino Mega
# 포트 선택
# 업로드
```

---

## 💻 실행 방법

### 1️⃣ 웹 서버 실행

```bash
cd Web
node app.js
```

**출력:**
```
[Glaisser] Web server starting... 
[Glaisser] Server running on port 3000
[Glaisser] Socket.io ready
```

### 2️⃣ 중간 매체 실행

```bash
cd middle_medium(client)
python socket_client. py
```

**출력:**
```
[Client] Connecting to server...
[Client] Connected to http://www.glaisser.com:3000
[Client] Serial port opened:  /dev/ttyUSB0
[Client] Ready to receive commands
```

### 3️⃣ 웹 브라우저 접속

```
http://localhost:3000
또는
http://www.glaisser.com:3000 (운영 중일 때)
```

---

## 🧠 핵심 기술 구현

### 1. Roboflow 기반 AI 사람 인식

**데이터셋 구축:**

```python
# 1. 데이터 수집
# - 학교 복도, 계단, 교실 등에서 직접 촬영
# - Roboflow Public 데이터셋 활용
# - 총 1000+ 이미지

# 2. 라벨링 (Roboflow)
# - Bounding Box로 사람 영역 표시
# - 클래스:  "person"
# - 어두운 환경 데이터 포함 (야간 경비 대비)

# 3. YOLOv5 학습
# Roboflow에서 자동 학습 또는
# Google Colab에서 커스텀 학습
```

**추론 코드:**

```python
# middle_medium(client)/ai_inference.py
import cv2
from roboflow import Roboflow

rf = Roboflow(api_key="YOUR_API_KEY")
project = rf.workspace().project("glaisser-person-detection")
model = project.version(1).model

def detect_person(image_path):
    """이미지에서 사람 감지"""
    result = model.predict(image_path, confidence=40).json()
    
    # 감지된 사람 수
    person_count = len(result['predictions'])
    
    # 결과 이미지 생성 (Bounding Box 표시)
    img = cv2.imread(image_path)
    for pred in result['predictions']:
        x1 = int(pred['x'] - pred['width']/2)
        y1 = int(pred['y'] - pred['height']/2)
        x2 = int(pred['x'] + pred['width']/2)
        y2 = int(pred['y'] + pred['height']/2)
        
        cv2.rectangle(img, (x1, y1), (x2, y2), (0, 255, 0), 2)
        cv2.putText(img, f"Person {pred['confidence']:.2f}", 
                    (x1, y1-10), cv2.FONT_HERSHEY_SIMPLEX, 
                    0.5, (0, 255, 0), 2)
    
    output_path = f"result_{image_path}"
    cv2.imwrite(output_path, img)
    
    return person_count, output_path
```

---

### 2. Socket.io 실시간 통신

**웹 서버 (Node.js):**

```javascript
// Web/app.js
const express = require('express');
const socketIO = require('socket.io');
const app = express();
const server = require('http').createServer(app);
const io = socketIO(server);

// EJS 템플릿 엔진 설정
app.set('view engine', 'ejs');
app.use(express.static('public'));

// Socket.io 연결
io.on('connection', (socket) => {
  console.log('[Server] 클라이언트 연결:', socket.id);
  
  // 로봇 제어 명령 수신
  socket. on('robot-control', (command) => {
    console.log('[Server] 명령 수신:', command);
    // 중간 매체로 전달
    socket.broadcast.emit('robot-command', command);
  });
  
  // 이미지 수신
  socket.on('image-upload', (data) => {
    const { classroom, image, timestamp } = data;
    // 이미지 저장 및 웹에 표시
    saveImage(classroom, image, timestamp);
    io.emit('new-image', { classroom, timestamp });
  });
});

server.listen(3000, () => {
  console.log('[Glaisser] Server running on port 3000');
});
```

**중간 매체 (Python):**

```python
# middle_medium(client)/socket_client.py
import socketio
import serial
import time

# Socket.io 클라이언트
sio = socketio.Client()

# Arduino Serial 연결
arduino = serial.Serial('/dev/ttyUSB0', 9600, timeout=1)

@sio.on('connect')
def on_connect():
    print('[Client] 서버 연결 성공')

@sio.on('robot-command')
def on_command(data):
    print(f'[Client] 명령 수신: {data}')
    # Arduino로 전송
    command = data['direction']  # 'forward', 'backward', 'left', 'right'
    arduino.write(f"{command}\n".encode())

# 서버 연결
sio.connect('http://www.glaisser.com:3000')

# 메인 루프
while True:
    # Arduino에서 데이터 수신 (예: 사진 촬영 완료 신호)
    if arduino.in_waiting:
        signal = arduino.readline().decode().strip()
        if signal == "PHOTO_TAKEN":
            # AI 추론
            person_count, result_image = detect_person('captured. jpg')
            # 서버로 전송
            sio.emit('image-upload', {
                'classroom': '1-1',
                'image': result_image,
                'person_count': person_count,
                'timestamp': time.time()
            })
    time.sleep(0.1)
```

---

### 3. Arduino 모터 제어

**C++ 펌웨어:**

```cpp
// Arduino_Glados Robot/공통/main. ino

// 모터 핀 정의
#define MOTOR_LEFT_FORWARD 2
#define MOTOR_LEFT_BACKWARD 3
#define MOTOR_RIGHT_FORWARD 4
#define MOTOR_RIGHT_BACKWARD 5

// 초음파 센서
#define TRIG_PIN 6
#define ECHO_PIN 7

void setup() {
  Serial.begin(9600);
  
  pinMode(MOTOR_LEFT_FORWARD, OUTPUT);
  pinMode(MOTOR_LEFT_BACKWARD, OUTPUT);
  pinMode(MOTOR_RIGHT_FORWARD, OUTPUT);
  pinMode(MOTOR_RIGHT_BACKWARD, OUTPUT);
  
  pinMode(TRIG_PIN, OUTPUT);
  pinMode(ECHO_PIN, INPUT);
}

void loop() {
  // Serial 명령 수신
  if (Serial.available()) {
    String command = Serial. readStringUntil('\n');
    executeCommand(command);
  }
  
  // 장애물 감지
  int distance = getDistance();
  if (distance < 20) {
    stopMotors();
    Serial.println("OBSTACLE_DETECTED");
  }
}

void executeCommand(String cmd) {
  if (cmd == "forward") {
    moveForward();
  } else if (cmd == "backward") {
    moveBackward();
  } else if (cmd == "left") {
    turnLeft();
  } else if (cmd == "right") {
    turnRight();
  } else if (cmd == "stop") {
    stopMotors();
  } else if (cmd == "photo") {
    // 사진 촬영 신호
    Serial.println("PHOTO_TAKEN");
  }
}

void moveForward() {
  digitalWrite(MOTOR_LEFT_FORWARD, HIGH);
  digitalWrite(MOTOR_LEFT_BACKWARD, LOW);
  digitalWrite(MOTOR_RIGHT_FORWARD, HIGH);
  digitalWrite(MOTOR_RIGHT_BACKWARD, LOW);
}

// ...  기타 모터 제어 함수
```

---

### 4. 동적 웹페이지 (EJS)

**메인 페이지:**

```html
<!-- Web/views/index.ejs -->
<!DOCTYPE html>
<html>
<head>
  <title>Glaisser - 학교 경비 로봇</title>
  <link rel="stylesheet" href="/css/style.css">
</head>
<body>
  <div class="container">
    <h1>🤖 Glaisser 실시간 모니터링</h1>
    
    <!-- 반별 실시간 사진 표시 -->
    <div class="classroom-grid">
      <% classrooms.forEach(function(classroom) { %>
        <div class="classroom-card" id="classroom-<%= classroom.id %>">
          <h3><%= classroom.name %></h3>
          <img src="/사진/<%= classroom.latestImage %>" alt="<%= classroom.name %>">
          <p>최근 감지: <%= classroom.personCount %>명</p>
          <p>시간: <%= classroom.timestamp %></p>
        </div>
      <% }); %>
    </div>
    
    <!-- 로봇 제어 -->
    <div class="control-panel">
      <h2>로봇 제어</h2>
      <button onclick="sendCommand('forward')">↑</button>
      <button onclick="sendCommand('left')">←</button>
      <button onclick="sendCommand('stop')">■</button>
      <button onclick="sendCommand('right')">→</button>
      <button onclick="sendCommand('backward')">↓</button>
    </div>
  </div>
  
  <script src="/socket.io/socket.io.js"></script>
  <script>
    const socket = io();
    
    // 새로운 이미지 수신
    socket.on('new-image', (data) => {
      const card = document.getElementById(`classroom-${data.classroom}`);
      // 이미지 업데이트 (Polling 기술)
      location.reload();
    });
    
    function sendCommand(direction) {
      socket.emit('robot-control', { direction });
    }
  </script>
</body>
</html>
```

---

## 🏆 프로젝트 성과

### ✅ 수상 및 인정

- 🎓 **미래산업과학고 메이커창작과 대표 작품 선정**
- 💡 **2023 Seoul Maker Fair 참가**
- 🔬 **Science Festival 전시**
- 🌟 **학교 공식 경비 시스템으로 사용** (기간 한정)

### 📊 운영 성과

- 👥 **웹사이트 방문자**:  약 150~200명 (Google Analytics)
- 🏫 **순찰 범위**: 1층, 2층, 구름다리 포함 전체 건물
- 📸 **총 촬영 이미지**: 1000+ 장
- ⏱️ **평균 순찰 시간**: 약 30분/회

### 💡 학습 성과

- 🌐 **첫 웹 개발 성공** (개인 - 김강현)
- 🤖 **AI 모델 학습 및 배포 경험**
- ☁️ **클라우드 서버 운영 경험** (AWS EC2)
- 🔌 **다양한 통신 프로토콜 구현** (Socket, Serial, SCP)

---

## 👥 팀 소개

**미래산업과학고 메이커창작과 5인 팀 × Geekble**

### 팀원

| 역할 | 이름 | 담당 |
|---|---|---|
| 👨‍💻 **AI & Web Dev** | 김강현 | AI 모델 학습, 웹 서버 개발, 전체 시스템 통합 |
| 👨‍🔧 **Leader & Electronic** | 조윤혁 | 팀 리더, 전자 회로 설계, Arduino 프로그래밍 |
| ⚡ **Electronic** | 송승현 | 모터 제어, 센서 통합 |
| 🔩 **Engineering** | 장한수 | 로봇 기구 설계 및 제작 |
| 🔨 **Engineering** | 김선우 | 로봇 조립 및 최적화 |

### 협력

- **Geekble 잭키**: 프로젝트 기획 및 멘토링
- **PD 모루**: 프로덕션 관리

---

## 🎥 미디어

### 유튜브 영상

- **제작 영상**: [https://youtu.be/JkVdGndak4U](https://youtu.be/JkVdGndak4U)
- **시연 영상**: [https://www.youtube.com/watch?v=lbPWybNbxP8](https://www.youtube.com/watch?v=lbPWybNbxP8)
- **업로드 날짜**: 2023년 11월 4일

### 전시 사진

<img src="https://github.com/hyun0810d/2023_Geekble_Project-Glaisser/assets/84117112/fdaa14c3-3bab-4185-89e1-f17258067645" width="600">

*Seoul Maker Fair 전시 현장*

---

## 📝 기술 상세

### 통신 방법 요약

| 구간 | 프로토콜 | 설명 |
|---|---|---|
| 웹 ↔ 서버 | HTTP, WebSocket | REST API, Socket.io |
| 서버 ↔ 중간매체 | Socket.io | 실시간 양방향 통신 |
| 중간매체 ↔ Arduino | Serial (PySerial) | 명령 전송 |
| 이미지 전송 | SCP | 파일 전송 |

### 이미지 관리

**Polling 기술:**
```javascript
// 클라이언트가 주기적으로 서버에 요청
setInterval(() => {
  fetch('/api/latest-images')
    .then(res => res.json())
    .then(data => {
      updateImages(data);
    });
}, 3000);  // 3초마다 갱신
```

**filesystem 라이브러리:**
```javascript
const fs = require('fs');

// 이미지 저장
function saveImage(classroom, imageData, timestamp) {
  const filename = `${classroom}_${timestamp}.jpg`;
  fs.writeFileSync(`./사진/${filename}`, imageData);
  
  // JSON에 기록
  const data = JSON.parse(fs.readFileSync('data.json'));
  data.images.push({ classroom, filename, timestamp });
  fs.writeFileSync('data.json', JSON.stringify(data));
}
```

---

## 📜 라이선스

이 프로젝트는 교육 목적으로 제작되었습니다.  

**참고**:  Portal 및 GLaDOS는 Valve Corporation의 상표입니다.  이 프로젝트는 팬메이드 프로젝트이며 Valve와 공식적으로 관련이 없습니다. 

---

## 📞 연락처

<div align="center">

### 프로젝트 관리자:   Deamonio (김강현)

![Email](https://img.shields.io/badge/Email-hyun0810d@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-Deamonio-181717?style=for-the-badge&logo=github&logoColor=white)

**프로젝트 링크**: [https://github.com/Deamonio/Glaisser](https://github.com/Deamonio/Glaisser)

</div>

---

## 🙏 감사의 말

이 프로젝트를 가능하게 해준 모든 분들께 감사드립니다. 

| Roboflow | Node.js | Arduino | AWS | Geekble |
|---|---|---|---|---|
| AI 플랫폼 | 웹 서버 | 하드웨어 | 클라우드 | 멘토링 |

특별히 **미래산업과학고 메이커창작과** 선생님들과 **Geekble 팀**에게 감사드립니다! 

---

<div align="center">

## ⭐ 이 프로젝트가 마음에 드셨다면 Star를 눌러주세요! 

[![Star History Chart](https://api.star-history.com/svg?repos=Deamonio/Glaisser&type=Date)](https://star-history.com/#Deamonio/Glaisser&Date)

---

**Made with ❤️ by 미래산업과학고 메이커창작과**

*"학교를 지키는 AI 경비 로봇, Glaisser"*

---

**© 2023 Deamonio & Team. All rights reserved.**

[⬆ 맨 위로 돌아가기](#-glaisser)

</div>

---

## 🌐 English Version

<div id="english">

### 🎯 About Glaisser

Glaisser is an AI-powered school security robot developed by the Maker Creation Department of Mirae Science High School in 2023, inspired by GLaDOS from Valve's Portal series.

### ✨ Key Features

- **AI Person Detection**: Roboflow-based YOLOv5 model
- **Web Monitoring**: Real-time surveillance via web interface
- **Autonomous Patrol**: Automatic school building patrol
- **History Tracking**: Past surveillance record management

### 🎥 Demo

- **Video**: [Watch on YouTube](https://www.youtube.com/watch?v=lbPWybNbxP8)
- **Website**: www.glaisser.com (Currently offline)

### 👥 Team

5-member team from Mirae Science High School Maker Creation Department

### 📅 Period

September 2023 ~ October 2023

### 🏆 Achievements

- ✅ Selected as representative work of the department
- ✅ Participated in 2023 Seoul Maker Fair
- ✅ 150~200 website visitors
- ✅ First successful web development project

[🔙 Back to Korean](#-목차)

</div>
