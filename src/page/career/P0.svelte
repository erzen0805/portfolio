<script>
  import Project from "./Project.svelte";
</script>

<Project name="동명대학교 컴퓨터공학과" imgSrc={["img/career/university2.png"]}>
  <h4 class="title">학생 시절</h4>
  <div class="content">
    <p class="contents-normal">
      동명대학교는 부산광역시에 있는 사립대학입니다.
    </p>
    <p class="contents-normal">
      정보공학부로 입학하여 컴퓨터공학과를 졸업하였고 평점 3.09/4.5로 이수하였습니다.
    </p>
    <p class="contents-normal">
      관심분야와 비관심분야 성적 차이가 큰편이였고, 성적장학금 2회를 (1,2등) 받았습니다.
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