<script>
	let name = "Person"
	let num = 0
	let num2 = 0
	let whatOperator = 0
	let button = 0

	function insertNumber(x){
		button = x
		num = num.toString()
		num = num + button.toString()
		num = parseInt(num)
	}
	function operator(x){
		num2 = num
		num = 0
		whatOperator = x
	}
	function doMaths(){
		if (whatOperator === 1) {
			num = num2 + num
		}
		if (whatOperator === 2) {
			num = num2 - num
		}
		if (whatOperator === 3) {
			num = num2 * num
		}
		if (whatOperator === 4) {
			num = num2 / num
		}
		if (whatOperator === 5) {
			num = Math.pow(num2, num)
		}
	}
	function allClear() {
		num = 0 
		num2 = 0
	}
</script>

<main>
	<h1>Hello {name}!</h1>
	<h2>Welcome to the two number calculator</h2>
	<h3>You can only use two numbers so choose wisely</h3>
	<p>Your answer is {num}</p>
	<button on:click={() => insertNumber(1)}>1</button>
	<button on:click={() => insertNumber(2)}>2</button>
	<button on:click={() => insertNumber(3)}>3</button>
	<button on:click={() => insertNumber(4)}>4</button>
	<button on:click={() => insertNumber(5)}>5</button>	
	<button on:click={() => insertNumber(6)}>6</button>
	<button on:click={() => insertNumber(7)}>7</button>
	<button on:click={() => insertNumber(8)}>8</button>
	<button on:click={() => insertNumber(9)}>9</button>
	<button on:click={() => insertNumber(0)}>0</button>
	<button on:click={() => operator(1)}>+</button>
	<button on:click={() => operator(2)}>-</button>
	<button on:click={() => operator(3)}>*</button>
	<button on:click={() => operator(4)}>/</button>
	<button on:click={() => operator(5)}>^</button>
	<button on:click={doMaths}>=</button>
	<button on:click={allClear}>AC</button>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>