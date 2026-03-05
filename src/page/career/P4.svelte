<script>
  import Project from "./Project.svelte";
</script>

<Project name="ATM/KIOSK 관리 서버" imgSrc={["img/career/atms_hyosung.jpg", "img/career/atms_hyosung2.jpg"]}>
  <h4 class="title">프로젝트 설명</h4>
  <div class="content">
    <p class="contents-normal">
      자동화 기기들을 원격으로 관리하는 역할을 수행합니다.
    </p>
    <p class="contents-normal">
      이 서버는 사용자 입출금 이력 관리, 기기 상태 모니터링, 소프트웨어 업데이트, 배치 스케줄 등록, 광고 스케줄 등록 등의 기능을 제공합니다.
    </p>
    <span class="contents-strong">유지보수,리뉴얼 | 4인(FE:1, BE:3) | Back-end 개발자로 참여</span>
  </div>
  <h4 class="title">수행 업무</h4>
  <div class="content">
    <p class="contents-normal">
      ATM Agent, Application Server, Web Server 유지보수
    </p>
    <p class="contents-strong">
      언어 - JSP | ASP.NET | Vanilla JS | GCC
    </p>
    <p class="contents-strong">
      기타 - HTTP | Oracle | MSSQL
    </p>
  </div>
</Project>

<style>
.title {
  font-size: 1.2rem;
  font-weight: 600;
  color: white;
  margin: 40px 0 0 20px;
}
.content {
  margin: 20px 10px 0px 10px;
}
.contents-strong {
  color: rgb(146, 146, 146);
  font-weight: 700;
  font-size: 1.1rem;
  line-height: 1.7;
}
.contents-normal {
  font-size: 1.05rem;
  font-weight: 400;
  color: rgb(213, 213, 213);
  line-height: 1.7;
  margin-bottom: 0.5em;
}
</style>