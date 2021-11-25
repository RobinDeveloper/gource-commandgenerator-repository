<script>
    import app from "../main";

    export let Text;

    function HandleClick(){
        app.GourceCommand += Text + " ";
    }

</script>

<button on:click={HandleClick}> add {Text}</button>