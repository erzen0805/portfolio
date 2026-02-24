<script>
  import Project from "./Project.svelte";
</script>

<Project name="바다이야기" imgSrc={["img/career/enton_sea_story.jpg"]}>
  <h4 class="title">프로젝트 설명</h4>
  <div class="content">
    <p class="contents-normal">
      대표적인 도박성이 강한 아케이드 게임으로, 2000년도 초반 많은 성인용 게임장의 인기를 휩쓸었습니다.
    </p>
    <p class="contents-normal">
      인터넷과 결합하여 합법적 인터넷 도박장을 만드는 것을 목표로 시작된 프로젝트 입니다.
    </p>
    <span class="contents-strong">신규프로젝트 | 4인 | S/W 개발자로 참여</span>
  </div>
  <h4 class="title">수행 업무</h4>
  <div class="content">
    <p class="contents-normal">
      화면 개발, 운영도구 개발, 게임 봇 개발
    </p>
    <p class="contents-strong">
      언어 - MFC
    </p>
    <p class="contents-strong">
      기타 - MSSQL
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