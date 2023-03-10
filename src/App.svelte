<script>
  import { afterUpdate } from 'svelte';
  import svelteLogo from './assets/svelte.svg'
  import CardPrice from './lib/Card-Price.svelte';
  import redstone from "redstone-api"
    import { compute_rest_props } from 'svelte/internal';

  let tokenlist = [];
  afterUpdate(async () => {
    // @ts-ignore
    const tokens = await redstone.getAllPrices();

    tokenlist = Object.values(tokens)
    console.log(typeof tokenlist)
    console.log(tokenlist)
  });
</script>

<main>
  <div>
    {#each tokenlist as token}
      <CardPrice token={token} />
    {/each}
  </div>
</main>

