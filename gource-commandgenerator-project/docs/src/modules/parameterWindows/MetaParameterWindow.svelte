<script>
    import NumberedParameter from "../NumberedParameter.svelte";
    import Parameter from "../Parameter.svelte";
    import Box from "../Box.svelte";

    let hovered = false;

    function handleMouseClick(e) {
        hovered = !hovered;
    }

</script>

<div  on:click={handleMouseClick}>
    {#if (hovered)}
        <Box>
            <NumberedParameter Text="--start-date" Placeholder="YYYY-MM-DD hh:mm:ss +tz"/><br>
            <NumberedParameter Text="--stop-date" Placeholder="YYYY-MM-DD hh:mm:ss +tz"/><br>
            <NumberedParameter Text="--time-scale" Placeholder="scale value"/><br>
            <NumberedParameter Text="--logo" Placeholder="path"/><br>
            <NumberedParameter Text="--logo-offset" Placeholder="XxY"/><br>
            <NumberedParameter Text="--output-ppm-stream" Placeholder="path to stream"/><br>
            <NumberedParameter Text="--output-framerate" Placeholder="FPS"/><br>
        </Box>
    {:else }
        <Box>
            <p style="text-align: center; margin-top: 10em ">Meta parameters</p>
        </Box>
    {/if}
</div>

<style>
    p {
        font-family: 'OCR A', cursive;
    }
</style>