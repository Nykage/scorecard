<script>
</script>

<div class="welcome-text">
    <p class="welcome-text-title">Login</p>
</div>

<div class="form-container">
    <form action="http://localhost/scorecard/back/login.php" method="post">
        <span class="title">E-mail:</span> <br><input type="email" name="email"><br>
        <span class="title">Password:</span> <br><input type="password" name="password"><br>
        <input type="submit" value="Submit">
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