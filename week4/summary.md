# Week 4 Summary
 너무 늦어져 죄송합니다.
 간단히 챕터의 내용들을 summary 하고 의견을 나누는 시간으로 진행하겠습니다.
  
  # 1. 웨어러블
  
    사례
 
     - MIT의 슈퍼슈즈
        신발내부의 IoT Sensor를 활용해 건강 정보를 측정하고 길안내를 가능하게함
     - 당뇨측정 장치
        웨어러블 디바이스를 통해 연속적으로 포도당 수치를 측정
     - 심장관찰
        심박수 측정을 통해 심부정맥등의 측정이 가능 (UCI Machine learning data set 오픈되어 있음)
     - 디지털 비서
        시리, 알렉사, 코타나 등을 이용한 일정관리
     
  # 2. 스마트 홈 & 사물 인터넷
  
    정보 수집 방법
    
     - 인간활동인식 (HAR Human Activity Recognition)
        인간의 행동을 인식하여 헬스, 피트니스, 요양병원, 재활센터 등에 이용
        레이터, 라이다, 카메라, 모션센서, 웨어러블 디바이스 등의 things 들을 통해 정보를 습득        
        핏빗 : 센서 감지를 통해 특정한 움직임으로 활동을 인식 (걷기, 달리기, 에어로빅 등)
        애플워치 : 넘어짐 감지를 통해 자동으로 응급전화를 연결
        영상의 HAR : 영상 분석을 통하여 사람의 특정행동들을 감지한다.
        스마트 라이팅 : 응급상황 발생 시 비상구 표시등을 이용하여 출구를 안내한다.
        홈서베일런스 : 가정내 보안을 위해 제공되는 서비스로 연결되어 있는 things 뜰간의 
        상호 작용을 통해 보다 높은 수준의 서비스가 가능하다
        
        데이터의 수집이 어려운 스마트 홈의 데이터 습득에 중요한 요소임.
        궁극적인 목적 : HAR을 통해 학습한 내용 및 장치들을 통해 수집된 데이터를 바탕으로 
        홈에서의 사용자의 상태를 인지하고 만족을 줄 수 있는 서비스를 제공해 준다.
 
 # 3. 스마트 시티
  
    스마트 시티란
     - 정보 통신 기술을 사용해 자원소비 혹은 총 비용을 감소가능할 수 있도록 도시 서비스의 품질과 성능을 높이는 것을 목적으로 갖는 도시
     - 세계 인구의 증가 추세로 인하여 인구 1000만 이상의 도시들이 급속도로 증가하고 있는 추세이다.
     
    정의 
     - 기반시설에 광범위한 전자 & 디지털 기술을 사용한다.
     - ICT(정보통신기술)을 이용하여 생활환경과 근무환경을 변화시킨다.
     - 정부 시스템에 ICT 기술을 접목한다.
     - 사람과 ICT 기술을 조합하는 관행을 정착시키고 이에 따른 정책을 시행한다.
     
    구성요소
     - 스마트 트래픽
     - 스카트 파킹
     - 스마트 웨이스트
     - 스마트 폴리싱
     - 스마트 라이팅
     - 스마트 거버넌스
     
    스마트 시티구성에 필요한 사물인터넷 기술
     - smart things sensor, camera, actuator network (COMMAX)
     - Field GateWay (things data to cloud) (COMMAX)
     - Stremming data processor (Dongobi)
     - Data Lake (Dongobi)
     - Data Warehouse (Dongobi)
     - Dashboard (Dongobi)
     - A.I. Algorithm (Together)
     - things control application (Dongobi)
     - User Application (Together)
     - Security (Dongobi)
    
# 4. 스마트 홈 서비스의 문제점  

   - 높은 소유비용 : 스마트 홈을 구성하기까지 비용이 비싸다
- 유연하지 못한 연결성 : 호환 되는 장비들을 구성하기 어렵다.
- 관리 : 전체 시스템을 관리하는데 전문성들이 필요하다
- 보안 : 신뢰할 만한 수준의 보안을 제공해주지 않는다.         
 참고 문헌 : https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/HomeOSCHI_cameraready_Final.pdf    

오래 전에 작성된 논문으로 현재의 상황을 반영해주는데는 다소 무리가 있다 하겠지만
이 내용이 시사해주는 점이 있다.
위의 문제들 중 지금 작성하고 있는 포켓의 장단점을 토의 하고 개선점을 도출해보자.

- 현재 기술만으로는 스마트홈과 AI의 접목은 시너지가 크지 않다
- 새로 개발될 기술, 센서, 로봇 등의 조합이 중요하다
- 스마트 홈의 수집 데이터는 주거환경 생활패턴에 따라 크게 달라진다.
- HAR(Human Activity Recognition)의 역할이 커질 수록 관련 법령들에 대한 개선도 함께 진행되어야 한다.

Key Pointers for any Smart Home System
- Data security and privacy (데이터 보안 및 개인정보 보호)
- Proper integration of AI and IoT (AI 기술의 IoT 로의 통합)
- Interoperability (상호 운용성)
- Better customer support (고객에 대한 더 나은 대응)
- Integration with voice controls (음성 제어 통합)
[출처 : https://qualetics.com/how-ai-iot-is-driving-intelligence-automation-in-smart-homes/]
    

# 5. 산업용 사물인터넷은 첨부파일로 대체
[kr_insights_deloitte-korea-review-10_11.pdf](https://github.com/sjh8543/dongobi-iotseminar/files/6751380/kr_insights_deloitte-korea-review-10_11.pdf)
