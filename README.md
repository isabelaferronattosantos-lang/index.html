# index.html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Agrinho 2026 - Missão Colheita Sustentável</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #e8f5e9;
            text-align: center;
            margin: 0;
            padding: 20px;
        }
        h1 { color: #2e7d32; }
        .painel {
            font-size: 20px;
            margin-bottom: 20px;
            font-weight: bold;
        }
        #fazenda {
            display: grid;
            grid-template-columns: repeat(3, 100px);
            gap: 15px;
            justify-content: center;
            margin-top: 20px;
        }
        .lote {
            width: 100px;
            height: 100px;
            background-color: #8d6e63;
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 40px;
            cursor: pointer;
            transition: transform 0.2s;
        }
        .lote:hover { transform: scale(1.05); }
    </style>
</head>
<body>

    <h1>Agrinho 2026: Agro Forte, Futuro Sustentável</h1>
    <p>Clique nos alimentos maduros (🌱 -> 🍎) para colher. Evite colher a planta jovem!</p>
    
    <div class="painel">Pontuação: <span id="pontos">0</span></div>

    <div id="fazenda">
        <div class="lote" onclick="colher(0)" id="lote0">🤎</div>
        <div class="lote" onclick="colher(1)" id="lote1">🤎</div>
        <div class="lote" onclick="colher(2)" id="lote2">🤎</div>
        <div class="lote" onclick="colher(3)" id="lote3">🤎</div>
        <div class="lote" onclick="colher(4)" id="lote4">🤎</div>
        <div class="lote" onclick="colher(5)" id="lote5">🤎</div>
    </div>

    <script src="script.js"></script>
</body>
</html>
