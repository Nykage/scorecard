<script>
	import Games from './Games.svelte';


</script>

<div class="container">
<header>
	<h1>Your Games List</h1>
</header>
</div>
<div class="wrapper">
	<Games />
</div>

<style>
	.container {
		display: flex;
		justify-content: center;
		flex: 1 1 0;
		background-image: url("https://i.imgur.com/40mADzB.png");
	}

	header {
		text-align: center;
		padding: 1em;
		width: 1000px;
		display: flex;
		justify-content: center;
		color: #e8e6e6;
	}

	header h1 {
		padding: 35px;
		border-radius: 70px;
		font-size: 50px;
		background-color: #42474b;
		transition: 0.3s;
	}

	@media only screen and (max-width: 640px) {
		header h1 {
			padding: 25px;
			border-radius: 50px;
			font-size: 35px;
			background-color: #42474b;
		}
	}

	.wrapper {
		width: 100%;
		padding: 40px 0;
		background-color: rgb(241, 239, 239);
	}


</style>