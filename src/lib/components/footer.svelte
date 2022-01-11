<script>
	import getYear from '$lib/getYear';
	import { page } from '$app/stores';

	const nav = [
		{
			url: '/',
			name: 'Home'
		},
		{
			url: '/posts',
			name: 'Posts'
		},
		{
			url: '/snippets',
			name: 'Snippets'
		}
	];
</script>

<footer class="border-t border-t-gray-700 py-8">
	<nav class="mb-10">
		<ul class="flex flex-col gap-10">
			{#each nav as navitems}
				<li class={$page.url.pathname === navitems.url ? 'font-semibold' : 'font-normal'}>
					<a href={navitems.url} class="hover:text-purple-600">
						{navitems.name}
					</a>
				</li>
			{/each}
		</ul>
	</nav>
	<p class="text-xs font-thin">
		&#169; {getYear(new Date())} Liam Silk built with SvelteKit and Tailwind.
	</p>
</footer>
