<script>
  import { fly } from 'svelte/transition';
  import { inview } from 'svelte-inview';
  import P0 from './P0.svelte';
  import P1 from './P1.svelte';
  import P2 from './P2.svelte';
  import P3 from './P3.svelte';
  import P4 from './P4.svelte';
  import P5 from './P5.svelte';
  import P6 from './P6.svelte';
  import P7 from './P7.svelte';
  import P8 from './P8.svelte';
  import P9 from './P9.svelte';
  import P10 from './P10.svelte';
  import P11 from './P11.svelte';
  import P12 from './P12.svelte';
  import UnderConstruction from '@/common/UnderConstruction.svelte';

  let stylish=$$props.style;

  let isInView = false;
  const viewCondition = { unobserveOnEnter: false, rootMargin: '-200px' };
  const onViewChange = ({detail}) => {
    isInView = detail.inView;
  };

  const groups = [
    { period: "~2026 (1.4년)", company: "빅스솔루션", projects: [
      { name: "에브리페이 정산 ERP", pageIndex: 12 },
      { name: "펌뱅킹 서비스",       pageIndex: 11 },
      { name: "선정산 서비스",       pageIndex: 10 },
    ]},
    { period: "~2024 (2.5년)", company: "비츠로시스", projects: [
      { name: "전력설비 예방진단", pageIndex: 9 },
    ]},
    { period: "~2022 (1.2년)", company: "YPP", projects: [
      { name: "전력설비 예방진단", pageIndex: 8 },
    ]},
    { period: "~2021 (1.0년)", company: "Autonics", projects: [
      { name: "SCADA", pageIndex: 7 },
    ]},
    { period: "~2020 (1.2년)", company: "쿠프마케팅", projects: [
      { name: "카카오 선물하기 서버", pageIndex: 6 },
    ]},
    { period: "~2019 (0.5년)", company: "개인개발", projects: [
      { name: "가상화폐 자동투자 봇", pageIndex: 5 },
    ]},
    { period: "~2018 (1.3년)", company: "효성TNS", projects: [
      { name: "ATM/KIOSK 관리 서버", pageIndex: 4 },
    ]},
    { period: "~2017 (7.3년)", company: "유호전기공업", projects: [
      { name: "전력설비 예방진단", pageIndex: 3 },
    ]},
    { period: "~2014 (0.8년)", company: "가보", projects: [
      { name: "전력 SCADA", pageIndex: 2 },
    ]},
    { period: "~2009 (1.0년)", company: "엔톤", projects: [
      { name: "바다이야기", pageIndex: 1 },
    ]},
    { period: "~2009", company: "동명대학교", projects: [
      { name: "컴퓨터공학과 학사", pageIndex: 0 },
    ]},
  ];

  let viewPage = 12;
  function onChangePage(pageIndex) {
    viewPage = pageIndex;
  }
</script>

<main class="container" style={stylish} use:inview={viewCondition} on:change={onViewChange}>
  <h2 style="display: none;">Career</h2>
  <div class="left-col">
  {#if isInView}
    <div class="contents" in:fly={{ y: 200, duration: 1000 }}>
      {#if viewPage === 12}
        <P12/>
      {:else if viewPage === 11}
        <P11/>
      {:else if viewPage === 10}
        <P10/>
      {:else if viewPage === 9}
        <P9/>
      {:else if viewPage === 8}
        <P8/>
      {:else if viewPage === 7}
        <P7/>
      {:else if viewPage === 6}
        <P6/>
      {:else if viewPage === 5}
        <P5/>
      {:else if viewPage === 4}
        <P4/>
      {:else if viewPage === 3}
        <P3/>
      {:else if viewPage === 2}
        <P2/>
      {:else if viewPage === 1}
        <P1/>
      {:else if viewPage === 0}
        <P0/>
      {:else}
        <UnderConstruction />
      {/if}
    </div>
  {/if}
  </div>
  <div style="width: 500px;">
    <ul class="list">
      {#each groups as group}
        {@const isActive = group.projects.some(p => p.pageIndex === viewPage)}
        <li class="group-row" class:active={isActive}>
          <div
            class="row-top"
            on:click={() => onChangePage(group.projects[0].pageIndex)}
            on:keypress={() => onChangePage(group.projects[0].pageIndex)}
            role="button"
            tabindex="0"
          >
            <span class="label-period">{group.period}</span>
            <span class="label-company">{group.company}</span>
          </div>
          <div class="row-projects">
            {#each group.projects as proj}
              <div
                class="proj-name"
                class:selected={viewPage === proj.pageIndex}
                on:click={() => onChangePage(proj.pageIndex)}
                on:keypress={() => onChangePage(proj.pageIndex)}
                role="button"
                tabindex="0"
              >{proj.name}</div>
            {/each}
          </div>
        </li>
      {/each}
    </ul>
  </div>
</main>

<style>
.container {
  display: flex;
  align-items: stretch;
  height: 100vh;
  padding: 40px 0;
  font-family: KoHo;
  font-size: 1.25rem;
  font-weight: 700;
  color: rgb(146, 146, 146);
}
.left-col {
  width: calc(100% - 500px);
  display: flex;
  flex-direction: column;
  padding-bottom: 0;
}
.contents {
  width: 100%;
  background-color: rgb(43, 44, 42);
  border-radius: 25px;
  flex: 1;
  min-height: 500px;
  box-shadow: rgb(0, 0, 0) 0px 0px 20px inset;
  overflow-y: auto;
}
.list {
  padding: 30px;
}
.group-row {
  margin-bottom: 22px;
  padding-left: 10px;
  border-left: 5px solid transparent;
}
.group-row.active {
  border-left: 5px solid pink;
}
.row-top {
  display: flex;
  align-items: baseline;
  gap: 8px;
  cursor: pointer;
}
.label-period {
  display: inline-block;
  width: 130px;
  flex-shrink: 0;
  font-size: 1.05rem;
  color: rgb(140, 140, 140);
}
.label-company {
  font-size: 1.05rem;
  font-weight: 700;
  color: rgb(190, 190, 190);
}
.group-row.active .label-company {
  color: white;
}
.row-projects {
  margin-top: 5px;
  padding-left: 20px;
  display: flex;
  flex-direction: column;
  gap: 4px;
}
.proj-name {
  cursor: pointer;
  font-size: 0.95rem;
  font-weight: 500;
  color: rgb(130, 130, 130);
  transition: color 0.15s;
  line-height: 1.5;
}
.proj-name::before {
  content: '— ';
  color: rgb(80, 80, 80);
  font-size: 0.85rem;
}
.proj-name:hover {
  color: rgb(200, 200, 200);
}
.proj-name.selected {
  color: white;
  font-weight: 700;
}
.proj-name.selected::before {
  color: pink;
}
</style>
