import streamlit as st
import random

# 페이지 제목
st.title("🌿 스마트팜 작물 환경 제어 시스템")

# 습도와 온도 랜덤 생성
x = random.randint(1, 100)
y = random.randint(1, 40)

# 현재 환경 출력
st.header("현재 환경")
st.write("습도💧:", f"{x}%", " / 온도🌡️:", f"{y}°C")

# 작물 입력 받기
crop = st.text_input("재배할 작물 이름을 입력하세요 (예: 토마토, 딸기)", "")

# 제어 함수 정의
def control_tomato(humidity, temp):
    if humidity < 78.1:
        st.write("💧 가습기 작동")
    if temp < 23.4:
        st.write("🔥 히터 작동")
    if temp > 26.5:
        st.write("❄️ 에어컨 작동")
    if humidity > 78.1 and 23.4 < temp < 26.5:
        st.success("✅ 최적의 상태입니다.")

def control_strawberry(humidity, temp):
    if humidity < 63.8:
        st.write("💧 가습기 작동")
    if temp < 22.1:
        st.write("🔥 히터 작동")
    if temp > 27.6:
        st.write("❄️ 에어컨 작동")
    if humidity > 63.8 and 22.1 < temp < 27.6:
        st.success("✅ 최적의 상태입니다.")

# 결과 출력
if crop:
    st.header("제어 결과")
    if crop == "토마토":
        control_tomato(x, y)
    elif crop == "딸기":
        control_strawberry(x, y)
    else:
        st.warning("🤷‍♂️ 지원하지 않는 작물입니다.")

