<script>  
	import Game from './Game.svelte';
	import Task from './Task.svelte'; 
	import Progress from './Progress.svelte';
	
</script>

<style>
	:global(*) {
		transition: all 0.4s ease 0.1s;
	} 
	
</style>

<Task />
<Progress />
<Game />