<script>
import NumberedParameter from "../NumberedParameter.svelte";
import Parameter from "../Parameter.svelte";
import Box from "../Box.svelte";
import SelectedParameter from "../SelectedParameter.svelte";

let hovered = false;

function handleMouseClick(e) {
    hovered = !hovered;
}

</script>

<div  on:click={handleMouseClick}>
{#if (hovered)}
    <Box>
    <NumberedParameter  Text="--title" Placeholder="enter title"/><br>
    <NumberedParameter Text="--path" Placeholder="enter path to git repository"/><br>
    <NumberedParameter Text="--viewport" Placeholder="enter resolution widthxheight"/><br>

    <Parameter Text="--fullscreen"/><br>
    <Parameter Text="--transparent"/><br>
    <Parameter Text="--loop"/><br>
    <Parameter Text="--frameless"/><br>
    <SelectedParameter Text="--camera-mode"/><br>
    </Box>
{:else }
    <Box>
        <p style="text-align: center; margin-top: 10em ">Main parameters</p>
    </Box>
{/if}
</div>

<style>
    p {
        font-family: 'OCR A', cursive;
    }
</style>