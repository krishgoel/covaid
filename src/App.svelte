<script>

	// Routing 
	import router from "page"
	let page;
	
	import Index from './routes/Index.svelte'
	import About from './routes/About.svelte'
	import Volunteer from './routes/Volunteer.svelte'
	
	router('/', () => (page = Index))
	router('/about', () => (page = About))
	router('/volunteer', () => (page = Volunteer))
	
	router.start()

	import Nav from "../components/Nav.svelte"
	import Footer from "../components/Footer.svelte"

</script>

<Nav/>

<svelte:component this="{page}"/>

<Footer/>