<script>
  export let token;

  const detail = () => {
    alert(`Token name: ${token.symbol}. Token price: $${token.value}`);
  } 
</script>

<!-- svelte-ignore a11y-click-events-have-key-events -->
<div
  on:click={detail}
  style="display: flex; gap: 5px;cursor: pointer;"
>
  <div>{token.symbol}</div>
  <div>${token.value}</div>
</div>
