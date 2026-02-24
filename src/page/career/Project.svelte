<script>
  import { slide, fade } from 'svelte/transition';

  export let name;
  export let imgSrc;

  let selectedIdx = 0;

  function selectIdx(idx) {
    selectedIdx = idx;
  }

  function prev() {
    selectedIdx = (selectedIdx - 1 + imgSrc.length) % imgSrc.length;
  }

  function next() {
    selectedIdx = (selectedIdx + 1) % imgSrc.length;
  }

  function onKeydown(e) {
    if (!imgSrc) return;
    if (e.key === 'ArrowLeft')   { e.preventDefault(); prev(); }
    if (e.key === 'ArrowRight' || e.key === ' ') { e.preventDefault(); next(); }
  }
</script>

<svelte:window on:keydown={onKeydown} />

<div class="root" in:fade>
  <div class="name-row">
    <h3 class="name">{name}</h3>
  </div>
  <slot />
  {#if !!imgSrc}
  <div class="thumbnails">
    {#each imgSrc as src, i}
    <button
      class="thumb-btn"
      class:active={selectedIdx === i}
      on:click={() => selectIdx(i)}
    >
      <img class="thumb" src={src} alt={name} />
    </button>
    {/each}
  </div>
  <div class="full-img-wrap">
    <div class="img-frame">
      {#if imgSrc.length > 1}
      <button class="nav-btn left" on:click={prev}>&#8249;</button>
      {/if}
      <img class="full-img" src={imgSrc[selectedIdx]} alt={name} />
      {#if imgSrc.length > 1}
      <button class="nav-btn right" on:click={next}>&#8250;</button>
      {/if}
    </div>
    {#if imgSrc.length > 1}
    <div class="img-counter">{selectedIdx + 1} / {imgSrc.length}</div>
    {/if}
  </div>
  {/if}
</div>

<style>
.root {
  padding: 20px 20px 40px 20px;
  font-family: KoHo;
  font-size: 1.25rem;
  font-weight: 700;
  color: rgb(146, 146, 146);
}
.name-row {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 15px;
  gap: 12px;
}
.name {
  font-size: 1.8rem;
  font-weight: 700;
  margin: 0;
  color: rgb(184, 232, 41);
}
.thumbnails {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 8px;
  margin-top: 28px;
  margin-bottom: 10px;
}
.thumb-btn {
  background: none;
  border: 2px solid transparent;
  border-radius: 8px;
  padding: 0;
  cursor: pointer;
  transition: border-color 0.15s, opacity 0.15s;
  opacity: 0.6;
}
.thumb-btn:hover {
  opacity: 1;
}
.thumb-btn.active {
  border-color: rgb(184, 232, 41);
  opacity: 1;
}
.thumb {
  display: block;
  width: 80px;
  height: 60px;
  object-fit: cover;
  border-radius: 6px;
}
.full-img-wrap {
  text-align: center;
  margin-bottom: 12px;
}
.img-frame {
  position: relative;
  display: inline-block;
  width: 90%;
}
.full-img {
  display: block;
  width: 100%;
  border-radius: 10px;
}
.nav-btn {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  background: rgba(0, 0, 0, 0.35);
  border: none;
  border-radius: 4px;
  color: rgba(255, 255, 255, 0.8);
  font-size: 1.4rem;
  width: 28px;
  height: 48px;
  cursor: pointer;
  transition: background 0.15s, color 0.15s;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 0;
}
.nav-btn:hover {
  background: rgba(0, 0, 0, 0.65);
  color: white;
}
.nav-btn.left  { left:  8px; }
.nav-btn.right { right: 8px; }
.img-counter {
  font-size: 0.8rem;
  color: rgb(120, 120, 120);
  margin-top: 6px;
  text-align: center;
}
</style>
