<script>
	import Progress from './Progress.svelte';
	import {fade} from 'svelte/transition'
	import Block from './Block.svelte';
 
		const drop = (e) => {
		const id = event.dataTransfer.getData('text');
		console.log(id, 'ddd')
		e.target.appendChild(document.getElementById(id))
	} 
</script>

<style>
	.activity {
		display: flex;
		flex-flow: column wrap;
		justify-content: center;
		border: 2px dashed silver;
		width: 70%; 
		padding: 80px 20px;
		border-radius: 8px; 
		margin-top: 15%;
	}
	
	.controls {
		margin-top: 30px;
	}
	
	.controls button {
		padding: 10px;
		width: 200px;
		margin: auto 10px;
	}
</style>

<Progress />
<section class='activity' on:drop|preventDefault={drop} on:dragover|preventDefault transition={fade}>
	<Block id='one' instruction={'input: ab + x + w'} len={85} />
	<Block id='two' instruction={'if a:'} len ={92} />
	<Block id='three' instruction={'else if a a > 2'} len ={70} />
	<Block id='four' instruction={'default: '} len ={95} />
	<Block id='five' instruction={'when i == 4'} len ={95} />
	<Block id='six' instruction={'89'} len ={60} />
</section>
<div class='controls'>
	<button type='button'>
	Show explanation
</button>
<button type='button'>
	Check answer
</button>
</div>
