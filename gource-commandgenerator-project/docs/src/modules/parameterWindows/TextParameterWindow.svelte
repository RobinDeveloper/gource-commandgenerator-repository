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
            <NumberedParameter Text="--font-scale" Placeholder="enter scale"/><br>
            <NumberedParameter Text="--font-size" Placeholder="enter font size"/><br>
            <NumberedParameter Text="--file-font-size" Placeholder="enter font size"/><br>
            <NumberedParameter Text="--dir-font-size" Placeholder="enter font size"/><br>
            <NumberedParameter Text="--user-font-size" Placeholder="enter font size"/><br>
            <NumberedParameter Text="--font-colour" Placeholder="font colour hex value"/><br>
        </Box>
    {:else }
        <Box>
            <p style="text-align: center; margin-top: 10em ">Text parameters</p>
        </Box>
    {/if}
</div>

<style>
    p {
        font-family: 'OCR A', cursive;
    }
</style>