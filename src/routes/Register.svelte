<script>
	if (performance.navigation.type == 1) {
		console.info( "This page is reloaded" );
		window.location.replace("https://scorecard-piia.netlify.app/");
	} else {
		console.info( "This page is not reloaded");
	}
</script>

<div class="welcome-text">
    <p class="welcome-text-title">Register</p>
</div>

<div class="form-container">
    <form action="https://scorecard-backend.truudeli15.net/back/create-user.php" method="post">
        <span class="title">First Name:</span> <br><input type="text" name="first_name"><br>
        <span class="title">Last Name:</span> <br><input type="text" name="last_name"><br>
        <span class="title">Password:</span> <br><input type="password" name="password"><br>
        <span class="title">E-mail:</span> <br><input type="email" name="email"><br>
        <input type="submit" value="Submit">
        <input type="text" name="user_type" value="user" style="visibility: hidden; margin: 0; padding: 0;">
    </form>
</div>

<style>
.welcome-text {
    text-align: center;
    color: #8372e6;
    font-size: 35px;
    margin-bottom: 3rem;
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

.form-container {
    max-width: 750px;
    display: flex;
    margin: 0 auto;
    justify-content: flex-start;
    align-items: center;
    margin-bottom: 3rem;
}

.title {
    text-align: center;
    color: #8372e6;
    font-size: 35px;
    margin-bottom: 4rem;
    text-align: center;
}
    
input[type=text] {
    width: 750px;
    padding: 12px 20px;
    margin: 8px 0;
    box-sizing: border-box;
}

input[type=email] {
    width: 750px;
    padding: 12px 20px;
    margin: 8px 0;
    box-sizing: border-box;
}

input[type=password] {
    width: 750px;
    padding: 12px 20px;
    margin: 8px 0;
    box-sizing: border-box;
}

input[type=submit] {
    width: 750px;
    padding: 12px 20px;
    margin: 8px 0;
    box-sizing: border-box;
    background-color: #8372e6;
    color: white;
    font-size: 25px;
}

input[type=submit]:hover {
    cursor: pointer;
}

@media all and (max-width: 400px) {
    .form-container {
        max-width: 250px;
        display: flex;
        margin: 0 auto;
        justify-content: flex-start;
        align-items: center;
        margin-top: 7rem;
    }
    
    .title {
        text-align: center;
        color: #8372e6;
        font-size: 35px;
        margin-bottom: 4rem;
        text-align: center;
    }
    
    input[type=text] {
        width: 250px;
        padding: 12px 20px;
        margin: 8px 0;
        box-sizing: border-box;
    }
        
    input[type=email] {
        width: 250px;
        padding: 12px 20px;
        margin: 8px 0;
        box-sizing: border-box;
    }
    
    input[type=password] {
        width: 250px;
        padding: 12px 20px;
        margin: 8px 0;
        box-sizing: border-box;
    }
    
    input[type=submit] {
        width: 250px;
        padding: 12px 20px;
        margin: 8px 0;
        box-sizing: border-box;
        background-color: #8372e6;
        color: white;
        font-size: 25px;
    }    
}
</style>