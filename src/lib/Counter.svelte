<script>
  import redstone from "redstone-api";

  let count = 0;
  const increment = async () => {
    const prices = await redstone.getAllPrices();

    console.log(prices); // Example output below
  };
</script>

<button on:click={increment}>
  count is {count}
</button>
