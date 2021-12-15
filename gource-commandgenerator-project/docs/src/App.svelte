<script>
	import Parameter from "./modules/Parameter.svelte";
	import NumberedParameter from "./modules/NumberedParameter.svelte";
	import SelectedParameter from "./modules/SelectedParameter.svelte";
	import CopyButton from "./modules/CopyButton.svelte";
	import MainParameterWindow from "./modules/parameterWindows/MainParameterWindow.svelte";
	import FileParameterWindow from "./modules/parameterWindows/FileParameterWindow.svelte";
	import TextParameterWindow from "./modules/parameterWindows/TextParameterWindow.svelte";
	import UserParameterWindow from "./modules/parameterWindows/UserParameterWindow.svelte";
	import FXParameterWindow from "./modules/parameterWindows/FXParameterWindow.svelte";
	import MetaParameterWindow from "./modules/parameterWindows/MetaParameterWindow.svelte";

	export let GourceCommand = "gource ";
</script>

<svelte:options accessors={true}>
</svelte:options>


<div class="row">
	<div class="column">
		<MainParameterWindow/>
		<UserParameterWindow/>
	</div>
	<div class="column">
		<FileParameterWindow/>
		<FXParameterWindow/>
	</div>
	<div class="column">
		<TextParameterWindow/>
		<MetaParameterWindow/>
	</div>
	<div class="column">
		<p id="gourcecommand">Command: {GourceCommand}</p> <CopyButton/>
	</div>
</div>





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

	p {
		font-family: 'OCR A', cursive;
	}
</style>