# Implementing an AI Voice-Activated Weather Information Device Using Raspberry Pi

음성 인식으로 "날씨"를 말하면 서울의 현재 기온과 습도를 한글 음성으로 출력하는 IoT 프로젝트입니다.

## 🎬 데모 영상

[![Demo Video](https://img.youtube.com/vi/ryhrrifhAaQ/0.jpg)](https://www.youtube.com/shorts/ryhrrifhAaQ)

## 📌 프로젝트 개요

- Google Speech Recognition API로 한국어 음성 인식
- OpenWeatherMap API로 서울 현재 기온·습도 수집
- espeak TTS로 "기온은 OO도 습도는 OO퍼센트 입니다" 한글 음성 출력

## 🛠️ 사용 기술

| 항목 | 내용 |
|---|---|
| Language | Python 3.12.10 |
| API | OpenWeatherMap, Google Speech Recognition |
| Library | speech_recognition, requests, os, time |
| TTS | espeak |
| Hardware | Raspberry Pi, 마이크, 스피커 |

## 📂 파일 구성

```
project_32/
├── main32.py       # 음성 인식 기본 동작 확인
├── main32-1.py     # 날씨 정보 음성 출력
└── main32-2.py     # 음성 인식 + 날씨 출력 통합 최종 코드
```

## 🚀 실행 방법

```bash
# 가상환경 활성화
cd myProjects/project_31
source 나의가상환경/bin/activate
cd ../project_32

# 음성 인식 기본 동작 확인
python main32.py

# 날씨 정보 음성 출력 확인
python main32-1.py

# 최종 통합 실행
python main32-2.py
```

## ⚙️ 사전 준비

```bash
# 패키지 설치
sudo apt-get install espeak -y
sudo apt install -y fonts-unfonts-core
sudo apt install -y fcitx5 fcitx5-hangul fcitx5-config-qt
```

- OpenWeatherMap API 키 발급 → https://openweathermap.org/
- `main32-1.py`, `main32-2.py` 코드 내 `API_KEY` 에 본인 API 키 입력 필요

## 📚 참고문헌

- [SpeechRecognition Library Documentation](https://pypi.org/project/SpeechRecognition/)
- [Google Cloud Speech-to-Text Documentation](https://cloud.google.com/speech-to-text/docs)
- [eSpeak Text to Speech](http://espeak.sourceforge.net/)
- [OpenWeatherMap Current Weather API](https://openweathermap.org/current)
