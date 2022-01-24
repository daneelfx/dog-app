<script>
  import { createEventDispatcher } from 'svelte'

  const dispatch = createEventDispatcher()
</script>

<p on:click={() => dispatch('get-dog')}>
  <i class="ph-paw-print" />
</p>

<style>
  p {
    background-color: #333;
    border-radius: 50%;
    padding: 16px;
    box-shadow: 0px 2px 10px 2px rgba(51, 51, 51, 0.5);
  }

  p > i {
    font-weight: 800;
    font-size: 8rem;
    color: white;
  }

  p:hover {
    transform: scale(1.2);
    transition: all 0.2s;
    cursor: pointer;
  }
</style>
