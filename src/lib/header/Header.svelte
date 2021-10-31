<script>
	import { page } from '$app/stores';
	import logo from './svelte-logo.svg';
	import 'papercss/dist/paper.min.css'
	import { Navbar } from 'spaper';

</script>

<header>
<nav class="border fixed split-nav">
  <div class="nav-brand">
    <h3><a href="#">Listing bank</a></h3>
  </div>
  <div class="collapsible">
    <input id="collapsible1" type="checkbox" name="collapsible1">
    <label for="collapsible1">
      <div class="bar1"></div>
      <div class="bar2"></div>
      <div class="bar3"></div>
	  <div class="bar4"></div>
    </label>
    <div class="collapsible-body">
      <ul class="inline">
        <li class:active={$page.path === '/'}><a sveltekit:prefetch href="/">Home</a></li>
			<li class:active={$page.path === '/about'}><a sveltekit:prefetch href="/about">About</a></li>
			<li class:active={$page.path === '/todos'}><a sveltekit:prefetch href="/todos">Todos</a></li>
			<li class:active={$page.path === '/paperkit'}><a sveltekit:prefetch href="/paperkit">paperkit</a></li>
      </ul>
    </div>
  </div>
</nav>

	
</header>

<style>

</style>
