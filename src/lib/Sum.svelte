<script>
    let numbers = [1, 2, 3, 4];

	function addNumber() {
		numbers = [...numbers,numbers.length + 1]
	}

	$: sum = numbers.reduce((t, n) => t + n, 0);

</script>

<button on:click={addNumber}>Add a Number</button>
<p> {numbers.join(' + ')} = {sum} </p>