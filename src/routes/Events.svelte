<script>
window.onbeforeunload = function() { 
    window.setTimeout(function () { 
        window.location = 'AAA.jsp';
    }, 0); 
    window.onbeforeunload = null; // necessary to prevent infinite loop, that kills your browser 
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