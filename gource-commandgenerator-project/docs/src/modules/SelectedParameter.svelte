<!--

<script>
    import Select from 'svelte-select';
    import app from "../main";

    export let Text;
    const Items = ['One', 'Two', 'Three'];
    const Selected = 'track';
    function HandleClick(){
        app.GourceCommand += Text + " " + Selected + " ";
    }
</script>

<style>
    .themed {
        --border: 3px solid lightgray;
        --borderRadius: 10px;
        --placeholderColor: gray;
    }
</style>

<div class="themed">
    <button on:click={HandleClick}>Add {Text}</button>
    <Select {Items} {Selected}></Select>
</div>

-->

<script>
    import Select from 'svelte-select';
    import app from "../main";

    export let Text;
    const items = ['Track', 'Overview'];
    let selectedValue = "Track";
    let Selected = "Track";

    function HandleClick(){
        app.GourceCommand += Text + " " + Selected + " ";
    }

    function HandleSelect(event){
        console.log('selected item', event.detail);
        Selected = event.detail.value;
    }
</script>

<style>
    .themed {
        --border: 3px solid lightgray;
        --borderRadius: 10px;
        --placeholderColor: gray;
    }

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

    Select {
        font-family: 'OCR A', cursive;
    }
</style>

<div class="themed">
    <button on:click={HandleClick}> add {Text}</button>
    <Select {items} {selectedValue} on:select={HandleSelect}></Select>
</div>
