<script>
    export let grade;
</script>

{#if grade > 90}
<p>You have A grade</p>
{:else if grade > 80 && grade < 90}
<p>You have B grade</p>
{/if}