<script>
  import { Router, Route } from 'svelte-routing';
  import Nav from './components/Nav';
  import Account from './routes/Account';
  import Index from './routes/Index';

  export let url;
</script>

<Router url={url}>
  <Nav />
  <hr class="color-gray-500"/>
  <Route path="/"><Index /></Route>
  <Route path="/users/:name" component={Account} let:params />
  <Route>Not Found</Route>
</Router>

