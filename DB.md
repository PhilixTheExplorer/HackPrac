```
CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    firstname VARCHAR(255) NOT NULL,
    lastname VARCHAR(255) NOT NULL,
    username VARCHAR(255) UNIQUE NOT NULL,
    university VARCHAR(255) NOT NULL,
    email VARCHAR(255) UNIQUE NOT NULL,
    password VARCHAR(255) NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
INSERT INTO users (firstname, lastname, username, university, email, password) VALUES
('John', 'Doe', 'johndoe', 'University of Example', 'john.doe@example.edu', 'password123'),
('Jane', 'Smith', 'janesmith', 'Example State University', 'jane.smith@example.edu', 'password123'),
('Michael', 'Johnson', 'mjohnson', 'Example Tech', 'michael.johnson@example.edu', 'password123'),
('Emily', 'Davis', 'emilyd', 'Example University', 'emily.davis@example.edu', 'password123'),
('Daniel', 'Brown', 'danbrown', 'Example Institute of Technology', 'daniel.brown@example.edu', 'password123'),
('Olivia', 'Wilson', 'owilson', 'Example College', 'olivia.wilson@example.edu', 'password123'),
('Matthew', 'Taylor', 'mtaylor', 'Example University', 'matthew.taylor@example.edu', 'password123'),
('Sophia', 'Anderson', 'sophiaa', 'Example University', 'sophia.anderson@example.edu', 'password123'),
('James', 'Thomas', 'jamesthomas', 'Example University', 'james.thomas@example.edu', 'password123'),
('Ava', 'Martinez', 'avam', 'Example College', 'ava.martinez@example.edu', 'password123');

```

```
const emailRegex = /^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.(edu|ac\.[a-zA-Z]{2,})$/;
const emails = [
    "example@university.edu",
    "example@kmutt.ac.th",
    "example@oxford.ac.uk",
    "example@something.ac.something"
];

emails.forEach(email => {
    console.log(`${email}: ${emailRegex.test(email)}`); // true or false
});

```
