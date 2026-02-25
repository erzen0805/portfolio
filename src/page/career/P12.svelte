<script>
  import Project from "./Project.svelte";
</script>

<Project name="에브리페이(EveryPay) 신용결제 정산 ERP" imgSrc={[
  "img/career/bix_ep4.png",
  "img/career/bix_ep5.png",
  "img/career/bix_ep10.png",
  "img/career/bix_ep11.png",
  "img/career/bix_ep12.png",
  "img/career/bix_ep13.png",
  "img/career/bix_ep16.png",
  "img/career/bix_ep17.png",
  "img/career/bix_ep18.png",
  "img/career/bix_ep20.png",
]}>
  <h4 class="title">프로젝트 설명</h4>
  <div class="content">
    <p class="contents-normal">
      가맹점 7,000개를 관리하고 일 평균 3,000건의 거래를 처리하는 신용결제 정산 ERP 시스템입니다.
    </p>
    <p class="contents-normal">
      관리자(admin.everypay.me) / 가맹점(store.everypay.me) 이중 서비스 구조로 운영됩니다.
    </p>
    <p class="contents-normal">
      개발자로 시작하여 FE팀장, 프로젝트 팀장으로 역할을 확대하며 전체 시스템을 리딩하였습니다.
    </p>
    <span class="contents-strong">신규프로젝트·운영 | 배치서버, FE 개발 → 프로젝트 리딩</span>
  </div>
  <h4 class="title">수행 업무</h4>
  <div class="content">
    <p class="contents-normal">
      배치 서버 및 FE 개발 후 FE팀장, 프로젝트 팀장으로 역할 확대
    </p>
    <p class="contents-normal">
      정산 배치 시스템 설계·개발, 관리자/가맹점 포털 FE 개발, 팀 리딩 및 일정 관리
    </p>
    <p class="contents-strong">
      언어 - Spring Boot 3.3 | Kotlin | Next.js 14 | MariaDB | RabbitMQ | Redis
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
