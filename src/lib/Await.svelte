<script>
   let todos = []
 

  const fetchData = async () => {
    todos = await  fetch('https://jsonplaceholder.typicode.com/todos')
  .then(response => response.json())
  .then(json => json )
  }
</script>

<button on:click={fetchData}>Fetch Data</button>

{#await todos}
<p>Waiting</p>
{:then todos}
{#each todos as todo }
<p>{todo.title}</p>
{/each}
{:catch error}
<p style="color:red">Error Fetching {error}</p>
{/await}