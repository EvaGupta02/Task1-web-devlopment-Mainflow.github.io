<!DOCTYPE html>
<html lang="en">
<head>  
    <!-- ===== Iconscout CSS ===== -->
    <link rel="stylesheet" href="https://unicons.iconscout.com/release/v4.0.0/css/line.css">

    <!-- ===== CSS ===== -->
    <link rel="stylesheet" href="stylesignup.css">
         
    <!--<title>Login & Registration Form</title>-->
    <script>
        function validateName()
        {
            var nm=document.form1.name.value;
            var pass=document.form1.upass.value;
            if(nm==null || nm=="")
            {
                alert("Name can't be blank");
                return false;
            }
            else if(pass.length<8)
            {
                alert("Password must be at least 8 characters");
                return false;
            }
            return true;
        }
        function matchpass()
        {
            var pass=document.form1.upass.value;
            var repass=document.form1.repass.value;
            if(pass==repass)
                return true;
            else{
                alert("Passwords must be same");
                return false;
            }
        }
        function validateEmail()
        {
            var x=document.form1.email.value;
            var atpos=x.indexof("@");
            var dotpos=x.lastIndexOf(".");
            if(atpos<1 || dotpos<atpos+2 || dotpos+2>=x.length)
                {
                    alert("Please enter valid email address");
                    return false;
                }
                else
                return true;
        }
    
    </script>
</head>
<body>
    
    <div class="container">
        <div class="forms">
            <div class="form login">
                <span class="title">Login</span>

                <form action="#">
                    <div class="input-field">
                        <input type="text" placeholder="Enter your email" required>
                        <i class="uil uil-envelope icon"></i>
                    </div>
                    <div class="input-field">
                        <input type="password" class="password" placeholder="Enter your password" required>
                        <i class="uil uil-lock icon"></i>
                        <i class="uil uil-eye-slash showHidePw"></i>
                    </div>

                    <div class="checkbox-text">
                        <div class="checkbox-content">
                            <input type="checkbox" id="logCheck">
                            <label for="logCheck" class="text">Remember me</label>
                        </div>
                        
                        <a href="#" class="text">Forgot password?</a>
                    </div>

                    <div class="input-field button">
                        <input type="button" value="Login">
                    </div>
                </form>

                <div class="login-signup">
                    <span class="text">Not a member?
                        <a href="#" class="text signup-link">Signup Now</a>
                    </span>
                </div>
            </div>

            <!-- Registration Form -->
            <div class="form signup">
                <span class="title">Registration</span>

                <form action="#" name="form1">
                    <div class="input-field">
                        <input type="text" name="name" placeholder="Enter your name" onfocusout="validateName()" required>
                        <i class="uil uil-user"></i>
                    </div>
                    <div class="input-field">
                        <input type="email" name="email" placeholder="Enter your email" onchange="validateEmail()" required>
                        <i class="uil uil-envelope icon"></i>
                    </div>
                    <div class="input-field">
                        <input type="password" name="upass" class="password" onchange="validateName()" placeholder="Create a password" required>
                        <i class="uil uil-lock icon"></i>
                    </div>
                    <div class="input-field">
                        <input type="password" name="repass" class="password" onchange="matchpass()" placeholder="Confirm a password" required>
                        <i class="uil uil-lock icon"></i>
                        <i class="uil uil-eye-slash showHidePw"></i>
                    </div>

                    <div class="checkbox-text">
                        <div class="checkbox-content">
                            <input type="checkbox" id="termCon">
                            <label for="termCon" class="text">I accepted all terms and conditions</label>
                        </div>
                    </div>

                    <div class="input-field button">
                        <input type="button" value="Signup">
                    </div>
                </form>

                <div class="login-signup">
                    <span class="text">Already a member?
                        <a href="#" class="text login-link">Login Now</a>
                    </span>
                </div>
            </div>
        </div>
    </div>

    <script src="signup.js"></script>
</body>
</html>
