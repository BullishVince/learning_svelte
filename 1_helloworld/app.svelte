<script>
	import Age from './Age.svelte';
	let name = 'world';
	let age = 27;
	let dogYears = age * 7;
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

<button>+</button>
<button>-</button>