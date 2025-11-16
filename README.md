# QR-BACK-END-PROJECT
This is a simple Node.js application that generates a QR code from any URL entered by the user. It uses Inquirer to collect user input, qr-image to create the QR code, and the native fs module to save both the QR image and the URL in a text file.
 Features

Prompts the user to enter any URL

Generates a QR code image (qr_img.png)

Saves the entered URL into URL.txt

Uses Node.js modules and npm packages

 Technologies Used

Node.js

Inquirer (for CLI prompts)

qr-image (for QR code creation)

fs (to write files)

 How It Works
1️ Ask the user for a URL
inquirer.prompt([{ message: "Type in your URL:", name: "URL" }])

2️ Convert the URL into a QR code
var qr_svg = qr.image(url);
qr_svg.pipe(fs.createWriteStream("qr_img.png"));

3️ Save the URL in a text file
fs.writeFile("URL.txt", url, (err) => { ... });

 Project Structure
qr-code-generator/
│── index.js
│── package.json
│── qr_img.png (generated)
└── URL.txt (generated)

 How to Run

Install dependencies

npm install inquirer qr-image


Run the script

node index.js


Enter any URL in the prompt

Your files will be generated:

 qr_img.png → Your QR Code

 URL.txt → Saved URL

 Notes

This project is ideal for beginners learning:

Working with Node.js modules

Using command-line prompts

Generating files dynamically
