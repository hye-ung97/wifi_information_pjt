# 📡 Wifi_information_PJT

서울시 공공와이파이 서비스 위치 정보 API 를 이용하여 내 위치 기반 공공 와이파이 정보를 제공하는 웹 서비스입니다. 

<div>
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=JavaScript&logoColor=white"/>
<img src="https://img.shields.io/badge/MariaDB_Foundation-1F305F?style=flat&logo=MariaDB&Foundation&logoColor=white"/>
<img src="https://img.shields.io/badge/Java-007396?style=flat&logo=Java&logoColor=white" />
<img src="https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=HTML5&logoColor=white" />
<img src="https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=CSS3&logoColor=white" />
</div>

<div>
<img src="https://img.shields.io/badge/IntelliJ_IDEA-000000?style=flat&logo=IntelliJIDEA&logoColor=white"/>
<img src="https://img.shields.io/badge/DataGrip-000000?style=flat&logo=DataGrip&Foundation&logoColor=white"/>
<img src="https://img.shields.io/badge/GitHub-181717?style=flat&logo=GitHub&logoColor=white" />
<img src="https://img.shields.io/badge/Apache_Tomcat-F8DC75?style=flat&logo=ApacheTomcat&logoColor=white" />
</div>

## 파일 설명
### JSP 
1. index.jsp : main 페이지
<p>
<img width="49%" alt="main" src="https://user-images.githubusercontent.com/117243197/210958735-0513114e-e6ea-4fb8-b080-7c4319c50364.png">
<img width="49%" alt="search" src="https://user-images.githubusercontent.com/117243197/210958950-2908e2cd-ade1-4ab0-bb5b-0435e67b03c3.png">
</p>

2. addWifiInfo.jsp : <code>Api</code> 데이터를 가져오며, 가져온 데이터 수를 화면에 출력하는 페이지
<img width="50%" alt="api" src="https://user-images.githubusercontent.com/117243197/210958947-af47a419-c717-4095-8ebb-746a8a693d24.png">

3. history.jsp : 위치 정보 조회한 리스트를 보여주는 페이지
<img width="50%" alt="history" src="https://user-images.githubusercontent.com/117243197/210958949-35c3eb4b-4ba7-48d4-b6e5-94f0000d0e0e.png">

4. delete.jsp : history.jsp 에서 받아온 id 값으로 wifi_history DB 에서 해당 값을 삭제하는 페이지

### JAVA
1. WifiInfo : 공공 와이파이 정보를 데이터를 <code>JSON</code> 으로 읽어옴(AddWifi), 내 위치에서 가까운 와이파이 위치를 조회(SearchWifi)
2. WifiDetail : 공공 wifi 정보를 객체화
3. InsertWifiInfo : WifiInfo 에서 AddWifi 로 읽어온 <code>JSON</code> 파일을 데이터 베이스에 insert
4. CalDistance : 내 위치의 좌표와 공공 와이파이의 좌표를 통해 <code>두 좌표의 거리</code>를 계산
5. History : 위치 정보 조회한 리스트를 객체화
6. HistoryDB : 위치 정보 조회한 history 를 wifi_history DB 에 삽입(historyInsert), 삭제(historyDel), 조회(historySelect)
