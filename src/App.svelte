<script>
  import { Router, Link, Route } from "svelte-routing";
  import Home from "./pages/Home.svelte";
  import About from "./pages/About.svelte";
  import Contact from "./pages/Contact.svelte";

  export let url = "";
</script>

<main>
  <Router url="{url}">
    <nav>
      <Link to="/">Home</Link>
      <Link to="about">About</Link>
      <Link to="contact">Contact</Link>
    </nav>
    <div>
      <Route path="contact" component="{Contact}" />
      <Route path="about" component="{About}" />
      <Route path="/"><Home /></Route>
    </div>
  </Router>
</main>

