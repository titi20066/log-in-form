senssion_start(

)


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login Form</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="login-container">
        <h2>Login Form</h2>

        <form action="" method="POST">
            <div class="input-field">
                <label for="username">Username</label>
                <input type="text" id="username" name="user" required>
            </div>

            <div class="input-field">
                <label for="password">Password</label>
                <input type="password" id="password" name="pass" required>
            </div>

            <input type="submit" name="ok" value="Login">
        </form>
    </div>

    <?php
    if (isset($_POST['ok'])) {
        $con = mysqli_connect("localhost", "root", "", "login");

        if (!$con) {
            die("Connection failed: " . mysqli_connect_error());
        }

        $user =$_POST['user'];
        $pass =$_POST['pass'];

        $sql = "INSERT INTO dml (username, password) VALUES ('$user', '$pass')";

        if (mysqli_query($con, $sql)) {
            echo "wellcome,$user</p>";
        } else {
            echo "<p>Error: " . mysqli_error($con) . "</p>";
        }

        mysqli_close($con);
        if($_SESSION[''])
    }

    ?>
</body>
</html>
# log-in-form
