<script>
  import Header from './Containers/Header.svelte'
  import DogGrid from './Containers/DogGrid.svelte'

  let dogs = []

  const fetchDog = async () => {
    const response = await fetch('https://dog.ceo/api/breeds/image/random')
    const { message: dogURL } = await response.json()
    dogs = [dogURL, ...dogs]
  }
</script>

<Header on:get-dog={() => fetchDog()} />
<DogGrid {dogs} />
