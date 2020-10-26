<script>
	export let size, color, opacity; 
	$: styles = `
		height: ${size}px;
		width: ${size}px;
		background: ${color};
		opacity: ${opacity};
	`
</script>

<div style='height:300px;'>
	<div  style={styles}></div>
</div>


