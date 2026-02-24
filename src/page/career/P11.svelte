<script>
  import Project from "./Project.svelte";
</script>

<Project name="펌뱅킹 서비스" imgSrc={[
  "img/career/bix_tn1.png",
  "img/career/bix_tn3.png",
  "img/career/bix_tn4.png",
  "img/career/bix_tn6.png",
  "img/career/bix_tn9.png",
]}>
  <h4 class="title">프로젝트 설명</h4>
  <div class="content">
    <p class="contents-normal">
      기업 자금관리 및 지급 서비스를 위한 펌뱅킹 프론트엔드 시스템입니다.
    </p>
    <p class="contents-normal">
      더즌, 키움페이, 위즈페이, 윈글로벌, 쿠콘 등 5개 지급대행사 연동을 지원합니다.
    </p>
    <p class="contents-normal">
      17개 기능 모듈을 구현하여 기업 자금 관리의 전 과정을 커버합니다.
    </p>
    <span class="contents-strong">신규프로젝트 | FE 전담 개발</span>
  </div>
  <h4 class="title">수행 업무</h4>
  <div class="content">
    <p class="contents-normal">
      FE 전담 개발, 17개 기능 모듈 설계 및 구현
    </p>
    <p class="contents-normal">
      5개 지급대행사 연동 UI, 자금관리 대시보드, 이체 처리 화면 개발
    </p>
    <p class="contents-strong">
      언어 - Next.js 14 | TypeScript | Redux Toolkit | Tailwind CSS
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
