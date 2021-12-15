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
            <NumberedParameter Text="--follow-user" Placeholder="enter username"/><br>
            <NumberedParameter Text="--highlight-user" Placeholder="enter username"/><br>
            <NumberedParameter Text="--max-user-speed" Placeholder="enter units"/><br>
            <NumberedParameter Text="--user-friction" Placeholder="enter seconds"/><br>
            <NumberedParameter Text="--user-scale" Placeholder="enter scale"/><br>
            <Parameter Text="--highlight-users"/><br>
        </Box>
    {:else }
        <Box>
            <p style="text-align: center; margin-top: 10em ">User parameters</p>
        </Box>
    {/if}
</div>

<style>
    p {
        font-family: 'OCR A', cursive;
    }
</style>