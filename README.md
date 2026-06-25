## Welcome to QuickyJS      
QuickyJS is a **lightweight** way to instantly test code snippets of HTML, CSS (with HTML because CSS can't "run" by itself), and JS!     

THIS README covers usage, use cases, tech stack, licensing, and has a few quick previews. 

## Usage
To start, copy/paste your code into the text box or drag and drop or click in the other box to insert a HTML/CSS/JS file.
Use theme button to switch between light/dark mode. 
Click run to execute your HTML/CSS/JS.
You can set it to auto (auto recognize HTML/CSS/JS), or set a specific language. 

## Use cases
Use this when you need to test web code snippets/files, or if you just want to play around.

## Licensing
MIT [LICENSE](LICENSE) - free to use, modify, post. 

## Previews
<img width="2560" height="1258" alt="Screenshot 2026-06-25 at 1 47 00 PM" src="https://github.com/user-attachments/assets/02134d7e-3f0b-460c-8917-70ae22792c22" /> 
Now we will run this HTML snippet:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Random Quote & Color Generator</title>
    <style>
        /* Modern, centered layout style */
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #2c3e50;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            transition: background-color 0.5s ease;
        }

        /* Card interface structure */
        .card {
            background-color: #ffffff;
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 8px 24px rgba(0, 0, 0, 0.2);
            text-align: center;
            max-width: 450px;
            width: 90%;
        }

        h1 {
            font-size: 1.5rem;
            color: #333333;
            margin-bottom: 20px;
        }

        p {
            font-size: 1.2rem;
            color: #555555;
            font-style: italic;
            line-height: 1.6;
            min-height: 80px;
        }

        /* Interactive button styling */
        button {
            background-color: #3498db;
            color: white;
            border: none;
            padding: 12px 24px;
            font-size: 1rem;
            border-radius: 6px;
            cursor: pointer;
            font-weight: bold;
            transition: transform 0.1s ease, background-color 0.2s ease;
        }

        button:hover {
            background-color: #2980b9;
        }

        button:active {
            transform: scale(0.98);
        }
    </style>
</head>
<body>

    <div class="card">
        <h1>Inspiration Capsule</h1>
        <!-- Target container where JavaScript injects random quotes -->
        <p id="quote-display">Click the button below to generate your first random quote!</p>
        <button onclick="generateRandomContent()">Generate New</button>
    </div>

    <script>
        // Array containing pre-defined quote elements
        const quotes = [
            "The only way to do great work is to love what you do. — Steve Jobs",
            "Change your thoughts and you change your world. — Norman Vincent Peale",
            "Success is not final, failure is not fatal: it is the courage to continue that counts. — Winston Churchill",
            "Act as if what you do makes a difference. It does. — William James",
            "Believe you can and you're halfway there. — Theodore Roosevelt"
        ];

        // Array containing curated background hex codes
        const colors = ["#1abc9c", "#2ecc71", "#3498db", "#9b59b6", "#e67e22", "#e74c3c", "#16a085"];

        function generateRandomContent() {
            // Pick an item index from the quotes array using Math.random
            const randomQuoteIndex = Math.floor(Math.random() * quotes.length);
            // Pick an item index from the colors array
            const randomColorIndex = Math.floor(Math.random() * colors.length);

            // Inject the selected elements into the DOM structure
            document.getElementById("quote-display").innerText = quotes[randomQuoteIndex];
            document.body.style.backgroundColor = colors[randomColorIndex];
        }
    </script>

</body>
</html>
```
And just take a look!
<img width="2560" height="1258" alt="Screenshot 2026-06-25 at 1 48 26 PM" src="https://github.com/user-attachments/assets/7af237f2-3f0d-41c8-9c6c-e5034ea26b7f" />

And that's all for the QuickyJS project!


