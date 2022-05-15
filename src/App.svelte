<script>
	import { Canvas, Layer, t } from "svelte-canvas"
	import Button from "./Button.svelte"

	$: render = ({ context, width, height }) => {
		context.beginPath()
		context.moveTo(50, 100)
		context.lineTo(200, 100)
		context.lineTo(100, 25)
		context.fillStyle = `green`;
		context.fill();
	};
</script>

<Canvas style="background-color:LightGray" width={400} height={400}>
	<Layer {render} />
	Generative Art
</Canvas>

<h1>Generative Art</h1>
<Button buttonType="primary">Randomize</Button>
<!-- <Button buttonType="secondary">Secondary</Button>
<Button buttonType="primary" inverse={true}>Inverse Primary</Button>
<Button buttonType="secondary" inverse={true}>Inverse Secondary</Button>
<Button flat={true}>Flat</Button>
<Button disabled={true}>Disabled</Button> -->

<style>
	@import 'https://unpkg.com/@responsive-ui/button@latest/lib/index.css';

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	body {
		background-color: darkgrey;
	}
</style>