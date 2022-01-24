<script>
  import Card from '../Components/Card.svelte'
  export let dogs
</script>

<main>
  {#each dogs as dog (dog)}
    <Card>
      <img src={dog} alt={dog} />
    </Card>
  {:else}
    <p>There are no dogs. Please press the icon just above</p>
  {/each}
</main>

<style>
  main {
    height: 75%;
    display: flex;
    justify-content: center;
    align-items: flex-start;
    flex-flow: row wrap;
    padding-top: 20px;
    box-sizing: border-box;
  }

  img {
    max-width: 100%;
    max-height: 100%;
    border-radius: 2%;
    box-shadow: 0px 2px 10px 2px rgba(51, 51, 51, 0.4);
  }

  img:hover {
    transform: scale(2);
    transition: all 0.4s;
  }

  p {
    font-size: 2rem;
  }
</style>
