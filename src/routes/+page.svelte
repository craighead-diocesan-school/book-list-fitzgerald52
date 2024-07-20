<script>
  let books = [
    { name: 'harry potter', read: 'false' },
    { name: 'harry potter 2', read: 'false' },
  ]

  let Read = false
  // adds book as and object to array saying the name and that the book has not been read
  function addbooks() {
    books = [...books, { name: '', Read: false }]
  }
</script>

<main>
  <button on:click={addbooks}> Add new book</button>

  {#each books as book, index}
    <div class="bookread">
      <input bind:value={books[index].name} />
      <input type="checkbox" bind:checked={books[index].Read} />
    </div>
  {/each}
</main>

<style>
  .book {
    display: block;
  }
</style>
