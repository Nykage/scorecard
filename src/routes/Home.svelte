<script>
	if (performance.navigation.type == 1) {
		console.info( "This page is reloaded" );
		window.location.replace("https://scorecard-piia.netlify.app/");
	} else {
		console.info( "This page is not reloaded");
	}
</script>

<div class="welcome-text">
    <p class="welcome-text-title">Welcome to Scorecard!</p>
    <p>
        Here you can place bets for fun on various events.
    </p>
    <p>
        Test your estimating skills now! Register and place a bet.
        <br>
        You will get points based on how well you did.
    </p>
    <p>
        <b>Join now and place a bet!</b>
    </p>
</div>

<style>
.welcome-text {
    text-align: center;
    color: #8372e6;
    font-size: 35px;
    margin-bottom: 4rem;
}

.welcome-text .welcome-text-title {
    text-align: center;
    color: #8372e6;
    font-size: 75px;
    margin-bottom: 10px;
}

.welcome-text p {
    margin-bottom: 0px;
}

@media all and (max-width: 400px) {
    .welcome-text {
        text-align: center;
        color: #8372e6;
        font-size: 20px;
        margin-bottom: 4rem;
    }

    .welcome-text .welcome-text-title {
        text-align: center;
        color: #8372e6;
        font-size: 60px;
        margin-bottom: 10px;
    }

    .welcome-text p {
        margin-bottom: 0px;
    }
}
</style>