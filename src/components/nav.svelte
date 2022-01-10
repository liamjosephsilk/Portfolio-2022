<script>
	import { page } from '$app/stores';
	import { nav } from '../utils/navitems';
</script>

<header class="flex items-center py-8">
	<h3>LJS.</h3>
	<nav class="ml-16">
		<ul class="flex gap-10">
			{#each nav as navitems}
				<li class={$page.url.pathname === navitems.url ? 'font-semibold' : 'font-normal'}>
					<a href={navitems.url} class="hover:text-purple-600">
						{navitems.name}
					</a>
				</li>
			{/each}
		</ul>
	</nav>
</header>
