<script>
  import { onMount } from 'svelte'
  export let message;
  onMount(async () => {
    let data = await (await fetch('/api')).json()
    message = data.msg
    console.log('MESSAGE: ', message)
  })
</script>

<style>
  h1 {
    color: purple;
  }
</style>

<h1>{message}</h1>
<h2>The Lord's Prayer</h2>
<p>Our Cage, who art thy savior,</p>
<p>Nicolas by thy name</p>
<p>The Lord of War will come,</p>
