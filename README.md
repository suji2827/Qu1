4s.
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Settings Page - Test Automation</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            text-align: center;
            padding: 20px;
        }
        .container {
            background: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0px 0px 10px #ccc;
            width: 40%;
            margin: auto;
        }
        .section {
            margin-bottom: 20px;
        }
        .success-message {
            color: green;
            font-weight: bold;
            display: none;
        }
        button {
            background-color: #28a745;
            color: white;
            padding: 10px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #218838;
        }
    </style>
</head>
<body>

    <div class="container">
        <h2>Settings Page</h2>

        <!-- Section 1: Checkbox and Radio Button -->
        <div class="section">
            <h3>Preferences</h3>
            <input type="checkbox" id="newsletters" name="preferences"> Newsletters<br>
            <input type="checkbox" id="updates" name="preferences"> Updates<br>
            <input type="checkbox" id="offers" name="preferences"> Offers<br>
            
            <h3>Gender</h3>
            <input type="radio" id="male" name="gender" value="male"> Male
            <input type="radio" id="female" name="gender" value="female"> Female
            <input type="radio" id="other" name="gender" value="other"> Other
            
            <br><br>
            <button onclick="savePreferences()">Save</button>
            <p id="saveMessage" class="success-message">Preferences Saved!</p>
        </div>

        <!-- Section 2: File Upload and Download -->
        <div class="section">
            <h3>File Upload</h3>
            <input type="file" id="fileUpload" accept=".png, .jpg">
            <button onclick="uploadFile()">Upload</button>
            <p id="uploadMessage" class="success-message">File Uploaded Successfully!</p>
        </div>

        <div class="section">
            <h3>File Download</h3>
            <a href="sample.txt" download id="downloadLink">Download Sample File</a>
        </div>
    </div>

    <script>
        function savePreferences() {
            document.getElementById("saveMessage").style.display = "block";
        }

        function uploadFile() {
            let fileInput = document.getElementById("fileUpload");
            if (fileInput.files.length > 0) {
                document.getElementById("uploadMessage").style.display = "block";
            } else {
                alert("Please select a file to upload.");
            }
        }
    </script>

</body>
</html>
