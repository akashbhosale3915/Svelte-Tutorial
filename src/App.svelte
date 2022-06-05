<script>
  import { Route, Router } from "svelte-routing";

  import Navbar from "./components/Navbar.svelte";
  import About from "./pages/About.svelte";
  import Contact from "./pages/contact.svelte";
  import Home from "./pages/Home.svelte";
</script>

<Router>
  <Navbar />
  <div class="dynamic">
    <Route path="/" component={Home} />
    <Route path="about" component={About} />
    <Route path="contact" component={Contact} />
  </div>
</Router>

<style>
  .dynamic {
    padding: 0 2rem;
  }
</style>
