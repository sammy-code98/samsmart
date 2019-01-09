# samsmart
just trying out some new stuff hmm
<?php
if(filter_has_var(INPUT_POST,'email')){
    if(filter_input(INPUT_POST, 'email', FILTER_VALIDATE_EMAIL)){
         echo 'email is valid';
    }else{
        echo 'email is not valid';
    }
    
   
}
?>



<!DOCTYPE html>
<html>

<head>
    <meta charset="utf-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <title>scripted form</title>
    <meta name="viewport" content="width=device-width, initial-scale=1 shrink-to-fit=no">
    <link rel="stylesheet" type="text/css" media="screen" href="form.css" />

</head>

<body>
    <div class="banner">
        <h3 id="sign">sign up </h3>

        <form  class="myform"  action="<?php echo $_SERVER['PHP_SELF']; ?>"    method="POST">

            <br>
            <input type="text" name="firstname"  placeholder="First Name">
            <br>
            <br>
            <input type="text" name="lastname"  placeholder="Last Name">
            <br>
            <br>
            <input type="email" name="email" placeholder=" Email">
            <br>
            <br>
            <input type="password" name="password" placeholder="Password">
            <br>
            <input type="password" name="password" placeholder="Confirm Password">
            <br>
            <br>

            <div class="checkbox">
                <input id="checkbox_signup" type="checkbox" checked>
                <label for="checkbox_signup">
                    i accept
                </label>
                <a href="#">terms & condition</a>
            </div>


            <input type="submit" value="Register" onclick="validate_form(form_val)">
            <br>

            <div class="response">
                 </div>
            <p id="signin">already have an account?
                <a href="#">sign in</a>
            </p>




        </form>
    </div>
    
</body>

</html>
