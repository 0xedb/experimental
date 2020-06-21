<script>
	import Sidebar from './Sidebar.svelte'; 
	const src = 'https://1.bp.blogspot.com/-e0UwaQI12Ag/WH0A3gl7TaI/AAAAAAAABAQ/6kBVTyvaPC4L-Fyas_wKMFOsXNbmJ2lmQCLcB/s1600/output_b8VOnq.gif'
</script>

<style>
	:global(*) {
		transition: all 0.4s ease 0.1s;
	}
	.anim, .inst {
		display: flex; 
		font-size: 20px;
	} 
	 
	.first img {
		width: 80%;
		margin-top: 20px;
	}	
	
 </style>

	<p class='inst'>
		What is the sum of the value of &nbsp; <var>x</var> &nbsp;?
	</p>
		<strong>Hint</strong>
<section class='anim'>
	<div class="first">
		<img {src} alt='eq' />
	</div>
	<Sidebar />
</section>
