<script>
let name = "Svetle";

let counter = 0;

$: counterClass = counter % 2 === 0 ? 'red' : 'blue'

$: upperName = name.toUpperCase();
$: lowerName = name.toLowerCase();

function changeName() {
	name= 'New name'
}

first: for (let i=0; i < 5; i++) {
	if (i % 2 === 0) {
	continue first;
	}
}
</script>

<style>
	h1 {
		color: purple;
	}
	.blue {
		color: blue
	}
	.red {
		color: red;
	}
</style>

<h1>{name}</h1>
<h2>{upperName}</h2>
<h2>{lowerName}</h2>

<button on:click={changeName}>Change Name</button>


<h1 class={counterClass}>Counter {counter}</h1>
<button on:click={() => counter++}>Add one to counter</button>
