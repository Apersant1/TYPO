<script>
  import { Carta, CartaEditor } from 'carta-md';
  import { math } from '@cartamd/plugin-math';
	import 'carta-md/default.css'; /* Default theme */
	import 'carta-md/light.css'; /* Markdown input theme */
  import 'katex/dist/katex.css';
  


  const carta = new Carta({
		extensions:[math()]
	});

	let value = '';
</script>

<main class="container">
  <h1>Welcome to TYPO!</h1>
  <CartaEditor {carta} bind:value />



</main>

<style>
 
  
  /* Set your custom monospace font */
	:global(.carta-font-code) {
		font-family: '...', monospace;
	}
</style>
