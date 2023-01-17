<script>
	import Header from '../widget/Header.svelte';
	import Footer from '../widget/Footer.svelte';
	import Banner from '../widget/Banner.svelte';
	import './styles.css';
	import './index.css';
</script>

<div class="app container bg-white shadow">
	<div class="row">
	<Banner/>
	<Header />
	<main class="col-md-10 p-3 col-10 fixed">
		<slot />
	</main>
		</div>
<Footer/>
</div>