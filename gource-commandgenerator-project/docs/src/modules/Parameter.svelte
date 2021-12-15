<script>
    import app from "../main";

    export let Text;

    function HandleClick(){
        app.GourceCommand += Text + " ";
    }

</script>

<button on:click={HandleClick}> add {Text}</button>

<style>
    button {
        font-family: 'OCR A', cursive;
        transition-duration: 0.4s;
        background-color: white; /* Green */
        color: black;
    }

    button:hover {
        background-color: black; /* Green */
        color: white;
    }
</style>