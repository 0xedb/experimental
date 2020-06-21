<script>
	import CardArea from './CardArea.svelte';
	const reset = "https://api.iconify.design/carbon:reset.svg";
	
		const cards = [
		{name: 'ace', pic: 'https://banner2.cleanpng.com/20180315/fje/kisspng-alices-adventures-in-wonderland-queen-of-hearts-pl-heart-playing-cards-5aaa18407509f5.0914836515210967684794.jpg'},
		{name: 'queen', pic : 'https://banner2.cleanpng.com/20171202/51c/playing-cards-png-5a228956720c96.3911822515122128224672.jpg'},
		{name: 'king', pic : 'https://w0.pngwave.com/png/610/755/poker-king-playing-card-card-game-standard-52-card-deck-king-png-clip-art.png'},
		{name: 'jack', pic : 'https://b1.pngbarn.com/png/861/876/pokerface-jack-of-spade-playing-card-png-clip-art.png'}
	]
</script>
<style>
	section {font-size: 20px;}
	img {height: 20px;}
	
	.instructions {
		display:flex;
	}
	
	#reset {
		margin-left: 150px; 
		border: 2px solid silver;
		border-radius: 10px;
	}
	
	.exp {
		padding: 14px;
		border: 2px solid silver;
		width: 30%;
		display: inline-block;
		margin: 10px;
		margin-bottom: 50px;
	}
	
</style>

<section>
	<div class="instructions">
		<div>Drag the characters into the dotted boxes</div>
		<button id="reset" type="reset">Reset &nbsp; <img src={reset} alt="" /></button>
	</div>
</section>

<CardArea />
<CardArea orig={true} {cards} />

<div>
	<button class='exp'>Show Explanation</button>
	<button class='exp'>Check Answer</button>
</div>