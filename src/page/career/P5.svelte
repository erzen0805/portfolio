<script>
  import Project from "./Project.svelte";
</script>

<Project name="가상화폐 자동투자 봇" imgSrc={["img/career/vcts_my.png"]}>
  <h4 class="title">프로젝트 설명</h4>
  <div class="content">
    <p class="contents-normal">
      이 서버 프로그램은 딥러닝 알고리즘을 활용하여 가상화폐 거래를 자동화합니다.
    </p>
    <p class="contents-normal">
      딥러닝을 통해 가격 패턴과 트렌드 등을 학습하고 예측하여 효과적인 투자 결정을 내립니다.
    </p>
    <p class="contents-normal">
      이 봇을 사용하여 운영 및 백데이터 수집을 위해 현재도 적은 금액으로 활동 중입니다.
    </p>
    <p class="contents-normal">
      빗썸, 바이낸스를 포함한 다수의 거래소의 API와 연동되어 있습니다.
    </p>
    <span class="contents-strong">신규프로젝트 | 1인 | 전체 개발</span>
  </div>
  <h4 class="title">수행 업무</h4>
  <div class="content">
    <p class="contents-normal">
      데몬서버 개발, 거래소 API연동, 알고리즘 개발 및 시뮬레이션
    </p>
    <p class="contents-strong">
      언어 - Python
    </p>
    <p class="contents-strong">
      기타 - HTTP | Keras | MySQL | Redis
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