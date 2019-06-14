<script>
let name = "Svetle"

$: upperName = name.toUpperCase();
$: lowerName = name.toLowerCase();

function changeName() {
	name= 'New name'
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

