<script>
	export let pic = ''
	export let id = ''
	
	const drag = (e) => {
		e.target.style.opacity = 0.1;
		e.dataTransfer.dropEffect = "move"; 
		e.dataTransfer.setData("text", e.target.id); 
	}
	
	const drop = (e) => {
		e.target.style.opacity = 1; 
	} 
</script>

<style>
	img {
		height: 98%;
		width: 98%; 
	}
</style> 
 
{#if pic} 
	<img {id} on:dragstart={drag} on:drop|preventDefault={drop} src={pic} alt='card'/>
{/if}
 