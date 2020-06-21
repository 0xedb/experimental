<script>
	import {fade} from 'svelte/transition'
	export let instruction;
	export let id;
	export let len = 100; 
	
	const drag = (e) => {
		e.dataTransfer.setData('text', event.target.id); 
	}
	
	const drop = (e) => {
		const id = event.dataTransfer.getData('text'); 
		e.target.appendChild(document.getElementById(id))  
	}
</script>

<style>
	.block {
		border-radius: inherit;
		border: 2px solid crimson;
		background: #efd5d5;
		margin: 8px 0; 
		padding: 20px;
	}
</style>

{#if instruction}
<div {id} class='block' draggable={true} style={`width: calc(${len}% - 20px)`}
		 transition={fade}
		 on:dragstart={drag} on:dragover|preventDefault on:drop|preventDefault={drop}>
	{instruction} 
</div>
{/if}
<!--   -->