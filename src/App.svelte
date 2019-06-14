<script>
	export let name;

	function changeNameHandler() {
		name = "Changed Name"
	}
</script>

<style>
	h1 {
		color: purple;
	}
</style>

<h1>{name}!</h1>
<button on:click={changeNameHandler}>Change Name</button>
