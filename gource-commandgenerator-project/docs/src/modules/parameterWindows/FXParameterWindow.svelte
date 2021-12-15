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

<div on:click={handleMouseClick}>
    {#if (hovered)}
        <Box>
            <NumberedParameter Text="--background-colour" Placeholder="hex value"/><br>
            <NumberedParameter Text="--background-image" Placeholder="path to image"/><br>
            <NumberedParameter Text="--padding" Placeholder="input padding value"/><br>
            <NumberedParameter Text="--bloom-multiplier" Placeholder="multiplier value"/><br>
            <NumberedParameter Text="--bloom-intensity" Placeholder="intensity value"/><br>
            <NumberedParameter Text="--elasticity" Placeholder="value"/>
            <Parameter Text="--disable-auto-rotate"/><br>
            <Parameter Text="--colour-images"/><br>
            <Parameter Text="--no-vsync"/><br>
        </Box>
    {:else }
        <Box>
            <p style="text-align: center; margin-top: 10em ">fx parameters</p>
        </Box>
    {/if}
</div>

<style>
    p {
        font-family: 'OCR A', cursive;
    }
</style>