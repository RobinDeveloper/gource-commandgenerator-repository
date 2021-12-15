<script>
    import NumberedParameter from "../NumberedParameter.svelte";
    import Parameter from "../Parameter.svelte";
    import Box from "../Box.svelte";

    let hovered = false;

    function handleMouseClick(e) {
        hovered = !hovered;
    }
</script>

<div on:click={handleMouseClick}>
    {#if (hovered)}
        <Box>
            <NumberedParameter Text="--font-file" Placeholder="font path"/><br>
            <NumberedParameter Text="--filename-colour" Placeholder="hex value"/><br>
            <NumberedParameter Text="--dir-colour" Placeholder="hex value"/><br>
            <NumberedParameter Text="--filename-time" Placeholder="seconds"/><br>
            <NumberedParameter Text="--max-files" Placeholder="max file count"/><br>
            <Parameter Text="--file-extensions"/><br>
            <Parameter Text="--file-extension-fallback"/><br>
            <Parameter Text="--key"/><br>
            <Parameter Text="--log-command VCS"/><br>
            <Parameter Text="--log-format VCS"/><br>
        </Box>
    {:else }
        <Box>
            <p style="text-align: center; margin-top: 10em ">File parameters</p>
        </Box>
    {/if}
</div>

<style>
    p {
        font-family: 'OCR A', cursive;
    }
</style>