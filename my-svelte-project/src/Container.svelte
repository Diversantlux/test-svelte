<script>
	let current = 'foo';
</script>

<style>
	button {
		display: block;
        min-width: 75px;
        min-height: 75px;
	}

	.active {
		opacity:0;
		color: white;
	}
	.green {
		background-color:green;
	}
	.red {
		background-color:red;
	}
	.blue {
		background-color:blue;
	}
</style>

<button class="red"
	class:active="{current === 'red'}"
	on:click="{() => current = current == 'red' ? '' : 'red' }"
>red</button>

<button class="green"
	class:active="{current === 'green'}"
	on:click="{() => current = current == 'green' ? '' : 'green'}"
>green</button>

<button class="blue"
	class:active="{current === 'blue'}"
	on:click="{() => current = current == 'blue' ? '' : 'blue'}"
>blue</button>

