<script>
	import Parameter from "./modules/Parameter.svelte";
	import NumberedParameter from "./modules/NumberedParameter.svelte";
	import SelectedParameter from "./modules/SelectedParameter.svelte";
	import CopyButton from "./modules/CopyButton.svelte";

	export let GourceCommand = "Gource ";
</script>

<svelte:options accessors={true}>
</svelte:options>
<!--gource  --max-user-speed 500 --seconds-per-day 0.05 --file-idle-time 10 -e 0.005 -f --max-files 300 --hide-files-->
<main>
	<p>Command: </p> <p id="gourcecommand">{GourceCommand}</p> <CopyButton/>
</main>

<div class="row">
	<div class="column">
		<NumberedParameter Text="--max-user-speed"/><br>
		<NumberedParameter Text="--seconds-per-day"/><br>
		<NumberedParameter Text="--file-idle-time"/><br>
		<NumberedParameter Text="-e"/><br>
		<NumberedParameter Text="--max-files"/><br>
		<NumberedParameter Text="--seconds-per-day"/><br>
		<NumberedParameter Text="--start-position"/><br>
		<NumberedParameter Text="--stop-position"/><br>
		<NumberedParameter Text="--auto-skip-seconds"/><br>
		<NumberedParameter Text="--file-idle-time"/><br>
		<NumberedParameter Text="--bloom-multiplier"/><br>
		<NumberedParameter Text="--bloom-intensity"/><br>
	</div>
	<div class="column">
		<NumberedParameter Text="--title" Placeholder="Enter title"/><br>
		<NumberedParameter Text="-" Placeholder="Enter resolution"/><br>
		<SelectedParameter Text="--camera-mode"/><br>
	</div>
	<div class="column">
		<Parameter Text="-f"/><br>
		<Parameter Text="--hide-files"/><br>
		<Parameter Text="--disable-auto-skip"/><br>
		<Parameter Text="--disable-auto-rotate"/>
	</div>
</div>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}

	.column {
		float: left;
		width: 33.33%;
	}

	/* Clear floats after the columns */
	.row:after {
		content: "";
		display: table;
		clear: both;
	}
</style>