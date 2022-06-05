<script>
  import { onMount } from "svelte";

  let res = [];
  onMount(async () => {
    const response = await fetch("https://jsonplaceholder.typicode.com/posts");
    res = await response.json();
  });
</script>

<main>
  {#each res as post}
    <div class="post">
      <h3>{post.title}</h3>
      <h5>{post.body}</h5>
    </div>
  {/each}
</main>

<style>
  .post {
    width: 80%;
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
