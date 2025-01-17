<script>
	import Navbar from './components/Navbar.svelte';
	import Footer from './components/Footer.svelte';
	import Home from './components/Home.svelte';
	import About from './components/About.svelte';
	import Events from './components/Events.svelte';
	import Team from './components/Team.svelte';
  
	let currentPage = 'home';
  
	function setPage(event) {
	  currentPage = event.detail;
	}
  </script>
  
  <style>
	.container {
	  display: flex;
	  flex-direction: column;
	  height: 100vh;
	}
	.content {
	  flex: 1;
	}
  </style>
  
  <div class="container">
	<Navbar on:changePage={setPage} />
	<div class="content">
	  {#if currentPage === 'home'}
		<Home />
	  {:else if currentPage === 'about'}
		<About />
	  {:else if currentPage === 'events'}
		<Events />
	  {:else if currentPage === 'team'}
		<Team />
	  {/if}
	</div>
	<Footer />
  </div>
  