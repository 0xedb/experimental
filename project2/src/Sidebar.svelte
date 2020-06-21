<script>
	import { fade } from 'svelte/transition';
	import Progress from './Progress.svelte';
	
	let ans = false 
	
	$: disabled = !ans
	
	const correct = (e) =>  ans = e.target.id === "second"  
 
</script>
<style>
	.sidebar {
		display: block;
		width: 100%;
	}
	button {
		margin-top: 10px;
		width: 230px;
		display: block; 
		padding: 9px;
		border: 2px solid silver;
	}
	
	label {
		font-size: 28px;
		display: inline;
	}
	
	.msg {
		padding: 10px;
	}
	
	section {
		font-size: 25px;
	}
	 
	input[type='radio'], label {
    transform: scale(1.8);
		cursor: pointer;
}
	.pos {
		padding-top: 20px;
	}
</style>
 

<section on:click={correct} class='sidebar'>
<Progress /> 
<div class='pos'> 
	<div class='inp' on:click={(e) => console.log(e.target)}>
			<input id="first" type='radio' value="9999" name="ans" /> 
		<label for="first">&nbsp;9999</label>
	</div>
<div  class='inp'>
	<input id="second" type='radio' value="10000" name="ans" />  
 <label for="second">&nbsp;10000</label>
	</div>
			
<div class='inp'>
			<input id="third" type='radio' value="1100" name="ans" /> 
	<label for="third">&nbsp;1100</label>   
	</div>
</div>

<div>
{#if ans}
	<div class='msg' in:fade out:fade>
		<strong>Correct! &#127881;</strong>
	<div>
		{Math.round(Math.random() * 100)}% of people got this right.
	</div>
	</div>
	
{/if}
</div>
	<button type='button' {disabled} on:click|stopPropagation>Submit</button>
	<button type='button' {disabled} on:click|stopPropagation>Show explanation</button>
</section>