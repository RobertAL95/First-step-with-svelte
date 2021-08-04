<script>
  const movies = [
    { name: "Avengers", available: 5, quantity: 0 },
    { name: "Wonder Woman", available: 15, quantity: 0 }
  ];
</script>

{#each movies as movie}
<form>
	<h3>{movie.name}</h3>
	<button type="button" on:click={() => movie.quantity--} disabled={movie.quantity <= 0}>-</button>
	{movie.quantity}
	<button type="button" on:click={() => movie.quantity++} disabled={!(movie.quantity < movie.available)}>+</button>
</form>
{/each}