<script>
  import DogIcon from '../Components/DogIcon.svelte'
</script>

<header>
  <DogIcon on:get-dog />
</header>

<style>
  header {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 25%;
    background: #70e1f5;
    background: linear-gradient(to right, #ffd194, #70e1f5);
    box-shadow: 0px 2px 10px 2px rgba(51, 51, 51, 0.2);
    box-sizing: border-box;
  }
</style>
