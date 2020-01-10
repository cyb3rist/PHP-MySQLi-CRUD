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

//SELECT ALL DATA IN DESENDING ORDER
//$sql = "SELECT * FROM MyGuests ORDER BY `id` DESC";
 
//SELECT TARGATED DATA IN DESENDING ORDER
$sql = "SELECT id, firstname, lastname, phone FROM MyGuests ORDER BY `id` DESC";
$result = $conn->query($sql);

if ($result->num_rows > 0) {
    // output data of each row
    while($row = $result->fetch_assoc()) {
        echo "id: " . $row["id"]. " - Name: " . $row["firstname"]. " -Call " . $row["phone"]. "<br>";
    }
} else {
    echo "0 results";
}
$conn->close();
?>
