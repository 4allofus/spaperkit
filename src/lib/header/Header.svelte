<script>
	import { page } from '$app/stores';
	import logo from './svelte-logo.svg';
	import 'papercss/dist/paper.min.css'
	import { Navbar } from 'spaper';

</script>

<header>
	<div class="corner">
		<a href="https://kit.svelte.dev">
			<img src={logo} alt="SvelteKit" />
		</a>
	</div>

	<Navbar split={false}>
    	<h3 slot="PaperKit">
      	<a href="#">Paperkit</a>
    	</h3>
    	<ul class="inline">
			<li class:active={$page.path === '/'}><a sveltekit:prefetch href="/">Home</a></li>
			<li class:active={$page.path === '/about'}><a sveltekit:prefetch href="/about">About</a></li>
			<li class:active={$page.path === '/todos'}><a sveltekit:prefetch href="/todos">Todos</a></li>
			<li class:active={$page.path === '/paperkit'}><a sveltekit:prefetch href="/paperkit">paperkit</a></li>		
    	</ul>
  	</Navbar>


</header>

<style>

</style>
