<script>
	import { Router, Link, Route } from "svelte-routing";
	import { link } from "svelte-routing";
	import Home from "./routes/Home.svelte";
	import Login from "./routes/Login.svelte";
	import Register from "./routes/Register.svelte";
	import Events from "./routes/Events.svelte";
	import Ranking from "./routes/Ranking.svelte";
	import League from "./routes/League.svelte";

	export let url = "";
</script>

<Router url="{url}">
<nav>
	<ul>
		<li><a href="/" use:link>Home</a></li>
		<li><a href="league" use:link>League</a></li>
		<li><a href="ranking" use:link>Ranking</a></li>
		<li><a href="login" use:link>Login</a></li>
		<li><a href="register" use:link>Register</a></li>
	</ul>
</nav>
</Router>

<div class="hero-image">
	<div class="hero-text">
		<span class="title">Scorecard</span>
		<br>
		<span><a href="events" use:link>Place Your Bet</a></span>
	</div>
</div>

<div class="mobile-title">
	Scorecard
</div>

<div class="wrapper">
<Router url="{url}">
	<Route path="events" component="{Events}" />
	<Route path="login" component="{Login}" />
	<Route path="register" component="{Register}" />
	<Route path="/"><Home /></Route>
    <Route path="league" component="{League}" />
    <Route path="ranking" component="{Ranking}" />
</Router>
</div>

<nav style="margin-bottom: 0rem; background-color: rgb(125, 125, 125); color: lightgrey">
	<ul>
		<li>About</li>
		<li>Contact</li>
	</ul>
</nav>

<style>
	.mobile-title {
		display: hidden;
		font-size: 0;
		margin: 0;
		padding: 0;
	}

	a {
		text-decoration: none;
		color: black;
	}

	nav {
		font-size: 2rem;
		background-color: #f1f1f1;
	}

	nav ul {
		list-style-type: none;
		margin: 0;
		padding: 0;
		align-items: center;
		display: flex;
	}

	nav ul li {
		cursor: pointer;
		padding: 1rem;
		flex: auto;
		text-align: center;
	}

	nav ul li:hover {
		background-color: #555;
		color: white;
	}

	nav ul li:hover > a {
		color: white;
	}

	@media all and (max-width: 750px) {
		nav {
			font-size: 2rem;
			margin-bottom: 3rem;
			background-color: rgb(125, 125, 125);
			color: lightgrey
		}

		nav ul {
			flex-direction: column;
		}

		nav ul li {
			text-align: center;
		}

		a {
			text-decoration: none;
			color: lightgrey;
		}

		nav ul li:hover {
			background-color: #555;
			color: lightgrey;
		}

		nav ul li:hover > a {
			color: lightgrey;
		}

		.hero-image {
			display: none;
		}

		.mobile-title {
			display: visible;
			color: #8372e6;
			text-align: center;
			font-size: 70px;
		}
	}

	.hero-image {
		background-image: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url('/img/hero-image.png');
		height: 75%;
		background-position: center;
		background-repeat: no-repeat;
		background-size: cover;
		position: relative;
		margin-bottom: 3rem;
	}

	.hero-text {
		text-align: center;
		position: absolute;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);
		color: white;
	}

	.hero-text .title {
		font-size: 110px;
	}

	.hero-text span {
		font-size: 50px;
		text-shadow: 0px 0px 8px rgba(0, 0, 0, 0.85);
	}

	.hero-text span a {
		color: #b6a9fd;
		text-decoration: none;
	}

	.wrapper {
		width: 100%;
		padding: 40px 0;
		background-color: rgb(241, 239, 239);
		margin-bottom: 3rem;
	}


</style>