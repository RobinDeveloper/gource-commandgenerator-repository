<script>
    import app from "../main";

    function copyStringToClipboard (str) {
        // Create new element
        var el = document.createElement('textarea');
        // Set value (string to be copied)
        el.value = str;
        // Set non-editable to avoid focus and move outside of view
        el.setAttribute('readonly', '');
        el.style = {position: 'absolute', left: '-9999px'};
        document.body.appendChild(el);
        // Select text inside element
        el.select();
        // Copy text to clipboard
        document.execCommand('copy');
        // Remove temporary element
        document.body.removeChild(el);
    }

    function ButtonClicked()
    {
        copyStringToClipboard(app.GourceCommand.toString());
    }
</script>

<button on:click="{ButtonClicked}">Copy command to clipboard</button>

<style>
    button {
        font-family: 'OCR A', cursive;
    }
</style>