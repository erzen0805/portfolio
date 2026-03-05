<script>
  import { onMount, onDestroy } from 'svelte';

  const sections = [
    { id: 'intro', label: 'INTRO' },
    { id: 'about', label: 'ABOUT' },
    { id: 'career', label: 'CAREER' },
  ];

  let activeSection = 'intro';

  function scrollTo(id) {
    document.getElementById(id)?.scrollIntoView({ behavior: 'smooth' });
  }

  function updateActive() {
    const mid = window.innerHeight / 2;
    for (const { id } of sections) {
      const el = document.getElementById(id);
      if (!el) continue;
      const rect = el.getBoundingClientRect();
      if (rect.top <= mid && rect.bottom > mid) {
        activeSection = id;
        break;
      }
    }
  }

  onMount(() => {
    window.addEventListener('scroll', updateActive, { passive: true });
    updateActive();
  });

  onDestroy(() => {
    window.removeEventListener('scroll', updateActive);
  });
</script>

<nav class="nav-dots">
  {#each sections as { id, label }}
    <button
      class="dot-row"
      class:active={activeSection === id}
      on:click={() => scrollTo(id)}
      aria-label={label}
    >
      <span class="label">{label}</span>
      <span class="dot"></span>
    </button>
  {/each}
</nav>

<style>
.nav-dots {
  position: fixed;
  right: 20px;
  top: 50%;
  transform: translateY(-50%);
  display: flex;
  flex-direction: column;
  gap: 18px;
  z-index: 100;
}

.dot-row {
  display: flex;
  align-items: center;
  gap: 10px;
  background: none;
  border: none;
  cursor: pointer;
  padding: 4px 0;
}

.label {
  font-family: KoHo, sans-serif;
  font-size: 0.7rem;
  letter-spacing: 1.5px;
  color: rgba(255, 255, 255, 0.4);
  opacity: 1;
  transition: color 0.25s;
  white-space: nowrap;
}

.dot-row:hover .label {
  color: rgba(255, 255, 255, 0.85);
}

.dot-row.active .label {
  color: rgb(184, 232, 41);
}

.dot {
  width: 7px;
  height: 7px;
  border-radius: 50%;
  background-color: transparent;
  border: 1.5px solid rgba(255, 255, 255, 0.55);
  transition: border-color 0.3s, background-color 0.3s, transform 0.3s;
  flex-shrink: 0;
}

.dot-row.active .dot {
  background-color: rgb(184, 232, 41);
  border-color: rgb(184, 232, 41);
  transform: scale(1.5);
}

.dot-row:hover .dot {
  border-color: rgba(255, 255, 255, 0.9);
  background-color: rgba(255, 255, 255, 0.2);
}
</style>
