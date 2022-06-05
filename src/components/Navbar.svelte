<script>
  import { Link } from "svelte-routing";
</script>

<nav>
  <ul>
    <li><Link to="/">Home</Link></li>
    <li><Link to="/about">About</Link></li>
    <li><Link to="/contact">Contact</Link></li>
  </ul>
</nav>

<style>
  nav {
    width: 100%;
    height: 50px;
    background: #333;
    color: white;
    display: flex;
    justify-content: center;
    align-items: center;
    position: sticky;
    top: 0;
    left: 0;
    box-shadow: 5px 5px 20px rgba(0, 0, 0, 0.5);
  }

  ul {
    list-style: none;
    display: flex;
  }

  ul li {
    padding: 0 15px;
    cursor: pointer;
    transition: 0.5s all ease;
  }
</style>
