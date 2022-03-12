<script>
    // export let name = "John Doe";
    // export let email = "johndoe@gmail.com";
    // export let avatar = "https://cloudflare-ipfs.com/ipfs/Qmd3W5DuhgHirLHGVixi6V76LhCkZUz6pnFt5AJBiyvHye/avatar/936.jpg";
    export let person;
</script>

<tr>
    {#each Object.keys(person) as key}
        {#if key === 'avatar'}
        <td>
            <img src={person.avatar} alt="">
        </td>
        {:else}    
        <td>{person[key]}</td>
        {/if}
    {/each}
</tr>

<style>
    td {
        padding: 12px;
    }
    img {
        width:100px;
        height:100px;
    }
</style>
