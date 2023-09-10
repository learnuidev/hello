<script>
	import Counter from './Counter.svelte';
	import welcome from '$lib/images/svelte-welcome.webp';
	import welcome_fallback from '$lib/images/svelte-welcome.png';
	import Button from '$lib/components/ui/button/button.svelte';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>


<div>

	<h1 class="text-2xl font-bold">Welcome, <span class="font-light"> Vishal</span></h1>

	<h2 class="my-4">Continue Learning</h2>

	<!-- <div>
		["svelte", "nextjs"].map(item => {
			return <Button>{item}</Button>
		})
	</div> -->

	<ul>
		{#each ["svelte", "nextjs", "modern css"] as data}
			<li>{data}</li>
		{/each} 
	</ul>


</div>