<script>
    import app from "../main";

    export let Text;
    export let Placeholder = "Enter preferred value"
    let Number;

    function HandleClick(){
        app.GourceCommand += Text + " " + Number.toString() + " ";
    }

</script>

<button on:click={HandleClick}> add {Text}</button>
<input bind:value={Number} placeholder="{Placeholder}">

<style>
    button {
        font-family: 'OCR A', cursive;
        transition-duration: 0.4s;
        background-color: white;
        color: black;
    }

    button:hover {
        background-color: black; /* Green */
        color: white;
    }

    input {
        font-family: 'OCR A', cursive;
    }
</style>