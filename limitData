<?php
$servername = "localhost";
$username = "root";
$password = "";
$dbname = "myDB";

// Create connection
$conn = new mysqli($servername, $username, $password, $dbname);
// Check connection
if ($conn->connect_error) {
    die("Connection failed: " . $conn->connect_error);
}

$sql = "SELECT * FROM MyGuests LIMIT 5";
$result = $conn->query($sql);

if ($result->num_rows > 0) {
    // output data of each row
    while($row = $result->fetch_assoc()) {
        echo "<strong>id</strong>: " . $row["id"]. " -<strong>Name:</strong> " . $row["firstname"]. " " . $row["lastname"]. " - <strong>Email:</strong> ". $row["email"]. "-<strong>Phone:</strong> " .$row["phone"]. "<br><br>";
    }
} else {
    echo "0 results";
}
$conn->close();
?>
