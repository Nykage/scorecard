<script>
	if (performance.navigation.type == 1) {
		console.info( "This page is reloaded" );
		window.location.replace("https://scorecard-piia.netlify.app/");
	} else {
		console.info( "This page is not reloaded");
	}
</script>

<div class="welcome-text">
    <p class="welcome-text-title">Choose an Event!</p>
    <p>
        On the navigation bar you will find the <b>League</b> and <b>Ranking</b> buttons.
    </p>
    <p>
        Pressing any of those buttons will direct you to the list of events of each category.
        <br>
        You need to sign up or log in to participate.
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