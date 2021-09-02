<script lang="ts">
	import { Router, Route, Link } from "svelte-routing";
	import Footer from "./Components/Footer.svelte";

	import Navbar from "./Components/Navbar.svelte";

	import About from "./Pages/About.svelte";
	import Contact from "./Pages/Contact.svelte";
	import Cost from "./Pages/Cost.svelte";
	import Endapp from "./Pages/Endapp.svelte";
	import Faq from "./Pages/Faq.svelte";
	import Home from "./Pages/Home.svelte";
	import Material from "./Pages/Material.svelte";
	import NotFound from "./Pages/NotFound.svelte";
	import Sustainability from "./Pages/Sustainability.svelte";

	export let url = "";
</script>

<main>
	<Router {url}>
		<Navbar />
		<Route path="confirm-account" component={Sustainability} />
		<Route path="/contact" component={Contact} />
		<Route path="/faq" component={Faq} />
		<Route path="/about" component={About} />
		<Route path="/endapp" component={Endapp} />
		<Route path="/material" component={Material} />
		<Route path="/cost" component={Cost} />
		<Route path="/" component={Home} />
		<Route component={NotFound} />
	</Router>
</main>

<style>
</style>
