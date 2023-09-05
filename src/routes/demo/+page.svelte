<script>
  let count = 0

  $: if (count >= 10) {
    count = 9
    alert('You have reached the limit')
  }
</script>

<span>Count is: {count}</span>
<button on:click={() => count++}>Increment</button>