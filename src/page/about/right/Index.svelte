<script>
  import Languages from './Languages.svelte';
  import WebFE from './WebFE.svelte';
  import ETC from './ETC.svelte';

  let viewPage = 0;
  function onChangePage(pageIndex) {
    viewPage = pageIndex;
  }
</script>

<section class="container">
  <div class="category">
    <ul>
      <li class:selected={viewPage===0} on:click|preventDefault={()=>onChangePage(0)}>- 언어 & 프레임워크</li>
      <li class:selected={viewPage===1} on:click|preventDefault={()=>onChangePage(1)}>- 웹 프론트엔드</li>
      <li class:selected={viewPage===2} on:click|preventDefault={()=>onChangePage(2)}>- 인프라 / 협업</li>
    </ul>
  </div>
  <div class="contents-parent">
    <div class="contents">
      {#if viewPage === 0}
      <Languages />
      {:else if viewPage === 1}
      <WebFE />
      {:else if viewPage === 2}
      <ETC />
      {/if}
    </div>
  </div>
</section>

<style>
.container {
  width: 90%;
  height: 100%;
  margin-top: 100px;
  padding: 0 30px 0 10px;
  background-color: rgb(76, 76, 76);
  display: inline-block;
  position: relative;
}
.container::after {
  transform: skewX(0.3deg) rotateZ(-7deg);
  content: "";
  width: 110%;
  height: 90%;
  background-color: rgb(46, 46, 46);
  position: absolute;
  top: 40px;
  box-shadow: rgb(0 0 0 / 50%) 0px 4px 24px;
}
.category {
  transform: skewX(0.3deg) rotateZ(-7deg);
}
.category li {
  margin-right: 20px;
  font-size: 1.25rem;
  color: rgb(158, 158, 158);
  cursor: pointer;
  display: inline;
}
.category .selected {
  color: rgb(245, 210, 14);
}
.contents-parent {
  display: flex;
  align-items: flex-start;
  z-index: 1;
  position: relative;
  width: 95%;
  left: 10%;
  top: 13%;
  height: 80%;
  overflow-y: auto;
}
.contents {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  width: 100%;
  padding: 3px;
}
</style>
