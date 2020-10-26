<script>
	import Block from "./Block.svelte";
	import Container from './Container.svelte' 
	let size=100, color='#0400ff', opacity=.5; 

</script>

<main>
	

	<Block {color} {size} {opacity}/>
	<div>
	<label> Цвет {color}
		<input bind:value={color} type='color'/>
	</label>
	<label> Размер {size}px
		<input type=range bind:value={size} min="0" max=280 step="1">
	</label>
	<label> Прозрачность {opacity}
		<input type=range bind:value={opacity} min="0" max=1 step=".01">
	</label>
</div>


	<Container />
</main>

<style>
	main {
		padding: 1em;
		margin: 0 auto;
		width: 300px;
	}

	input {
	display: block;
	height: 40px;
	border: none;
}




	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>

