<script>
import NumberedParameter from "../NumberedParameter.svelte";
import Parameter from "../Parameter.svelte";
import Box from "../Box.svelte";

</script>

<Box>
<NumberedParameter  Text="--title" Placeholder="enter title"/><br>
<NumberedParameter Text="--path" Placeholder="enter path to git repository"/><br>
<NumberedParameter Text="--viewport" Placeholder="enter resolution widthxheight"/><br>

<Parameter Text="--fullscreen"/><br>
<Parameter Text="--transparent"/><br>
<Parameter Text="--loop"/><br>
<Parameter Text="--frameless"/><br>
</Box>