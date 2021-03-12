<template>
	<v-app id="app">
		<Header/>
		<Menu/>
		<Content/>
	
		
	</v-app>
</template>

<script>
import Header from './components/Header'
import Menu from './components/template/Menu'
import Content from './components/template/Content'
export default {
	components: {Header, Menu, Content},
	created() {
		this.$store.dispatch('initStocks')
	}

}
</script>

<style>

body {
		margin: 0;
	}
	#app {
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;

		height: 100vh;
		display: grid;
		grid-template-rows: 60px 1fr 40px;
		grid-template-columns: 300px 1fr;
		grid-template-areas:  
			'header header'
			'menu content'
			

	}

</style>

