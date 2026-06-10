# index.html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Projeto Agrinho 2026</title>
    <style>
        /* ==========================================================================
           ESTILO DO SITE (CSS) - Visual moderno e focado no Agro sustentável
           ========================================================================== */
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f7f6;
            color: #333;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }

        /* Cabeçalho */
        header {
            background: linear-gradient(135deg, #2e7d32, #1b5e20);
            color: white;
            padding: 50px 0;
            text-align: center;
            box-shadow: 0 4px 10px rgba(0,0,0,0.15);
        }

        header h1 {
            margin: 0;
            font-size: 2.6rem;
            letter-spacing: 1px;
        }

        header p {
            margin: 10px 0 0 0;
            font-size: 1.2rem;
            opacity: 0.9;
        }

        /* Conteúdo Principal */
        main {
            padding: 20px 0;
        }

        /* Seções */
        section {
            background: white;
            padding: 30px;
            margin: 30px 0;
            border-radius: 12px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.05);
        }

        h2 {
            color: #1b5e20;
            border-bottom: 3px solid #a5d6a7;
            padding-bottom: 10px;
            margin-top: 0;
        }

        /* Cartões de Monitoramento (Dashboard) */
        .cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
            margin: 25px 0;
        }

        .card {
            background: #e8f5e9;
            padding: 25px;
            border-left: 6px solid #2e7d32;
            border-radius: 8px;
            text-align: center;
            transition: transform 0.2s;
        }

        .card:hover {
            transform: translateY(-5px);
        }

        .card h3 {
            margin: 0 0 15px 0;
            color: #1b5e20;
            font-size: 1.2rem;
            text-transform: uppercase;
        }

        .card p {
            margin: 0;
            font-size: 1.8rem;
            font-weight: bold;
        }

        /* Botão de Atualização */
        .btn-container {
            text-align: center;
            margin-top: 20px;
        }

        button {
            background-color: #2e7d32;
            color: white;
            border: none;
            padding: 14px 30px;
            font-size: 1.1rem;
            font-weight: bold;
            border-radius: 6px;
            cursor: pointer;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            transition: background 0.3s, transform 0.1s;
        }

        button:hover {
            background-color: #1b5e20;
        }

        button:active {
            transform: scale(0.98);
        }

        /* Rodapé */
        footer {
            background-color: #263238;
            color: #b0bec5;
            text-align: center;
            padding: 25px 0;
            margin-top: 50px;
            font-size: 0.95rem;
        }
    </style>
</head>
<body>

    <header>
        <div class="container">
            <h1>Agrinho 2026: Inovação no Campo</h1>
            <p>Tecnologia e Sustentabilidade a Serviço do Produtor</p>
        </div>
    </header>

    <main class="container">
        <section id="sobre">
            <h2>🌱 Sobre o Projeto</h2>
            <p>Este sistema foi desenvolvido para responder aos desafios propostos pelo Concurso Agrinho 2026. Nossa solução foca na aplicação prática de tecnologia no campo, permitindo monitorar as condições ideais do solo para evitar o desperdício de água e insumos, fortalecendo a agricultura familiar e a produtividade sustentável.</p>
        </section>

        <section id="dashboard">
            <h2>📊 Painel de Monitoramento em Tempo Real</h2>
            <p>Abaixo estão exibidos os dados capturados pelos sensores em campo (Simulação automatizada):</p>
            
            <div class="cards">
                <div class="card">
                    <h3>Umidade do Solo</h3>
                    <p id="umidade-valor">-- %</p>
                </div>
                <div class="card">
                    <h3>Status do Sistema</h3>
                    <p id="status-bomba">Analisando...</p>
                </div>
            </div>

            <div class="btn-container">
                <button onclick="atualizarDados()">Simular Nova Leitura dos Sensores</button>
            </div>
        </section>
    </main>

    <footer>
        <div class="container">
            <p>&copy; 2026 - Projeto Desenvolvido para o Concurso Agrinho</p>
        </div>
    </footer>

    <script>
        /* ==========================================================================
           LÓGICA DO SITE (JAVASCRIPT) - Processamento de dados e interatividade
           ========================================================================== */
        function atualizarDados() {
            // Simula um valor de umidade realista capturado por um sensor (entre 20% e 85%)
            const umidadeCalculada = Math.floor(Math.random() * (85 - 20 + 1)) + 20;
            
            const campoUmidade = document.getElementById("umidade-valor");
            const campoBomba = document.getElementById("status-bomba");

            // Atualiza o texto na tela
            campoUmidade.innerText = umidadeCalculada + "%";

            // Regra de Negócio: Se a umidade for menor que 45%, a terra está seca e precisa de água
            if (umidadeCalculada < 45) {
                campoBomba.innerText = "Irrigação Ativada";
                campoBomba.style.color = "#d32f2f"; // Vermelho Alerta
            } else {
                campoBomba.innerText = "Solo Estável";
                campoBomba.style.color = "#2e7d32"; // Verde Estável
            }
        }

        // Executa a primeira leitura automaticamente assim que a página abre
        window.onload = atualizarDados;
    </script>
</body>
</html>
