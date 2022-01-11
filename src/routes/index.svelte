<script context="module">
	import { gql, GraphQLClient } from 'graphql-request';
	import { client } from '$lib/graphql-client';
	import HeroCopy from '$lib/components/heroCopy.svelte';

	export const load = async () => {
		const query = gql`
			query getPosts {
				posts(where: { featured: true }) {
					title
					publishDate
					slug
					description
				}
			}
		`;

		const { posts } = await client.request(query);

		return {
			props: {
				posts
			}
		};
	};
</script>

<script>
	export let posts;
</script>

<HeroCopy />

<pre>{JSON.stringify(posts, null, 2)}</pre>
