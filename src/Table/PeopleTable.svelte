<script>
    import TableHead from "./TableHead.svelte";
    import TableRow from "./TableRow.svelte";
    import { faker } from '@faker-js/faker';
    faker.setLocale('nb_NO')

    function getPerson() {
        let name = faker.name.findName()
        return {    
            name : name,
            email: faker.internet.email(name),
            avatar: faker.internet.avatar('50x50'),        
            username: faker.internet.userName(name),
        }
    }
</script>

<table>
<TableHead person = {getPerson()}/>

{#each Array(4) as _, i}
    <TableRow person = {getPerson()}/>
{/each}

</table>

<style>
    table {
        width:60%;
        padding: 10px;
        margin:auto;
    }
</style>