<script>
  import Project from "./Project.svelte";
</script>

<Project name="선정산 서비스" imgSrc={[
  "img/career/bix_mf0.png",
  "img/career/bix_mf2.png",
  "img/career/bix_mf4.png",
  "img/career/bix_mf6.png",
  "img/career/bix_mf8.png",
  "img/career/bix_mf10.png",
  "img/career/bix_mf12.png",
  "img/career/bix_mf14.png",
]}>
  <h4 class="title">프로젝트 설명</h4>
  <div class="content">
    <p class="contents-normal">
      15개 PG사 거래 통보 연동, 8개 지급대행사 이체 연동을 지원하는 선정산 플랫폼입니다.
    </p>
    <p class="contents-normal">
      Quartz Scheduler 기반 배치 시스템으로 자동화된 정산 처리를 구현하였으며, 헥사고날 아키텍처로 설계되었습니다.
    </p>
    <p class="contents-normal">
      Vibe Coding(AI 페어 프로그래밍)을 도입하여 개발 생산성을 향상시켰습니다.
    </p>
    <span class="contents-strong">신규프로젝트 | 팀 리딩, BE 설계·개발, 시스템 아키텍처</span>
  </div>
  <h4 class="title">수행 업무</h4>
  <div class="content">
    <p class="contents-normal">
      PL 역할로 팀 리딩 및 BE 전체 설계·개발, 헥사고날 아키텍처 적용
    </p>
    <p class="contents-normal">
      PG사 거래 통보 수신 처리, 지급대행사 이체 연동, Quartz 기반 정산 배치 개발
    </p>
    <p class="contents-strong">
      언어 - Spring Boot 3.4 | Kotlin 2.1 | Java 21 | QueryDSL | MariaDB
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
