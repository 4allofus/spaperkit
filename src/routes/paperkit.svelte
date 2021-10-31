<script context="module">
    import { browser, dev } from '$app/env';
    import 'papercss/dist/paper.min.css'

    import { Button } from 'spaper';
    import { Alert } from 'spaper';

	// we don't need any JS on this page, though we'll load
	// it in dev so that we get hot module replacement...
	export const hydrate = dev;

	// ...but if the client-side router is already loaded
	// (i.e. we came here from elsewhere in the app), use it
	export const router = browser;

	// since there's no dynamic data here, we can prerender
	// it so that it gets served as a static asset in prod
	export const prerender = true;

	let targetLocation = 'jakarta';
</script>

<svelte:head>
	<title>Paperkit</title>
</svelte:head>

<div class="paper container-lg">
	<h1>SPaper</h1>
	<input bind:value={targetLocation} placeholder="masukan lokasi">

	<div class="mapouter">
	<div class="gmap_canvas">
	<iframe class="gmap_iframe" width="100%" frameborder="0" scrolling="no" marginheight="0" marginwidth="0" 
	src="https://maps.google.com/maps?width=600&amp;height=400&amp;hl=en&amp;
	q={targetLocation}}&amp;
	t=&amp;z=14&amp;ie=UTF8&amp;iwloc=B&amp;output=embed">
	</iframe><a href="https://www.fnfgo.com/">FNF</a></div>
	<style>.mapouter{position:relative;text-align:right;width:100%;height:400px;}.gmap_canvas {overflow:hidden;background:none!important;width:100%;height:400px;}.gmap_iframe {height:400px!important;}</style></div>

</div>

<div class="paper container-lg">
	<div class="row">
		<div class="col-3 col">
			<div class="card" style="width: 20rem;">
  				<div class="card-body">
    			<h4 class="card-title">My awesome Paper card!</h4>
    			<h5 class="card-subtitle">Nice looking subtitle.</h5>
    			<p class="card-text">You can also place image on the bottom of the card.</p>
    			<button>Saya tertarik</button>
  				</div>
  				<img class="image-bottom" src="https://unsplash.it/550/250" alt="Card example image">
			</div>
		</div>
		<div class="col-3 col">
			<div class="card" style="width: 20rem;">
  				<div class="card-body">
    			<h4 class="card-title">My awesome Paper card!</h4>
    			<h5 class="card-subtitle">Nice looking subtitle.</h5>
    			<p class="card-text">You can also place image on the bottom of the card.</p>
    			<button>Saya tertarik</button>
  				</div>
  				<img class="image-bottom" src="https://unsplash.it/550/250" alt="Card example image">
			</div>
		</div>
		<div class="col-3 col">
			<div class="card" style="width: 20rem;">
  				<div class="card-body">
    			<h4 class="card-title">My awesome Paper card!</h4>
    			<h5 class="card-subtitle">Nice looking subtitle.</h5>
    			<p class="card-text">You can also place image on the bottom of the card.</p>
    			<button>Saya tertarik</button>
  				</div>
  				<img class="image-bottom" src="https://unsplash.it/550/250" alt="Card example image">
			</div>
		</div>
		<div class="col-3 col">
			<div class="card" style="width: 20rem;">
  				<div class="card-body">
    			<h4 class="card-title">My awesome Paper card!</h4>
    			<h5 class="card-subtitle">Nice looking subtitle.</h5>
    			<p class="card-text">You can also place image on the bottom of the card.</p>
    			<button>Saya tertarik</button>
  				</div>
  				<img class="image-bottom" src="https://unsplash.it/550/250" alt="Card example image">
			</div>
		</div>
	</div>

</div>

<style>
</style>
