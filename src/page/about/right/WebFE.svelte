<script>
  import ImageBox from './ImageBox.svelte';
</script>

<h3 class="subtitle">기본</h3>
<ImageBox source="img/skill/html.png" title="HTML5" />
<ImageBox source="img/skill/css.png" title="CSS" />
<ImageBox source="img/skill/js.png" title="JavaScript" />
<ImageBox source="img/skill/es6.png" title="ES6" />
<ImageBox source="img/skill/jquery.png" title="jQuery" />

<h3 class="subtitle">프레임워크 / 도구</h3>
<ImageBox source="img/skill/typescript.png" title="TypeScript" />
<ImageBox source="img/skill/tailwind.png" title="Tailwind CSS" />
<ImageBox source="img/skill/svelte.png" title="Svelte.js" />
<ImageBox source="img/skill/react.png" title="React.js" />
<ImageBox source="img/skill/nextjs.png" title="Next.js" />
<ImageBox source="img/skill/vue.png" title="Vue.js" />
<ImageBox source="img/skill/threejs.png" title="Three.js" />

<style>
.subtitle {
  grid-column: 1 / -1;
  color: rgb(200, 200, 200);
  font-size: 0.85rem;
  font-weight: 600;
  letter-spacing: 0.05em;
  text-transform: uppercase;
  margin: 16px 0 4px 0;
  padding-bottom: 4px;
  border-bottom: 1px solid rgb(100, 100, 100);
}
.subtitle:first-child {
  margin-top: 4px;
}
</style>
