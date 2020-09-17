<script>
  import { onMount } from 'svelte';

  export let name = 'loading';

  export let accounts = {};

  onMount(() => {
    accounts = {
      shonenada: {
        homepage: 'https://shonenada.com',
        github: 'https://github.com/shonenada',
      }
    }
  });
</script>

<ul>
  <li>Name: <span class="text-gray-600">{name}</span></li>
  <li>Homepage: <span class="text-gray-600">{accounts[name] && accounts[name].homepage}</span></li>
  <li>GitHub: <span class="text-gray-600">{accounts[name] && accounts[name].github}</span></li>
</ul>
