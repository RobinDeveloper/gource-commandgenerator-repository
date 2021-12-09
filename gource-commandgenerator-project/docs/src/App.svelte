<script>
	import Parameter from "./modules/Parameter.svelte";
	import NumberedParameter from "./modules/NumberedParameter.svelte";
	import SelectedParameter from "./modules/SelectedParameter.svelte";
	import CopyButton from "./modules/CopyButton.svelte";
	import MainParameterWindow from "./modules/parameterWindows/MainParameterWindow.svelte";

	export let GourceCommand = "gource ";
</script>

<svelte:options accessors={true}>
</svelte:options>

<div class="row">
	<div class="column">
		<MainParameterWindow/>
		<MainParameterWindow/>
	</div>
	<div class="column">
		<MainParameterWindow/>
		<MainParameterWindow/>
	</div>
	<div class="column">
		<MainParameterWindow/>
		<MainParameterWindow/>
	</div>
</div>


<p id="gourcecommand">Command: {GourceCommand}</p> <CopyButton/>


<style>

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