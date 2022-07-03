<script>
    let users = [{id:1,name:"Nijin Nazar",age:21},{id:2,name:"Abhishek",age:25},{id:3,name:'Aswin',age:19}]
</script>

<ul>
    {#each users as user }
    <li>{user.id}. {user.name} of age {user.age}</li>
    {/each}
</ul>

<style>
    ul {
        list-style-type: none;
        font-size: 24px;
        line-height: 50px;
    }
</style>