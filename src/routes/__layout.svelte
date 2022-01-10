<script>
	import '../app.css';
	import '@fontsource/inter/400.css';
	import '@fontsource/inter/600.css';
	import 'cal-sans';

	import Nav from '../components/nav.svelte';
	import Footer from '../components/footer.svelte';
</script>

<div class="px-2 md:px-24 lg:px-80 text-white bg-[#222222]">
	<main class="">
		<Nav />

		<slot />

		<Footer />
	</main>
</div>
