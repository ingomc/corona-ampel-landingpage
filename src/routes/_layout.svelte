<script>
	import Header from '../components/Header.svelte';
	import Footer from '../components/Footer.svelte';
  import Matomo from '../components/Matomo.svelte';

	// export let segment;
</script>

<style>

</style>

<Header/>

	<main>
		<slot></slot>
	</main>

<Footer />


<Matomo />
