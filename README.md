# opencv

#  OpenCV 간단 정리

> **OpenCV (Open Source Computer Vision Library)**  
> 오픈소스 컴퓨터 비전(Computer Vision) 및 머신러닝 라이브러리로,  
> 이미지 처리와 영상 분석을 쉽게 할 수 있게 도와주는 도구입니다.

---

##  OpenCV란?

| 항목 | 내용 |
|------|------|
| **이름** | OpenCV (Open Source Computer Vision) |
| **개발 언어** | C++ 기반, Python 등 여러 언어에서 사용 가능 |
| **용도** | 이미지/영상 처리, 얼굴 인식, 객체 탐지 등 |
| **라이선스** | 오픈소스 (BSD 라이선스) |
| **지원 플랫폼** | Windows, macOS, Linux, Android, iOS 등 |

---

##  OpenCV 설치하기 (Python)

```bash
pip install opencv-python
 pip install opencv-python-headless
GUI가 필요 없는 서버 환경에서는 위 명령어를 사용하세요.

 기본 예제
 이미지 불러오기 & 표시하기
python
코드 복사
import cv2

# 이미지 읽기
img = cv2.imread('image.jpg')

# 이미지 보여주기
cv2.imshow('My Image', img)
cv2.waitKey(0)
cv2.destroyAllWindows()
 이미지 회색조로 변환
python
코드 복사
import cv2

img = cv2.imread('image.jpg')
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)

cv2.imshow('Gray Image', gray)
cv2.waitKey(0)
cv2.destroyAllWindows()
 주요 기능 요약
기능	설명	주요 함수
이미지 읽기/쓰기	파일 입출력	cv2.imread(), cv2.imwrite()
영상 보기	창에 표시	cv2.imshow()
색상 변환	RGB ↔ Grayscale 등	cv2.cvtColor()
블러 처리	이미지 부드럽게 하기	cv2.GaussianBlur()
엣지 검출	윤곽선 찾기	cv2.Canny()
얼굴 인식	사람 얼굴 찾기	cv2.CascadeClassifier()
도형 그리기	선, 원, 사각형 등	cv2.line(), cv2.circle()
