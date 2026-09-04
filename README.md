# MatrizesDRE-Maracan-
Matriz SAEB e ENEM
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Matriz Completa de Progressão Cognitiva - Língua Portuguesa e Matemática</title>
    <style>
        :root {
            --primary: #1E293B;
            --secondary: #2563EB;
            --bg: #F8FAFC;
            --text: #0F172A;
            --card-bg: #FFFFFF;
            --basic: #16A34A;
            --inter: #D97706;
            --advanced: #DC2626;
            --border: #E2E8F0;
            --badge-grade: #475569;
        }
        
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
        }

        body {
            background-color: var(--bg);
            color: var(--text);
            line-height: 1.6;
            padding-bottom: 3rem;
        }

        header {
            background: linear-gradient(135deg, var(--primary), #0F172A);
            color: white;
            text-align: center;
            padding: 2.5rem 1rem;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
        }

        .org-badge {
            display: inline-block;
            background-color: rgba(255, 255, 255, 0.15);
            padding: 4px 16px;
            border-radius: 20px;
            font-size: 0.9rem;
            font-weight: 600;
            margin-bottom: 0.8rem;
            border: 1px solid rgba(255, 255, 255, 0.25);
            letter-spacing: 0.5px;
        }

        header h1 {
            font-size: 2.2rem;
            margin-bottom: 0.5rem;
            font-weight: 700;
        }

        header p {
            color: #94A3B8;
            font-size: 1.1rem;
        }

        .container {
            max-width: 1200px;
            margin: 2rem auto;
            padding: 0 1rem;
        }

        /* Controles de Busca e Filtro */
        .controls {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            margin-bottom: 2rem;
            background-color: var(--card-bg);
            padding: 1.2rem;
            border-radius: 12px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.05);
            border: 1px solid var(--border);
            align-items: center;
        }

        .search-box {
            flex: 2;
            min-width: 250px;
        }

        .search-box input {
            width: 100%;
            padding: 10px 15px;
            border: 1px solid var(--border);
            border-radius: 8px;
            font-size: 1rem;
            outline: none;
            transition: border-color 0.2s;
        }

        .search-box input:focus {
            border-color: var(--secondary);
        }

        .filter-box {
            flex: 1;
            min-width: 180px;
        }

        .filter-box select {
            width: 100%;
            padding: 10px 15px;
            border: 1px solid var(--border);
            border-radius: 8px;
            font-size: 1rem;
            background-color: white;
            outline: none;
            cursor: pointer;
        }

        /* Botões de Ação */
        .action-buttons {
            display: flex;
            gap: 0.5rem;
            flex-wrap: wrap;
        }

        .btn-search {
            background-color: var(--primary);
            color: white;
            border: none;
            padding: 10px 18px;
            font-size: 0.95rem;
            font-weight: 600;
            border-radius: 8px;
            cursor: pointer;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            transition: background-color 0.2s, transform 0.1s;
        }

        .btn-search:hover {
            background-color: #334155;
            transform: translateY(-1px);
        }

        .btn-print {
            background-color: var(--secondary);
            color: white;
            border: none;
            padding: 10px 18px;
            font-size: 0.95rem;
            font-weight: 600;
            border-radius: 8px;
            cursor: pointer;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            transition: background-color 0.2s, transform 0.1s;
        }

        .btn-print:hover {
            background-color: #1D4ED8;
            transform: translateY(-1px);
        }

        /* Abas */
        .tabs {
            display: flex;
            justify-content: center;
            gap: 0.8rem;
            margin-bottom: 2rem;
            flex-wrap: wrap;
        }

        .tab-btn {
            background-color: #E2E8F0;
            border: none;
            padding: 12px 24px;
            font-size: 1rem;
            font-weight: 600;
            color: var(--primary);
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.2s ease;
        }

        .tab-btn:hover {
            background-color: #CBD5E1;
        }

        .tab-btn.active {
            background-color: var(--secondary);
            color: white;
            box-shadow: 0 4px 10px rgba(37, 99, 235, 0.3);
        }

        .tab-content {
            display: none;
        }

        .tab-content.active {
            display: block;
            animation: fadeIn 0.4s ease;
        }

        /* Seções e Tópicos */
        .topic-group {
            margin-bottom: 2.5rem;
            background: white;
            padding: 1.5rem;
            border-radius: 12px;
            border: 1px solid var(--border);
            box-shadow: 0 2px 6px rgba(0,0,0,0.02);
        }

        .topic-title {
            font-size: 1.3rem;
            color: var(--primary);
            margin-bottom: 1.2rem;
            padding-bottom: 0.5rem;
            border-bottom: 2px solid var(--secondary);
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .cards-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
            gap: 1.2rem;
        }

        /* Card de Descritor */
        .card {
            background-color: var(--card-bg);
            border-radius: 8px;
            padding: 1.2rem;
            border: 1px solid var(--border);
            border-left: 5px solid var(--secondary);
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            transition: transform 0.2s, box-shadow 0.2s;
        }

        .card:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 16px rgba(0,0,0,0.06);
        }

        .card[data-level="1"] { border-left-color: var(--basic); }
        .card[data-level="2"] { border-left-color: var(--inter); }
        .card[data-level="3"] { border-left-color: var(--advanced); }

        .card-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 0.8rem;
        }

        .descriptor-code {
            font-weight: 700;
            font-size: 1.1rem;
            color: var(--primary);
        }

        .level-badge {
            padding: 2px 10px;
            border-radius: 12px;
            font-size: 0.75rem;
            font-weight: 700;
            color: white;
            text-transform: uppercase;
        }

        .card[data-level="1"] .level-badge { background-color: var(--basic); }
        .card[data-level="2"] .level-badge { background-color: var(--inter); }
        .card[data-level="3"] .level-badge { background-color: var(--advanced); }

        .grade-pills {
            display: flex;
            flex-wrap: wrap;
            gap: 4px;
            margin-bottom: 0.8rem;
        }

        .pill {
            font-size: 0.72rem;
            padding: 2px 8px;
            border-radius: 4px;
            background-color: #F1F5F9;
            color: #334155;
            font-weight: 600;
            border: 1px solid #CBD5E1;
        }

        .pill.ef5 { background-color: #E0F2FE; color: #0369A1; border-color: #BAE6FD; }
        .pill.ef9 { background-color: #FEF3C7; color: #B45309; border-color: #FDE68A; }
        .pill.em3 { background-color: #FEE2E2; color: #B91C1C; border-color: #FECACA; }

        .card-body h4 {
            font-size: 1rem;
            margin-bottom: 0.5rem;
            color: #1E293B;
        }

        .card-body p {
            font-size: 0.9rem;
            color: #475569;
        }

        .cognitive-detail {
            margin-top: 0.8rem;
            padding-top: 0.8rem;
            border-top: 1px dashed var(--border);
            font-size: 0.82rem;
            color: #64748B;
            font-style: italic;
        }

        /* Estilos da Tabela Comparativa */
        .table-responsive {
            overflow-x: auto;
        }

        .comp-table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 1rem;
            font-size: 0.92rem;
        }

        .comp-table th, .comp-table td {
            padding: 12px 15px;
            border: 1px solid var(--border);
            text-align: left;
        }

        .comp-table th {
            background-color: var(--primary);
            color: white;
            font-weight: 600;
        }

        .comp-table tr:nth-child(even) {
            background-color: #F8FAFC;
        }

        .comp-table tr:hover {
            background-color: #F1F5F9;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(8px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @media(max-width: 768px) {
            .cards-grid { grid-template-columns: 1fr; }
            .controls { flex-direction: column; align-items: stretch; }
            .action-buttons { flex-direction: column; }
            .btn-search, .btn-print { justify-content: center; }
        }

        /* Configurações Estilizadas para Impressão */
        @media print {
            header {
                background: white !important;
                color: black !important;
                padding: 1rem;
                box-shadow: none;
                border-bottom: 2px solid #000;
            }
            header h1 { font-size: 1.6rem; color: #000; }
            header p { color: #333; }
            .org-badge {
                border: 1px solid #000;
                color: #000;
                background: none;
            }
            .controls, .tabs, .action-buttons, .btn-search, .btn-print {
                display: none !important;
            }
            body {
                background: white;
                color: black;
            }
            .container {
                max-width: 100%;
                margin: 0;
                padding: 0;
            }
            .topic-group {
                border: 1px solid #ccc;
                box-shadow: none;
                page-break-inside: avoid;
                margin-bottom: 1.5rem;
            }
            .card {
                page-break-inside: avoid;
                border: 1px solid #ccc;
                box-shadow: none;
                transform: none !important;
            }
            .tab-content {
                display: block !important;
            }
        }
    </style>
</head>
<body>

    <header>
        <div class="org-badge">DRE-MARACANÃ — Organização: Núcleo de Formação - Linguagens e Matemática</div>
        <h1>Ferramenta de Progressão Cognitiva</h1>
        <p>Língua Portuguesa & Matemática: Matrizes SAEB e ENEM (5º EF | 9º EF | 3ª EM)</p>
    </header>

    <div class="container">
        
        <!-- Controles de Busca e Filtro -->
        <div class="controls">
            <div class="search-box">
                <input type="text" id="searchInput" onkeyup="filterCards()" placeholder="Pesquise por código (ex: D1, D14, H8, H24) ou palavra-chave (ex: tese, área, gráficos)...">
            </div>

            <div class="filter-box">
                <select id="gradeFilter" onchange="filterCards()">
                    <option value="all">Todas as Etapas de Ensino</option>
                    <option value="5ef">5º Ano Ensino Fundamental</option>
                    <option value="9ef">9º Ano Ensino Fundamental</option>
                    <option value="3em">3ª Série Ensino Médio</option>
                </select>
            </div>

            <div class="filter-box">
                <select id="levelFilter" onchange="filterCards()">
                    <option value="all">Todos os Níveis Cognitivos</option>
                    <option value="1">Nível 1 - Básico / Identificação</option>
                    <option value="2">Nível 2 - Intermediário / Relação e Aplicação</option>
                    <option value="3">Nível 3 - Avançado / Análise Crítica e Resolução de Problemas</option>
                </select>
            </div>

            <div class="action-buttons">
                <button class="btn-search" onclick="filterCards()">🔍 Pesquisar</button>
                <button class="btn-print" onclick="window.print()">🖨️ Imprimir / Salvar PDF</button>
            </div>
        </div>

        <!-- Abas Principais -->
        <div class="tabs">
            <button class="tab-btn active" onclick="openTab('saeb', this)">Português: SAEB</button>
            <button class="tab-btn" onclick="openTab('enem', this)">Português: ENEM</button>
            <button class="tab-btn" onclick="openTab('matematica', this)">📐 Matemática: SAEB & ENEM</button>
            <button class="tab-btn" onclick="openTab('quadro', this)">Quadro Comparativo de Etapas</button>
        </div>

        <!-- ==================== CONTEÚDO SAEB - PORTUGUÊS ==================== -->
        <div id="saeb" class="tab-content active">

            <!-- Tópico I -->
            <div class="topic-group">
                <h3 class="topic-title">Tópico I: Procedimentos de Leitura</h3>
                <div class="cards-grid">
                    <div class="card" data-level="1" data-grades="5ef 9ef 3em">
                        <div class="card-header">
                            <span class="descriptor-code">D1 (9º/3ªEM) | D1 (5º)</span>
                            <span class="level-badge">Básico</span>
                        </div>
                        <div class="grade-pills">
                            <span class="pill ef5">5º Ano EF</span>
                            <span class="pill ef9">9º Ano EF</span>
                            <span class="pill em3">3ª Série EM</span>
                        </div>
                        <div class="card-body">
                            <h4>Localizar informações explícitas em um texto</h4>
                            <p>Varredura e identificação direta de dados visíveis na superfície do texto.</p>
                            <div class="cognitive-detail">Operação Cognitiva: Reconhecimento e cópia funcional.</div>
                        </div>
                    </div>

                    <div class="card" data-level="1" data-grades="5ef 9ef 3em">
                        <div class="card-header">
                            <span class="descriptor-code">D3 (9º/3ªEM) | D3 (5º)</span>
                            <span class="level-badge">Básico</span>
                        </div>
                        <div class="grade-pills">
                            <span class="pill ef5">5º Ano EF</span>
                            <span class="pill ef9">9º Ano EF</span>
                            <span class="pill em3">3ª Série EM</span>
                        </div>
                        <div class="card-body">
                            <h4>Inferir o sentido de uma palavra ou expressão</h4>
                            <p>Dedução do significado de itens lexicais com base no contexto imediato.</p>
                            <div class="cognitive-detail">Operação Cognitiva: Contextualização e sinonímia.</div>
                        </div>
                    </div>

                    <div class="card" data-level="2" data-grades="5ef 9ef 3em">
                        <div class="card-header">
                            <span class="descriptor-code">D4 (9º/3ªEM) | D4 (5º)</span>
                            <span class="level-badge">Intermediário</span>
                        </div>
                        <div class="grade-pills">
                            <span class="pill ef5">5º Ano EF</span>
                            <span class="pill ef9">9º Ano EF</span>
                            <span class="pill em3">3ª Série EM</span>
                        </div>
                        <div class="card-body">
                            <h4>Inferir uma informação implícita em um texto</h4>
                            <p>Leitura nas entrelinhas articulando pistas textuais ao conhecimento prévio de mundo.</p>
                            <div class="cognitive-detail">Operação Cognitiva: Dedução lógica e pressuposição.</div>
                        </div>
                    </div>

                    <div class="card" data-level="2" data-grades="5ef 9ef 3em">
                        <div class="card-header">
                            <span class="descriptor-code">D6 (9º/3ªEM) | D6 (5º)</span>
                            <span class="level-badge">Intermediário</span>
                        </div>
                        <div class="grade-pills">
                            <span class="pill ef5">5º Ano EF</span>
                            <span class="pill ef9">9º Ano EF</span>
                            <span class="pill em3">3ª Série EM</span>
                        </div>
                        <div class="card-body">
                            <h4>Identificar o tema de um texto</h4>
                            <p>Compreensão global e síntese do assunto central que norteia todo o texto.</p>
                            <div class="cognitive-detail">Operação Cognitiva: Sumarização e abstração.</div>
                        </div>
                    </div>

                    <div class="card" data-level="3" data-grades="5ef 9ef 3em">
                        <div class="card-header">
                            <span class="descriptor-code">D14 (9º/3ªEM) | D11 (5º)</span>
                            <span class="level-badge">Avançado</span>
                        </div>
                        <div class="grade-pills">
                            <span class="pill ef5">5º Ano EF: D11</span>
                            <span class="pill ef9">9º Ano EF: D14</span>
                            <span class="pill em3">3ª Série EM: D14</span>
                        </div>
                        <div class="card-body">
                            <h4>Distinguir um fato da opinião relativa a esse fato</h4>
                            <p>Diferenciação entre acontecimentos objetivos e juízos de valor/subjetividade do autor.</p>
                            <div class="cognitive-detail">Operação Cognitiva: Análise crítica e discernimento epistêmico.</div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Tópico II -->
            <div class="topic-group">
                <h3 class="topic-title">Tópico II: Implicações do Suporte, do Gênero e/ou do Enunciador</h3>
                <div class="cards-grid">
                    <div class="card" data-level="1" data-grades="5ef 9ef 3em">
                        <div class="card-header">
                            <span class="descriptor-code">D5 (9º/3ªEM) | D5 (5º)</span>
                            <span class="level-badge">Básico</span>
                        </div>
                        <div class="grade-pills">
                            <span class="pill ef5">5º Ano EF</span>
                            <span class="pill ef9">9º Ano EF</span>
                            <span class="pill em3">3ª Série EM</span>
                        </div>
                        <div class="card-body">
                            <h4>Interpretar texto com auxílio de material gráfico diverso</h4>
                            <p>Leitura integrada de linguagem verbal e não verbal (tirinhas, fotos, gráficos, tiras).</p>
                            <div class="cognitive-detail">Operação Cognitiva: Integração multissemiótica.</div>
                        </div>
                    </div>

                    <div class="card" data-level="2" data-grades="5ef 9ef 3em">
                        <div class="card-header">
                            <span class="descriptor-code">D12 (9º/3ªEM) | D9 (5º)</span>
                            <span class="level-badge">Intermediário</span>
                        </div>
                        <div class="grade-pills">
                            <span class="pill ef5">5º Ano EF: D9</span>
                            <span class="pill ef9">9º Ano EF: D12</span>
                            <span class="pill em3">3ª Série EM: D12</span>
                        </div>
                        <div class="card-body">
                            <h4>Identificar a finalidade de textos de diferentes gêneros</h4>
                            <p>Reconhecimento do objetivo comunicativo (informar, convencer, instruir, entreter).</p>
                            <div class="cognitive-detail">Operação Cognitiva: Análise da função sociocomunicativa.</div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Tópico III -->
            <div class="topic-group">
                <h3 class="topic-title">Tópico III: Relação entre Textos</h3>
                <div class="cards-grid">
                    <div class="card" data-level="3" data-grades="5ef 9ef 3em">
                        <div class="card-header">
                            <span class="descriptor-code">D20 (9º/3ªEM) | D15 (5º)</span>
                            <span class="level-badge">Avançado</span>
                        </div>
                        <div class="grade-pills">
                            <span class="pill ef5">5º Ano EF: D15</span>
                            <span class="pill ef9">9º Ano EF: D20</span>
                            <span class="pill em3">3ª Série EM: D20</span>
                        </div>
                        <div class="card-body">
                            <h4>Reconhecer diferentes formas de tratar uma informação na comparação de textos</h4>
                            <p>Análise comparativa de abordagens sobre o mesmo tema em diferentes produções.</p>
                            <div class="cognitive-detail">Operação Cognitiva: Comparação intertextual e contextual.</div>
                        </div>
                    </div>

                    <div class="card" data-level="3" data-grades="9ef 3em">
                        <div class="card-header">
                            <span class="descriptor-code">D21 (9º/3ªEM)</span>
                            <span class="level-badge">Avançado</span>
                        </div>
                        <div class="grade-pills">
                            <span class="pill ef9">9º Ano EF: D21</span>
                            <span class="pill em3">3ª Série EM: D21</span>
                        </div>
                        <div class="card-body">
                            <h4>Reconhecer posições distintas entre duas ou mais opiniões relativas ao mesmo fato</h4>
                            <p>Confronto dialético entre pontos de vista divergentes ou complementares sobre um tema.</p>
                            <div class="cognitive-detail">Operação Cognitiva: Análise crítica e avaliação do discurso.</div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Tópico IV -->
            <div class="topic-group">
                <h3 class="topic-title">Tópico IV: Coerência e Coesão no Processamento do Texto</h3>
                <div class="cards-grid">
                    <div class="card" data-level="1" data-grades="5ef 9ef 3em">
                        <div class="card-header">
                            <span class="descriptor-code">D2 (9º/3ªEM) | D2 (5º)</span>
                            <span class="level-badge">Básico</span>
                        </div>
                        <div class="grade-pills">
                            <span class="pill ef5">5º Ano EF</span>
                            <span class="pill ef9">9º Ano EF</span>
                            <span class="pill em3">3ª Série EM</span>
                        </div>
                        <div class="card-body">
                            <h4>Estabelecer relações entre partes de um texto (Substituições / Repetições)</h4>
                            <p>Identificação da coesão referencial por meio de pronomes, sinônimos ou elipses.</p>
                            <div class="cognitive-detail">Operação Cognitiva: Anáfora, catáfora e encadeamento.</div>
                        </div>
                    </div>

                    <div class="card" data-level="1" data-grades="5ef 9ef 3em">
                        <div class="card-header">
                            <span class="descriptor-code">D10 (9º/3ªEM) | D7 (5º)</span>
                            <span class="level-badge">Básico</span>
                        </div>
                        <div class="grade-pills">
                            <span class="pill ef5">5º Ano EF: D7</span>
                            <span class="pill ef9">9º Ano EF: D10</span>
                            <span class="pill em3">3ª Série EM: D10</span>
                        </div>
                        <div class="card-body">
                            <h4>Identificar o conflito gerador do enredo e elementos da narrativa</h4>
                            <p>Reconhecimento da estrutura narrativa: personagem, tempo, espaço e complicação.</p>
                            <div class="cognitive-detail">Operação Cognitiva: Identificação da tipologia narrativa.</div>
                        </div>
                    </div>

                    <div class="card" data-level="2" data-grades="9ef 3em">
                        <div class="card-header">
                            <span class="descriptor-code">D7 (9º/3ªEM)</span>
                            <span class="level-badge">Intermediário</span>
                        </div>
                        <div class="grade-pills">
                            <span class="pill ef9">9º Ano EF: D7</span>
                            <span class="pill em3">3ª Série EM: D7</span>
                        </div>
                        <div class="card-body">
                            <h4>Identificar a tese de um texto</h4>
                            <p>Localização ou dedução da ideia central/posicionamento defendido pelo autor.</p>
                            <div class="cognitive-detail">Operação Cognitiva: Isolamento do núcleo argumentativo.</div>
                        </div>
                    </div>

                    <div class="card" data-level="2" data-grades="9ef 3em">
                        <div class="card-header">
                            <span class="descriptor-code">D8 (9º/3ªEM)</span>
                            <span class="level-badge">Intermediário</span>
                        </div>
                        <div class="grade-pills">
                            <span class="pill ef9">9º Ano EF: D8</span>
                            <span class="pill em3">3ª Série EM: D8</span>
                        </div>
                        <div class="card-body">
                            <h4>Estabelecer relação entre a tese e os argumentos oferecidos</h4>
                            <p>Compreensão da estratégia utilizada pelo autor para fundamentar sua posição.</p>
                            <div class="cognitive-detail">Operação Cognitiva: Articulação lógico-argumentativa.</div>
                        </div>
                    </div>

                    <div class="card" data-level="2" data-grades="9ef 3em">
                        <div class="card-header">
                            <span class="descriptor-code">D9 (9º/3ªEM)</span>
                            <span class="level-badge">Intermediário</span>
                        </div>
                        <div class="grade-pills">
                            <span class="pill ef9">9º Ano EF: D9</span>
                            <span class="pill em3">3ª Série EM: D9</span>
                        </div>
                        <div class="card-body">
                            <h4>Diferenciar as partes principais das secundárias em um texto</h4>
                            <p>Hierarquização das informações textuais para elaboração de esquemas ou resumos.</p>
                            <div class="cognitive-detail">Operação Cognitiva: Seleção e triagem da informatividade.</div>
                        </div>
                    </div>

                    <div class="card" data-level="2" data-grades="5ef 9ef 3em">
                        <div class="card-header">
                            <span class="descriptor-code">D11 (9º/3ªEM) | D8 (5º)</span>
                            <span class="level-badge">Intermediário</span>
                        </div>
                        <div class="grade-pills">
                            <span class="pill ef5">5º Ano EF: D8</span>
                            <span class="pill ef9">9º Ano EF: D11</span>
                            <span class="pill em3">3ª Série EM: D11</span>
                        </div>
                        <div class="card-body">
                            <h4>Estabelecer relação causa/consequência entre partes e elementos</h4>
                            <p>Identificação do nexo causal que une fatos e ideias na construção do sentido.</p>
                            <div class="cognitive-detail">Operação Cognitiva: Raciocínio de causalidade.</div>
                        </div>
                    </div>

                    <div class="card" data-level="3" data-grades="5ef 9ef 3em">
                        <div class="card-header">
                            <span class="descriptor-code">D15 (9º/3ªEM) | D12 (5º)</span>
                            <span class="level-badge">Avançado</span>
                        </div>
                        <div class="grade-pills">
                            <span class="pill ef5">5º Ano EF: D12</span>
                            <span class="pill ef9">9º Ano EF: D15</span>
                            <span class="pill em3">3ª Série EM: D15</span>
                        </div>
                        <div class="card-body">
                            <h4>Estabelecer relações lógico-discursivas marcadas por conectivos</h4>
                            <p>Compreensão das relações de oposição, adição, condição e causa marcadas por conjunções e advérbios.</p>
                            <div class="cognitive-detail">Operação Cognitiva: Análise sintático-semântica da coesão.</div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Tópico V -->
            <div class="topic-group">
                <h3 class="topic-title">Tópico V: Relações entre Recursos Expressivos e Efeitos de Sentido</h3>
                <div class="cards-grid">
                    <div class="card" data-level="2" data-grades="5ef 9ef 3em">
                        <div class="card-header">
                            <span class="descriptor-code">D16 (9º/3ªEM) | D13 (5º)</span>
                            <span class="level-badge">Intermediário</span>
                        </div>
                        <div class="grade-pills">
                            <span class="pill ef5">5º Ano EF: D13</span>
                            <span class="pill ef9">9º Ano EF: D16</span>
                            <span class="pill em3">3ª Série EM: D16</span>
                        </div>
                        <div class="card-body">
                            <h4>Identificar o efeito de sentido decorrente do uso da pontuação e notações</h4>
                            <p>Reconhecimento do papel expressivo de aspas, reticências, travessão e pontos de exclamação/interrogação.</p>
                            <div class="cognitive-detail">Operação Cognitiva: Decodificação expressiva e entonação.</div>
                        </div>
                    </div>

                    <div class="card" data-level="2" data-grades="5ef 9ef 3em">
                        <div class="card-header">
                            <span class="descriptor-code">D17 (9º/3ªEM) | D14 (5º)</span>
                            <span class="level-badge">Intermediário</span>
                        </div>
                        <div class="grade-pills">
                            <span class="pill ef5">5º Ano EF: D14</span>
                            <span class="pill ef9">9º Ano EF: D17</span>
                            <span class="pill em3">3ª Série EM: D17</span>
                        </div>
                        <div class="card-body">
                            <h4>Reconhecer o efeito de sentido da escolha de palavras ou expressões</h4>
                            <p>Análise das intenções do autor e das nuances de significado produzidas pela seleção vocabular.</p>
                            <div class="cognitive-detail">Operação Cognitiva: Sensibilidade estilística e conotação.</div>
                        </div>
                    </div>

                    <div class="card" data-level="3" data-grades="9ef 3em">
                        <div class="card-header">
                            <span class="descriptor-code">D18 e D19 (9º/3ªEM)</span>
                            <span class="level-badge">Avançado</span>
                        </div>
                        <div class="grade-pills">
                            <span class="pill ef9">9º Ano EF</span>
                            <span class="pill em3">3ª Série EM</span>
                        </div>
                        <div class="card-body">
                            <h4>Identificar efeitos de sentido de recursos expressivos (ironia, humor, figuras)</h4>
                            <p>Compreensão de duplos sentidos, sarcasmo, metáforas e personificações em textos literários e charges.</p>
                            <div class="cognitive-detail">Operação Cognitiva: Análise do discurso pragmático e figurado.</div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Tópico VI -->
            <div class="topic-group">
                <h3 class="topic-title">Tópico VI: Variação Linguística</h3>
                <div class="cards-grid">
                    <div class="card" data-level="1" data-grades="5ef 9ef 3em">
                        <div class="card-header">
                            <span class="descriptor-code">D13 (9º/3ªEM) | D10 (5º)</span>
                            <span class="level-badge">Básico</span>
                        </div>
                        <div class="grade-pills">
                            <span class="pill ef5">5º Ano EF: D10</span>
                            <span class="pill ef9">9º Ano EF: D13</span>
                            <span class="pill em3">3ª Série EM: D13</span>
                        </div>
                        <div class="card-body">
                            <h4>Identificar as marcas linguísticas que evidenciam o locutor e o interlocutor</h4>
                            <p>Reconhecimento de registros formais e informais, gírias, regionalismos e jargões socioculturais.</p>
                            <div class="cognitive-detail">Operação Cognitiva: Sociolinguística e adequação vocabular.</div>
                        </div>
                    </div>
                </div>
            </div>

        </div>

        <!-- ==================== CONTEÚDO ENEM - PORTUGUÊS ==================== -->
        <div id="enem" class="tab-content">
            <div class="topic-group">
                <h3 class="topic-title">Habilidades de Linguagens e Códigos (Matriz ENEM)</h3>
                <div class="cards-grid">
                    <div class="card" data-level="1" data-grades="3em">
                        <div class="card-header">
                            <span class="descriptor-code">H1 (Comp. 1)</span>
                            <span class="level-badge">Básico</span>
                        </div>
                        <div class="grade-pills">
                            <span class="pill em3">3ª Série EM</span>
                        </div>
                        <div class="card-body">
                            <h4>Identificar diferentes linguagens e seus recursos expressivos</h4>
                            <p>Reconhecimento do papel das linguagens na caracterização dos sistemas de comunicação.</p>
                            <div class="cognitive-detail">Operação Cognitiva: Classificação de recursos multimodais.</div>
                        </div>
                    </div>

                    <div class="card" data-level="2" data-grades="3em">
                        <div class="card-header">
                            <span class="descriptor-code">H8 (Comp. 2)</span>
                            <span class="level-badge">Intermediário</span>
                        </div>
                        <div class="grade-pills">
                            <span class="pill em3">3ª Série EM</span>
                        </div>
                        <div class="card-body">
                            <h4>Relacionar o texto literário ao seu contexto de produção</h4>
                            <p>Articulação entre a obra artística/literária e os aspectos históricos, sociais e culturais da época.</p>
                            <div class="cognitive-detail">Operação Cognitiva: Contextualização histórico-literária.</div>
                        </div>
                    </div>

                    <div class="card" data-level="3" data-grades="3em">
                        <div class="card-header">
                            <span class="descriptor-code">H12 (Comp. 4)</span>
                            <span class="level-badge">Avançado</span>
                        </div>
                        <div class="grade-pills">
                            <span class="pill em3">3ª Série EM</span>
                        </div>
                        <div class="card-body">
                            <h4>Reconhecer estratégias argumentativas na persuasão</h4>
                            <p>Análise da estrutura discursiva utilizada pelo autor para convencer o interlocutor sobre um ponto de vista.</p>
                            <div class="cognitive-detail">Operação Cognitiva: Avaliação crítica da argumentação.</div>
                        </div>
                    </div>

                    <div class="card" data-level="2" data-grades="3em">
                        <div class="card-header">
                            <span class="descriptor-code">H24 (Comp. 8)</span>
                            <span class="level-badge">Intermediário</span>
                        </div>
                        <div class="grade-pills">
                            <span class="pill em3">3ª Série EM</span>
                        </div>
                        <div class="card-body">
                            <h4>Relacionar variedades linguísticas às situações de uso e identidade</h4>
                            <p>Compreensão da variação como fenômeno natural e reflexo de diversidade social e territorial.</p>
                            <div class="cognitive-detail">Operação Cognitiva: Análise sociolinguística crítica.</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- ==================== CONTEÚDO MATEMÁTICA - SAEB & ENEM ==================== -->
        <div id="matematica" class="tab-content">
            
            <div class="topic-group">
                <h3 class="topic-title">Tópico I: Espaço e Forma (Geometria)</h3>
                <div class="cards-grid">
                    <div class="card" data-level="1" data-grades="5ef 9ef 3em">
                        <div class="card-header">
                            <span class="descriptor-code">D1 (SAEB) | H6 (ENEM)</span>
                            <span class="level-badge">Básico</span>
                        </div>
                        <div class="grade-pills">
                            <span class="pill ef5">5º Ano EF</span>
                            <span class="pill ef9">9º Ano EF</span>
                            <span class="pill em3">3ª Série EM</span>
                        </div>
                        <div class="card-body">
                            <h4>Localização e movimentação de objetos no espaço</h4>
                            <p>Interpretação de coordenadas, croquis, mapas e representações bidimensionais/tridimensionais.</p>
                            <div class="cognitive-detail">Operação Cognitiva: Orientação espacial e leitura de esquemas.</div>
                        </div>
                    </div>

                    <div class="card" data-level="2" data-grades="9ef 3em">
                        <div class="card-header">
                            <span class="descriptor-code">D2/D3 (SAEB) | H8 (ENEM)</span>
                            <span class="level-badge">Intermediário</span>
                        </div>
                        <div class="grade-pills">
                            <span class="pill ef9">9º Ano EF</span>
                            <span class="pill em3">3ª Série EM</span>
                        </div>
                        <div class="card-body">
                            <h4>Propriedades de figuras planas e espaciais</h4>
                            <p>Reconhecimento de semelhança de triângulos, teorema de Pitágoras e relações métricas.</p>
                            <div class="cognitive-detail">Operação Cognitiva: Raciocínio geométrico e deductivo.</div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="topic-group">
                <h3 class="topic-title">Tópico II: Grandezas e Medidas</h3>
                <div class="cards-grid">
                    <div class="card" data-level="2" data-grades="5ef 9ef 3em">
                        <div class="card-header">
                            <span class="descriptor-code">D12/D13 (SAEB) | H11 (ENEM)</span>
                            <span class="level-badge">Intermediário</span>
                        </div>
                        <div class="grade-pills">
                            <span class="pill ef5">5º Ano EF</span>
                            <span class="pill ef9">9º Ano EF</span>
                            <span class="pill em3">3ª Série EM</span>
                        </div>
                        <div class="card-body">
                            <h4>Cálculo de perímetro, área e volume</h4>
                            <p>Resolução de problemas práticos que envolvem estimativa e cálculo de superfícies e capacidades.</p>
                            <div class="cognitive-detail">Operação Cognitiva: Aplicação de fórmulas e modelagem de grandezas.</div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="topic-group">
                <h3 class="topic-title">Tópico III: Números, Operações e Álgebra</h3>
                <div class="cards-grid">
                    <div class="card" data-level="1" data-grades="5ef 9ef 3em">
                        <div class="card-header">
                            <span class="descriptor-code">D19 (SAEB) | H15 (ENEM)</span>
                            <span class="level-badge">Básico</span>
                        </div>
                        <div class="grade-pills">
                            <span class="pill ef5">5º Ano EF</span>
                            <span class="pill ef9">9º Ano EF</span>
                            <span class="pill em3">3ª Série EM</span>
                        </div>
                        <div class="card-body">
                            <h4>Operações fundamentais com números reais</h4>
                            <p>Resolução de problemas envolvendo adição, subtração, multiplicação, divisão e fracionários.</p>
                            <div class="cognitive-detail">Operação Cognitiva: Algoritmos operacionais e estimativa.</div>
                        </div>
                    </div>

                    <div class="card" data-level="2" data-grades="9ef 3em">
                        <div class="card-header">
                            <span class="descriptor-code">D28 (SAEB) | H17 (ENEM)</span>
                            <span class="level-badge">Intermediário</span>
                        </div>
                        <div class="grade-pills">
                            <span class="pill ef9">9º Ano EF</span>
                            <span class="pill em3">3ª Série EM</span>
                        </div>
                        <div class="card-body">
                            <h4>Porcentagem, proporções e regra de três</h4>
                            <p>Cálculo de acréscimos, descontos e relações diretamente ou inversamente proporcionais.</p>
                            <div class="cognitive-detail">Operação Cognitiva: Raciocínio proporcional.</div>
                        </div>
                    </div>

                    <div class="card" data-level="3" data-grades="9ef 3em">
                        <div class="card-header">
                            <span class="descriptor-code">D33 (SAEB) | H21 (ENEM)</span>
                            <span class="level-badge">Avançado</span>
                        </div>
                        <div class="grade-pills">
                            <span class="pill ef9">9º Ano EF</span>
                            <span class="pill em3">3ª Série EM</span>
                        </div>
                        <div class="card-body">
                            <h4>Funções e representações algébricas/gráficas</h4>
                            <p>Modelagem de situações-problema por meio de equações, inequações e funções de 1º e 2º graus.</p>
                            <div class="cognitive-detail">Operação Cognitiva: Abstração algébrica e análise gráfica.</div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="topic-group">
                <h3 class="topic-title">Tópico IV: Tratamento da Informação, Estatística e Probabilidade</h3>
                <div class="cards-grid">
                    <div class="card" data-level="1" data-grades="5ef 9ef 3em">
                        <div class="card-header">
                            <span class="descriptor-code">D36 (SAEB) | H27 (ENEM)</span>
                            <span class="level-badge">Básico</span>
                        </div>
                        <div class="grade-pills">
                            <span class="pill ef5">5º Ano EF</span>
                            <span class="pill ef9">9º Ano EF</span>
                            <span class="pill em3">3ª Série EM</span>
                        </div>
                        <div class="card-body">
                            <h4>Leitura e interpretação de dados em gráficos e tabelas</h4>
                            <p>Extração de informações e dados organizados em gráficos de colunas, setores, linhas e tabelas simples/compostas.</p>
                            <div class="cognitive-detail">Operação Cognitiva: Decodificação de dados estatísticos.</div>
                        </div>
                    </div>

                    <div class="card" data-level="3" data-grades="9ef 3em">
                        <div class="card-header">
                            <span class="descriptor-code">D37 (SAEB) | H28 (ENEM)</span>
                            <span class="level-badge">Avançado</span>
                        </div>
                        <div class="grade-pills">
                            <span class="pill ef9">9º Ano EF</span>
                            <span class="pill em3">3ª Série EM</span>
                        </div>
                        <div class="card-body">
                            <h4>Estatística descritiva e probabilidade</h4>
                            <p>Cálculo de média, moda, mediana e probabilidade de ocorrência de eventos simples ou compostos.</p>
                            <div class="cognitive-detail">Operação Cognitiva: Análise combinatória e tomada de decisão.</div>
                        </div>
                    </div>
                </div>
            </div>

        </div>

        <!-- ==================== QUADRO COMPARATIVO DE ETAPAS ==================== -->
        <div id="quadro" class="tab-content">
            <div class="topic-group">
                <h3 class="topic-title">Quadro de Evolução Cognitiva por Etapa de Ensino</h3>
                <div class="table-responsive">
                    <table class="comp-table">
                        <thead>
                            <tr>
                                <th>Eixo / Dimensão</th>
                                <th>5º Ano (Ensino Fundamental)</th>
                                <th>9º Ano (Ensino Fundamental)</th>
                                <th>3ª Série (Ensino Médio / ENEM)</th>
                                <th>Evolução Cognitiva Esperada</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td><strong>Localização & Inferência</strong></td>
                                <td>Localiza dados explícitos diretos; infere sentido de palavras simples.</td>
                                <td>Infere ideias implícitas complexas e diferencia fato de opinião.</td>
                                <td>Analisa intenções subjacentes, duplos sentidos e pressupostos ideológicos.</td>
                                <td>Do reconhecimento literal à análise crítica do discurso.</td>
                            </tr>
                            <tr>
                                <td><strong>Coesão & Argumentação</strong></td>
                                <td>Identifica substituições pronominais diretas.</td>
                                <td>Identifica a tese, argumentos e conectivos interfrásicos.</td>
                                <td>Avalia a força argumentativa, estratégias persuasivas e falácias.</td>
                                <td>Da coesão referencial local ao domínio da macroestrutura argumentativa.</td>
                            </tr>
                            <tr>
                                <td><strong>Geometria & Medidas</strong></td>
                                <td>Reconhece figuras planas e calcula perímetros/áreas em malhas.</td>
                                <td>Aplica Teorema de Pitágoras, semelhança e áreas de polígonos.</td>
                                <td>Modela problemas de geometria espacial, trigonometria e vetores.</td>
                                <td>Do reconhecimento empírico à dedução e modelagem tridimensional.</td>
                            </tr>
                            <tr>
                                <td><strong>Tratamento da Informação</strong></td>
                                <td>Lê dados diretamente em tabelas e gráficos de colunas.</td>
                                <td>Calcula porcentagens, médias e interpreta gráficos combinados.</td>
                                <td>Analisa dispersão, desvio padrão, probabilidade condicional e inferência.</td>
                                <td>Da leitura passiva à tomada de decisão fundamentada em dados.</td>
                            </tr>
                        </tbody>
                    </table>
                </div>
            </div>
        </div>

    </div>

    <!-- Script de Interatividade e Filtros -->
    <script>
        function openTab(tabName, btnElement) {
            // Esconde todos os conteúdos das abas
            var contents = document.getElementsByClassName("tab-content");
            for (var i = 0; i < contents.length; i++) {
                contents[i].classList.remove("active");
            }

            // Remove classe active de todos os botões das abas
            var buttons = document.getElementsByClassName("tab-btn");
            for (var i = 0; i < buttons.length; i++) {
                buttons[i].classList.remove("active");
            }

            // Ativa o conteúdo e o botão selecionado
            document.getElementById(tabName).classList.add("active");
            if (btnElement) {
                btnElement.classList.add("active");
            }

            // Executa o filtro para ajustar os cards visíveis na aba atual
            filterCards();
        }

        function filterCards() {
            var searchInput = document.getElementById("searchInput").value.toLowerCase().trim();
            var gradeFilter = document.getElementById("gradeFilter").value;
            var levelFilter = document.getElementById("levelFilter").value;

            var activeTab = document.querySelector(".tab-content.active");
            if (!activeTab) return;

            // Filtragem dos Cards
            var cards = activeTab.querySelectorAll(".card");
            cards.forEach(function(card) {
                var cardText = card.innerText.toLowerCase();
                var cardGrades = card.getAttribute("data-grades") || "";
                var cardLevel = card.getAttribute("data-level") || "";

                var matchesSearch = searchInput === "" || cardText.includes(searchInput);
                var matchesGrade = gradeFilter === "all" || cardGrades.includes(gradeFilter);
                var matchesLevel = levelFilter === "all" || cardLevel === levelFilter;

                if (matchesSearch && matchesGrade && matchesLevel) {
                    card.style.display = "flex";
                } else {
                    card.style.display = "none";
                }
            });

            // Filtragem das Linhas da Tabela (se a aba ativa for o Quadro Comparativo)
            var rows = activeTab.querySelectorAll(".comp-table tbody tr");
            rows.forEach(function(row) {
                var rowText = row.innerText.toLowerCase();
                if (searchInput === "" || rowText.includes(searchInput)) {
                    row.style.display = "";
                } else {
                    row.style.display = "none";
                }
            });
        }
    </script>
</body>
</html>
