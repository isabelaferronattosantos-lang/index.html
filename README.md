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
        h1 { 
            color: #2e7d32; 
            margin-bottom: 5px;
        }
        .subtitulo {
            color: #558b2f;
            font-weight: bold;
            margin-top: 0;
        }
        .painel {
            font-size: 22px;
            margin: 20px font-weight: bold;
            display: flex;
            justify-content: center;
            gap: 30px;
        }
        #fazenda {
            display: grid;
            grid-template-columns: repeat(3, 110px);
            gap: 15px;
            justify-content: center;
            margin-top: 20px;
        }
        .lote {
            width: 110px;
            height: 110px;
            background-color: #8d6e63;
            border: 4px solid #5d4037;
            border-radius: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 45px;
            cursor: pointer;
            transition: transform 0.2s, background-color 0.3s;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }
        .lote:hover { 
            transform: scale(1.05); 
            background-color: #a1887f;
        }
        .btn-reiniciar {
            margin-top: 30px;
            padding: 12px 25px;
            font-size: 16px;
            font-weight: bold;
            color: white;
            background-color: #2e7d32;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            transition: background 0.2s;
        }
        .btn-reiniciar:hover {
            background-color: #1b5e20;
        }
    </style>
</head>
<body>

    <h1>Agrinho 2026</h1>
    <p class="subtitulo">Agro Forte, Futuro Sustentável</p>
    <p>Clique nos alimentos maduros (🌱 -> 🍎) para colher. Evite colher a planta jovem!</p>
    
    <div class="painel">
        <div>Pontos: <span id="pontos">0</span></div>
    </div>

    <div id="fazenda">
        <div class="lote" onclick="colher(0)" id="lote0">🤎</div>
        <div class="lote" onclick="colher(1)" id="lote1">🤎</div>
        <div class="lote" onclick="colher(2)" id="lote2">🤎</div>
        <div class="lote" onclick="colher(3)" id="lote3">🤎</div>
        <div class="lote" onclick="colher(4)" id="lote4">🤎</div>
        <div class="lote" onclick="colher(5)" id="lote5">🤎</div>
    </div>

    <button class="btn-reiniciar" onclick="reiniciarJogo()">Reiniciar Tabuleiro</button>

    <script src="script.js"></script>
</body>
</html>
