<script>
	import Card from './Card.svelte';
	export let orig = false;
	export let pic = "";
	export let hash = "";
	
	$: kind = orig ? 'orig' : null;
	
	
	const drop = (e) => {
		if(e.target.childElementCount) return;
		const data = e.dataTransfer.getData("text");
		const el = document.getElementById(data);
		e.target.appendChild(el);
		el.style.opacity = 1; 
	}  
	 
</script> 

<style> 
	div {
		display: flex;
		justify-content: center;
		align-items: center; 
		color: silver;
		width: 210px; 
		height: 250px; 
		margin: 10px;
		font-size: 30px;
		border-radius: 8px;
		border: 2px dashed #969696;
	}
	
	.orig {
		transform: scale(0.85);
	}
</style>
<div class={kind} on:drop|preventDefault={drop} on:dragover|preventDefault>
 <Card {pic} id={hash} />
</div>