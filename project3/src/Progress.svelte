<script>
	const left = "https://api.iconify.design/eva:arrow-ios-back-fill.svg?color=%23c0c0c096";
	const right = "https://api.iconify.design/eva:arrow-ios-forward-fill.svg?color=%23c0c0c096";
</script>
<style>
	img {
		height: 40px;
	}
	
	section {
		display: flex;
		position: absolute;
		flex-flow: column wrap;
		justify-content: center;
		align-items: center;
		top: 1%;
		right: 10%;
	}
	
	div {
		display: flex;
		align-items: center;
		font-size: 30px;
	}
	
	.progress > div {
		display: inline-block;
		background: #000;
		margin: 1px;
		padding: 1px;
		width: 60px;
		height: 20px;
	}
	
	.progress > div:nth-child(4) {
		background: orange;
	} 
	
	.progress > div:nth-child(5) {
		width: 80px;
		background: #c0c0c052;
	} 
</style>

<section>
<h1>LOGIC</h1>
<div>
	<img class="arrow" src={left} alt="" />
	<div class='progress'>
		<div></div>
		<div></div>
		<div></div>
		<div></div>
		<div></div>
	</div>
	<img class="arrow" src={right} alt="" />
</div>  
</section>