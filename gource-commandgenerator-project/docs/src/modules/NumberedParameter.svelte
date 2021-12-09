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