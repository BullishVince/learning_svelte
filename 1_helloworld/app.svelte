<script>
	import Age from './Age.svelte';
	let name = 'world';
	let age = 27;
	$: dogYears = age * 7;

	function add(){
		age += 1;
	}
	
	function subtract(){
		age -= 1;
	}
	
</script>

<style>
	:global(h1) {
		color: maroon;
		font-size: 32px;
	}
</style>

<h1>Hello {name}!</h1>
<Age {age}/>
<Age age={dogYears} yearType='dog'/>

<button on:click={add}>+</button>
<button on:click={subtract}>-</button>