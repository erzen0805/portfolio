<script>
  import Menu from './Menu.svelte';
  import NavDots from './NavDots.svelte';
  import Intro from './page/intro/Index.svelte';
  import About from './page/about/Index.svelte';
  import Career from './page/career/Index.svelte';

  const menuWidth = "100px";
</script>

<h1 style="display: none;">Donghyun Lee's portfolio</h1>
<Menu style="width: {menuWidth};"/>
<NavDots/>
<div style="margin-left: {menuWidth}; overflow: hidden;">
  <div id="intro"><Intro/></div>
  <div id="about"><About/></div>
  <div id="career"><Career/></div>
</div>
