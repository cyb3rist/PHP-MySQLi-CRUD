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

// prepare and bind
$stmt = $conn->prepare("INSERT INTO MyGuests (firstname, lastname, email, phone) VALUES (?, ?, ?, ?)");
$stmt->bind_param("ssss", $firstname, $lastname, $email, $phone);

//INSERT MULTIPLE RECORDS INTO MYSQL WITH PHP
//Including Prepared Statements and Bound Parameters
//Prepared statements are very useful against SQL injections
// set parameters and execute
$firstname = "orange";
$lastname = "Duck";
$email = "duckorange@example.com";
$phone = "1111111111";
$stmt->execute();

$firstname = "Cloud";
$lastname = "Frog";
$email = "frogcloud@example.com";
$phone = "2222222222";
$stmt->execute();

$firstname = "Trippy";
$lastname = "Cat";
$email = "cattrippy@example.com";
$phone = "3333333333";
$stmt->execute();

echo "New records created successfully";

$stmt->close();
$conn->close();
?>


/**
 //Get ID of The Last Inserted Record -paste code before $stmt->close();

 if ($conn->connect_error) {
    die("Connection failed: " . $conn->connect_error);
} else {
    ($conn->query($stmt) === TRUE);
    $last_id = $conn->insert_id;
    echo "New record created successfully. Last inserted ID is: " . $last_id;
}
 */
