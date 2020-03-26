<script>

  let list = [
    {
      "name": "Page 1",
      "url": "/"
    },
    {
      "name": "Page 2",
      "url": "/page-2"
    },
    {
      "name": "Page 3",
      "url": "/page-3"
    }
  ]
</script>

<nav>
    <ul>
        {#each list as item}
            <li><a href={item.url}>{item.name}</a></li>
        {/each}
    </ul>
</nav>
