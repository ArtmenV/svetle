<script>
let name = "Svetle"

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
</style>

<h1>{name}</h1>
<h2>{upperName}</h2>
<h2>{lowerName}</h2>

<button on:click={changeName}>Change Name</button>

