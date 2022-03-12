<script>
    export let person;
</script>

<tr>
    {#each Object.keys(person) as key}
        <th>{key.toUpperCase()}</th>
    {/each}
</tr>

<style>
    tr {
        padding: 12px;
    }
</style>