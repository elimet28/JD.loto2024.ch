<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Commande de Boissons</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f8f9fa;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        .container {
            background-color: #ffffff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        h1 {
            text-align: center;
        }
        form {
            display: flex;
            flex-direction: column;
        }
        label, input, select {
            margin-bottom: 10px;
        }
        button {
            background-color: #007bff;
            color: #ffffff;
            border: none;
            padding: 10px;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Commande de Boissons</h1>
        <form id="orderForm">
            <label for="name">Nom :</label>
            <input type="text" id="name" name="name" required>
            
            <label for="drink">Boisson :</label>
            <select id="drink" name="drink" required>
                <option value="coffee">Café</option>
                <option value="tea">Thé</option>
                <option value="juice">Jus</option>
                <option value="water">Eau</option>
            </select>
            
            <label for="quantity">Quantité :</label>
            <input type="number" id="quantity" name="quantity" required min="1" max="10">
            
            <button type="submit">Commander</button>
        </form>
    </div>

    <script>
        document.getElementById('orderForm').addEventListener('submit', function(event) {
            event.preventDefault();
            alert('Commande passée !');
        });
    </script>
</body>
</html>
