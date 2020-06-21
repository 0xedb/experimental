<script>
	import CardDest from './CardDest.svelte';
	export let cards = null;
	const fields = new Array(4)
		 
	export let orig = false;
</script>
<style>
	section {
		display: flex; 
		align-items: center; 
		margin-top: 10px;
	}
</style>

<section> 
	{#each fields as field, ind(ind)}		
	<CardDest {orig} pic={cards ? cards[ind].pic : null} hash={cards ? cards[ind].name : null} />
	{/each}
</section>

