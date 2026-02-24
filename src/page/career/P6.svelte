<script>
  import Project from "./Project.svelte";
</script>

<Project name="카카오 선물하기 서버" imgSrc={["img/career/coop_kakao.png", "img/career/coop_kakao3.jpg"]}>
  <h4 class="title">프로젝트 설명</h4>
  <div class="content">
    <p class="contents-normal">
      카카오 선물하기 서버는 카카오톡을 통해 다른 사용자에게 선물을 보낼 수 있는 기능을 제공합니다.
    </p>
    <p class="contents-normal">
      이를 위해 파트너사와 통신 연동을 통해 쿠폰 발급, 연장, 폐기 서비스를 신속하고 신뢰성 있게 제공하는 것이 핵심입니다.
    </p>
    <p class="contents-normal">
      As-Is 발급서비스와 비교하여 발급 속도을 개선하고, 운영자가 서버 운영 상황을 모니터링 및 제어가능하도록 개선하였습니다.
    </p>
    <p class="contents-normal">
      또한 서버 이상 발생 시 생기는 대량 장애 메시지를 벌크동작으로 만들고 통계정보를 추가하여, 빠른 장애 복구 할 수 있게 하였습니다.
    </p>
    <span class="contents-strong">리뉴얼프로젝트 | 2인(Senior, Junior) | Senior 개발자로 참여</span>
  </div>
  <h4 class="title">수행 업무</h4>
  <div class="content">
    <p class="contents-normal">
      화면기획, 발급/선발급 서버, 운영자용 웹서버 개발
    </p>
    <p class="contents-strong">
      언어 - Java Spring Boot | Vue.js
    </p>
    <p class="contents-strong">
      기타 - HTTP | Oracle
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