<script>
  import { onMount } from "svelte";
  let res = [];
  let someres = [];
  onMount(async () => {
    const response = await fetch("https://jsonplaceholder.typicode.com/posts");
    res = await response.json();
    someres = res.slice(0, 5);
  });

  export let location;
</script>

<div class="home">
  {#each someres as post}
    <div class="post">
      <h3>{post.title}</h3>
      <h5>{post.body}</h5>
    </div>
  {/each}
</div>

<style>
  .post {
    margin: 15px auto;
    box-shadow: 0px 5px 20px rgba(0, 0, 0, 0.2);
    border-radius: 8px;
    padding: 10px;
  }

  .post h3 {
    margin-bottom: 10px;
    text-transform: capitalize;
  }
</style>
