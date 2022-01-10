<script>
	import getYear from '../utils/getYear';
	import { nav } from '../utils/navItems';
	import { page } from '$app/stores';
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
