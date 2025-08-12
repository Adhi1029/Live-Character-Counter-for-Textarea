<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Live Character Counter</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 600px;
            margin: 0 auto;
            padding: 20px;
        }
        h1 {
            color: #333;
        }
        textarea {
            width: 100%;
            height: 100px;
            padding: 10px;
            margin-bottom: 10px;
            border: 1px solid #ccc;
            border-radius: 4px;
            resize: vertical;
        }
        #charCount {
            font-weight: bold;
            color: #333;
        }
        .placeholder {
            color: #999;
            font-style: italic;
        }
    </style>
</head>
<body>
    <h1>Live Character Counter</h1>
    <p id="placeholder" class="placeholder">Start typing...</p>
    <textarea id="textInput" placeholder="Type something..."></textarea>
    <p><strong>Characters: <span id="charCount">0</span></strong></p>

    <script>
        const textInput = document.getElementById('textInput');
        const charCount = document.getElementById('charCount');
        const placeholder = document.getElementById('placeholder');

        textInput.addEventListener('input', function() {
            const count = this.value.length;
            charCount.textContent = count;
            
            if (count > 0) {
                placeholder.style.display = 'none';
            } else {
                placeholder.style.display = 'block';
            }
        });
    </script>
</body>
</html>
