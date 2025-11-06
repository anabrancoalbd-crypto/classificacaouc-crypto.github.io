# classificacaouc-crypto.github.io
Classificação UC Integral ou Sustentável
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Classificação UC: Integral ou Sustentável</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700;800&display=swap" rel="stylesheet">
    <!-- Adicionando Font Awesome para o ícone de próxima questão e feedback -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <style>
        /* ------------------------------------------- */
        /* CSS GERAL E DECORAÇÕES (AGORA MUITO MAIS VERDE) */
        /* ------------------------------------------- */
        body {
            font-family: 'Poppins', sans-serif;
            /* Fundo de floresta profunda: Gradiente de verde médio a verde musgo escuro */
            background: linear-gradient(135deg, #56AB2F 0%, #388E3C 70%, #1B5E20 100%); 
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            /* REMOVIDO: padding: 20px; PARA OCUPAR 100% DA TELA */
            position: relative;
            overflow: hidden; 
        }
        .container-quiz {
            max-width: 650px;
            width: 90%; /* Ajustado para 90% para garantir margem em telas pequenas */
            background-color: #ffffff;
            border-radius: 20px;
            /* Sombra mais orgânica e elevada, com destaque verde profundo */
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.4), 0 0 20px rgba(27, 94, 32, 0.9); 
            padding: 40px;
            text-align: center;
            /* Borda Verde Floresta Escura */
            border: 5px solid #1B5E20; 
            position: relative;
            z-index: 10; 
            margin: 20px; /* Adicionado margem para garantir que o container não encoste nas bordas */
        }

        /* DECORAÇÕES DE FOLHAGEM ABSTRATA AO REDOR DO QUIZ */
        .decoration-leaf {
            position: absolute;
            width: 30px;
            height: 30px;
            border-radius: 0 50% 50% 50%; 
            transform: rotate(45deg);
            opacity: 0.6; /* Aumentado levemente a opacidade para mais presença */
            z-index: 1;
            animation: float 10s infinite linear alternate;
        }
        /* Variações de folhas para profundidade (Cores mais intensas) */
        .leaf-primary { background-color: #4CAF50; width: 45px; height: 45px; opacity: 0.7; } /* Mais visível */
        .leaf-secondary { background-color: #81C784; width: 30px; height: 30px; opacity: 0.5; } /* Verde claro */
        .leaf-dark { background-color: #1E8449; width: 35px; height: 35px; opacity: 0.8; } /* Verde escuro */


        @keyframes float {
            0% { transform: translate(0, 0) rotate(45deg); }
            50% { transform: translate(var(--x-translate), var(--y-translate)) rotate(var(--rotate-end)); }
            100% { transform: translate(0, 0) rotate(45deg); }
        }
        
        /* ESTILOS DA CAIXA DE PERGUNTA (SIMULANDO PLACA/PERGAMINHO) */
        #question-box {
            /* Fundo simulando um pergaminho ou papel natural */
            background: #fdfcf7; 
            /* Borda verde médio */
            border: 4px solid #81C784; 
            padding: 30px; 
            border-radius: 15px;
            /* Sombra interna para dar um efeito de profundidade de placa */
            box-shadow: 0 0 0 5px rgba(255, 255, 255, 0.7) inset, 0 4px 8px rgba(0, 0, 0, 0.1); 
            margin-bottom: 30px;
            transition: all 0.3s ease;
        }
        #question-text {
            font-size: 1.6rem;
            /* Texto da pergunta em verde escuro quase preto (teal dark) */
            color: #004D40; 
            line-height: 1.5;
            margin-bottom: 15px;
            font-weight: 700;
        }
        
        /* ESTILOS ADICIONAIS */
        .container-quiz h1 {
            /* Título mais verde */
            color: #004D40; 
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.2);
            animation: pulse-light 2s infinite alternate;
        }
        @keyframes pulse-light {
            from { opacity: 0.9; }
            to { opacity: 1; }
        }


        /* ESTILOS DE BOTÕES E FEEDBACK */
        .btn-game {
            transition: all 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275); /* Efeito "pulo" ao clicar */
            padding: 14px 28px;
            font-size: 1.25rem;
            font-weight: 700;
            border: none;
            border-radius: 12px;
            cursor: pointer;
            margin: 12px;
            box-shadow: 0 8px #1a202c; /* Aumentado o box-shadow padrão */
            transform: translateY(0);
            text-shadow: 1px 1px 2px rgba(0,0,0,0.4);
        }
        /* Botão Integral agora com verde mais clássico e forte */
        .btn-integral {
            background: linear-gradient(45deg, #388E3C, #4CAF50);
            color: white;
            box-shadow: 0 6px #1B5E20; /* Sombra verde escura */
        }
        .btn-integral:hover {
            background: linear-gradient(45deg, #4CAF50, #388E3C);
            transform: translateY(-4px);
            box-shadow: 0 10px #1B5E20;
        }
        /* Botão Sustentável (Azul) mantido para contraste, mas com sombra mais escura */
        .btn-sustentavel {
            background: linear-gradient(45deg, #3498db, #2980b9);
            color: white;
            box-shadow: 0 6px #20619a;
        }
        .btn-sustentavel:hover {
            background: linear-gradient(45deg, #2980b9, #3498db);
            transform: translateY(-4px);
            box-shadow: 0 10px #20619a;
        }
        .btn-next {
            background: linear-gradient(45deg, #ff8c00, #ff6f00);
            color: white;
            box-shadow: 0 6px #cc5a00;
        }
        .btn-next:hover {
            background: linear-gradient(45deg, #ff6f00, #ff8c00);
            transform: translateY(-4px);
            box-shadow: 0 10px #cc5a00;
        }
        .btn-game:active {
            transform: translateY(3px);
            box-shadow: 0 3px #1a202c;
        }
        #feedback {
            margin-top: 25px;
            padding: 18px;
            border-radius: 12px;
            font-weight: 700;
            font-size: 1.1rem;
            animation: fadeIn 0.5s ease-out;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
        
        /* Animações de Feedback mais nítidas */
        @keyframes pulseCorrect {
            0% { transform: scale(1); box-shadow: 0 0 0 0 rgba(76, 175, 80, 0.7); } /* Verde forte */
            70% { transform: scale(1.02); box-shadow: 0 0 0 15px rgba(76, 175, 80, 0); }
            100% { transform: scale(1); }
        }

        @keyframes shakeIncorrect {
            0%, 100% { transform: translateX(0); }
            20%, 60% { transform: translateX(-15px); }
            40%, 80% { transform: translateX(15px); }
        }

        .correct {
            /* Fundo verde claro e texto verde musgo */
            background: linear-gradient(90deg, #e6ffe6, #b3ffb3);
            color: #1B5E20;
            border: 2px solid #4CAF50;
            animation: fadeIn 0.5s ease-out, pulseCorrect 1s ease-out;
        }
        .incorrect {
            background: linear-gradient(90deg, #ffe6e6, #ffb3b3);
            color: #8b0000;
            border: 2px solid #e74c3c;
            animation: fadeIn 0.1s ease-out, shakeIncorrect 0.5s ease-out;
        }
        .box-flash-correct {
            animation: pulseCorrect 1s ease-out;
        }
        .box-shake-incorrect {
            animation: shakeIncorrect 0.5s ease-out;
            border-color: #e74c3c !important;
        }
        .final-score {
            font-size: 2.5rem;
            font-weight: 800;
            /* Texto da pontuação em verde escuro */
            color: #004D40;
            margin-bottom: 25px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
        }
        
        /* ESTILO DO GABARITO (COM ROLAGEM) */
        #answer-summary {
            max-height: 350px; 
            overflow-y: auto; 
            padding-right: 15px; 
            text-align: left;
            margin-top: 32px; 
            padding: 20px; 
            background-color: #f0fff0; /* Fundo muito claro e agradável */
            border-radius: 12px; 
            border: 1px solid #d4edda; 
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.05); /* Sombra suave */
        }
        #answer-summary::-webkit-scrollbar {
            width: 8px;
        }
        #answer-summary::-webkit-scrollbar-thumb {
            background-color: #388E3C; /* Verde da Floresta */
            border-radius: 10px;
        }
        #answer-summary::-webkit-scrollbar-track {
            background: #e6ffe6;
            border-radius: 10px;
        }
        .summary-item {
            border-left: 5px solid #4CAF50; /* Borda Verde Forte */
            background-color: #ffffff;
            transition: transform 0.2s;
        }
        .summary-item:hover {
            transform: translateX(5px);
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(-10px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body>
<!-- Decorações de Folhagem Flutuante (Mais variadas e mais verdes) -->
<div class="decoration-leaf leaf-primary" style="top: 10%; left: 5%; --x-translate: 20px; --y-translate: -30px; --rotate-end: 25deg; animation-duration: 12s;"></div>
<div class="decoration-leaf leaf-secondary" style="top: 80%; left: 15%; animation-delay: 3s; animation-duration: 15s; --x-translate: 0px; --y-translate: -15px; --rotate-end: 120deg;"></div>
<div class="decoration-leaf leaf-dark" style="top: 30%; right: 10%; animation-delay: 5s; animation-duration: 10s; --x-translate: -25px; --y-translate: 5px; --rotate-end: 200deg;"></div>
<div class="decoration-leaf leaf-primary" style="bottom: 5%; right: 25%; animation-delay: 1s; animation-duration: 13s; --x-translate: 15px; --y-translate: 25px; --rotate-end: 300deg;"></div>
<div class="decoration-leaf leaf-secondary" style="top: 50%; left: 20%; animation-delay: 7s; animation-duration: 18s; --x-translate: 5px; --y-translate: -20px; --rotate-end: 90deg;"></div>
<div class="decoration-leaf leaf-dark" style="bottom: 15%; left: 5%; animation-delay: 2s; animation-duration: 11s; --x-translate: -20px; --y-translate: 15px; --rotate-end: 50deg;"></div>

<!-- NOVAS FOLHAS (Mais verde) -->
<div class="decoration-leaf leaf-dark" style="top: 20%; right: 30%; animation-delay: 4s; animation-duration: 16s; --x-translate: -10px; --y-translate: 10px; --rotate-end: 150deg;"></div>
<div class="decoration-leaf leaf-primary" style="bottom: 30%; left: 40%; animation-delay: 9s; animation-duration: 14s; --x-translate: 10px; --y-translate: -10px; --rotate-end: 250deg;"></div>
<div class="decoration-leaf leaf-secondary" style="top: 5%; left: 45%; animation-delay: 0s; animation-duration: 9s; --x-translate: -5px; --y-translate: 5px; --rotate-end: 60deg;"></div>
<div class="decoration-leaf leaf-dark" style="bottom: 10%; right: 5%; animation-delay: 6s; animation-duration: 17s; --x-translate: 5px; --y-translate: 20px; --rotate-end: 320deg;"></div>

<!-- Fim das Decorações -->

<div class="container-quiz">
    <!-- Título em verde escuro -->
    <h1 class="text-4xl font-extrabold text-[#004D40] mb-5 animate-pulse">Classificação UC: Integral ou Sustentável</h1>
    <p class="text-lg text-gray-700 mb-6" id="score-display">Pontuação: 0 | Questão: 1 / 15</p>

    <div id="game-area">
        <div id="question-box">
            <h2 id="question-text"></h2>
            <p id="scenario-details"></p>
        </div>
        
        <!-- INSTRUÇÃO CLARA DAS ALTERNATIVAS FIXAS -->
        <p class="text-xl font-semibold text-gray-700 mb-4" id="instruction-text">Classifique a UC como:</p>

        <div id="button-area" class="flex justify-center gap-6">
            <button class="btn-game btn-integral" id="btn-integral" onclick="checkAnswer('Proteção Integral')">Proteção Integral</button>
            <button class="btn-game btn-sustentavel" id="btn-sustentavel" onclick="checkAnswer('Uso Sustentável')">Uso Sustentável</button>
            
            <!-- Botão de Próxima Questão (Inicialmente escondido) -->
            <button class="btn-game btn-next" id="btn-next" style="display:none;" onclick="nextQuestion()">
                Próxima Questão <i class="fa-solid fa-arrow-right-long ml-2"></i>
            </button>
        </div>

        <div id="feedback"></div>
    </div>

    <div id="end-message" class="hidden">
        <!-- Título em verde escuro -->
        <h2 class="text-3xl font-bold text-[#004D40] mb-4">Fim do Jogo!</h2>
        <p class="final-score" id="final-score-text"></p>
        
        <!-- Nova seção para exibir as respostas corretas -->
        <div id="answer-summary">
            <!-- O sumário será inserido aqui pelo JavaScript -->
        </div>
        
        <button class="btn-game btn-sustentavel mt-6" onclick="startGame()">Jogar Novamente</button>
    </div>
</div>

<script>
    const questions = [
        {
            scenario: "1. Parque Nacional de Jericoacoara. Atividade: Visitação turística, proibida a moradia e extração.",
            type: "Proteção Integral",
            details: "Permite visitação e educação, mas proíbe o uso direto dos recursos (uso indireto)."
        },
        {
            scenario: "2. Reserva Extrativista (RESEX). Atividade: Coleta de açaí e castanha por comunidades locais.",
            type: "Uso Sustentável",
            details: "Concilia a conservação com o uso sustentável dos recursos pelas populações tradicionais."
        },
        {
            scenario: "3. Estação Ecológica (ESEC). Atividade: Acesso restrito apenas para pesquisa científica.",
            type: "Proteção Integral",
            details: "Preservação integral, proibindo qualquer uso ou visitação que não seja para pesquisa."
        },
        {
            scenario: "4. Floresta Nacional (FLONA). Atividade: Extração legal e planejada de madeira (manejo florestal).",
            type: "Uso Sustentável",
            details: "Permite o uso múltiplo, mas sustentável, dos recursos florestais."
        },
        {
            scenario: "5. Reserva Biológica (REBIO). Atividade: Proibida a caça e qualquer alteração no ambiente.",
            type: "Proteção Integral",
            details: "Objetivo é a preservação total, sendo o uso dos recursos naturais proibido."
        },
        {
            scenario: "6. Área de Proteção Ambiental (APA). Atividade: Uso sustentável e ordenamento de ocupação humana.",
            type: "Uso Sustentável",
            details: "Permite a ocupação humana e atividades econômicas sob regras de sustentabilidade e zoneamento."
        },
        {
            scenario: "7. Reserva Particular do Patrimônio Natural (RPPN). Atividade: Propriedade privada dedicada à conservação e pesquisa.",
            type: "Uso Sustentável",
            details: "É uma UC privada que visa a conservação, mas permite atividades de baixo impacto (visitação, pesquisa) e está classificada como Uso Sustentável."
        },
        {
            scenario: "8. Reserva de Desenvolvimento Sustentável (RDS). Atividade: Manejo dos recursos por populações tradicionais em regime de cooperação.",
            type: "Uso Sustentável",
            details: "Visa a melhoria da qualidade de vida e a exploração sustentável dos recursos naturais pelas populações locais."
        },
        {
            scenario: "9. Monumento Natural (MONA). Atividade: Proteção de um local singular e permitida a visitação.",
            type: "Proteção Integral",
            details: "Protege sítios naturais raros ou únicos; permite visitação, mas proíbe atividades de uso direto dos recursos."
        },
        {
            scenario: "10. Área de Relevante Interesse Ecológico (ARIE). Atividade: Protege áreas pequenas, mas importantes, permitindo ocupação sob regras.",
            type: "Uso Sustentável",
            details: "Protege ambientes naturais de importância regional, geralmente mantendo a ocupação humana existente, mas sob forte regulação."
        },
        {
            scenario: "11. Refúgio de Vida Silvestre (REVIS). Atividade: Proteção de ambientes naturais necessários para a reprodução de espécies.",
            type: "Proteção Integral",
            details: "Foco na proteção de espécies e ambientes essenciais, exigindo medidas rigorosas de controle de acesso e uso."
        },
        {
            scenario: "12. Pergunta conceitual: Qual grupo proíbe a extração de recursos, exceto para pesquisa?",
            type: "Proteção Integral",
            details: "O grupo de Proteção Integral (Parques, ESECs, REBIOs) tem como regra o uso indireto dos recursos, ou seja, sem extração."
        },
        {
            scenario: "13. Pergunta conceitual: Qual grupo busca compatibilizar a conservação da natureza com o uso sustentável de parte de seus recursos?",
            type: "Uso Sustentável",
            details: "O grupo de Uso Sustentável permite a exploração planejada e responsável dos recursos naturais (uso direto)."
        },
        {
            scenario: "14. Qual UC, que permite visitação, tem como foco a preservação da natureza sem exploração comercial de recursos?",
            type: "Proteção Integral",
            details: "O Parque Nacional permite turismo e é a UC de Proteção Integral mais acessível ao público, mas não permite exploração dos recursos."
        },
        {
            scenario: "15. Qual tipo de UC é estabelecido em área de domínio privado, mas com a concordância do proprietário para conservação?",
            type: "Uso Sustentável",
            details: "RPPN (Reserva Particular do Patrimônio Natural), que faz parte do grupo de Uso Sustentável por ser privada e depender da anuência do dono, embora seu foco seja a preservação."
        }
    ];

    let currentQuestionIndex = 0;
    let score = 0;
    // O total de questões foi atualizado para 15
    const totalQuestions = 15;

    const questionText = document.getElementById('question-text');
    const scenarioDetails = document.getElementById('scenario-details');
    const scoreDisplay = document.getElementById('score-display');
    const feedbackDiv = document.getElementById('feedback');
    const gameArea = document.getElementById('game-area');
    const endMessage = document.getElementById('end-message');
    const finalScoreText = document.getElementById('final-score-text');
    const buttonArea = document.getElementById('button-area');
    const questionBox = document.getElementById('question-box');
    
    // Referências aos botões
    const btnIntegral = document.getElementById('btn-integral');
    const btnSustentavel = document.getElementById('btn-sustentavel');
    const btnNext = document.getElementById('btn-next');
    const answerSummaryDiv = document.getElementById('answer-summary'); // Novo elemento


    function shuffleArray(array) {
        for (let i = array.length - 1; i > 0; i--) {
            const j = Math.floor(Math.random() * (i + 1));
            [array[i], array[j]] = [array[j], array[i]];
        }
    }

    function startGame() {
        // A função shuffleArray está sendo aplicada ao array questions.
        // Isso garante que a ordem das perguntas seja aleatória a cada jogo.
        shuffleArray(questions);
        currentQuestionIndex = 0;
        score = 0;
        gameArea.classList.remove('hidden');
        endMessage.classList.add('hidden');
        answerSummaryDiv.innerHTML = ''; // Limpa o gabarito ao reiniciar
        showQuestion();
    }

    function showQuestion() {
        if (currentQuestionIndex < totalQuestions) {
            const q = questions[currentQuestionIndex];
            questionText.textContent = q.scenario;
            scenarioDetails.textContent = ''; 
            scoreDisplay.textContent = `Pontuação: ${score} | Questão: ${currentQuestionIndex + 1} / ${totalQuestions}`;
            feedbackDiv.textContent = '';
            feedbackDiv.className = '';
            
            // Exibe botões de resposta, esconde o botão de próxima
            btnIntegral.style.display = 'inline-block';
            btnSustentavel.style.display = 'inline-block';
            btnNext.style.display = 'none';

            buttonArea.classList.remove('pointer-events-none'); // Reativa botões de resposta
        } else {
            endGame();
        }
    }

    function checkAnswer(userAnswer) {
        const q = questions[currentQuestionIndex];
        const isCorrect = userAnswer === q.type;

        // Desativa os botões de resposta
        btnIntegral.style.display = 'none';
        btnSustentavel.style.display = 'none';
        
        // Exibe feedback
        if (isCorrect) {
            score++;
            feedbackDiv.textContent = `✅ CORRETO! É uma UC de ${q.type}.`;
            feedbackDiv.className = 'correct';
            questionBox.classList.add('box-flash-correct');
        } else {
            // A resposta incorreta agora mostra o tipo correto e a justificativa
            feedbackDiv.textContent = `❌ ERRADO! A resposta correta era ${q.type}. Lembre-se: ${q.details}`;
            feedbackDiv.className = 'incorrect';
            questionBox.classList.add('box-shake-incorrect');
        }

        scoreDisplay.textContent = `Pontuação: ${score} | Questão: ${currentQuestionIndex + 1} / ${totalQuestions}`;

        // Exibe o botão de "Próxima Questão"
        btnNext.style.display = 'inline-block';
    }

    function nextQuestion() {
        // Remove as classes de animação da caixa da pergunta
        questionBox.classList.remove('box-flash-correct', 'box-shake-incorrect');
        
        // Avança a questão
        currentQuestionIndex++;
        showQuestion();
    }
    
    // Função: Gera o gabarito completo no final
    function generateAnswerSummary() {
        let summaryHTML = '<h3 class="text-2xl font-bold mb-4 text-[#004D40]">Gabarito Completo:</h3>';

        // O loop itera sobre todas as 15 perguntas
        questions.forEach((q, index) => {
            // Utilizamos o índice + 1 para a numeração, mesmo após o shuffle
            summaryHTML += `
                <div class="mb-4 p-3 shadow-sm rounded-lg summary-item">
                    <p class="font-bold text-lg mb-1 text-gray-800">Questão ${index + 1}:</p>
                    <p class="text-gray-700 italic">${q.scenario.substring(q.scenario.indexOf(' ') + 1)}</p>
                    <p class="mt-1">
                        <span class="font-extrabold text-green-700">Resposta Correta:</span> ${q.type}
                    </p>
                    <p class="text-sm text-gray-600 mt-1">
                        <span class="font-semibold">Justificativa:</span> ${q.details}
                    </p>
                </div>
            `;
        });

        answerSummaryDiv.innerHTML = summaryHTML;
    }

    function endGame() {
        gameArea.classList.add('hidden');
        endMessage.classList.remove('hidden');
        finalScoreText.textContent = `Você acertou ${score} de ${totalQuestions} questões!`;
        
        // Chama a função para exibir o gabarito completo
        generateAnswerSummary(); 
    }

    // Iniciar o jogo ao carregar
    window.onload = startGame;

</script>
</body>
</html>
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            /* REMOVIDO: padding: 20px; PARA OCUPAR 100% DA TELA */
            position: relative;
            overflow: hidden; 
        }
        .container-quiz {
            max-width: 650px;
            width: 90%; /* Ajustado para 90% para garantir margem em telas pequenas */
            background-color: #ffffff;
            border-radius: 20px;
            /* Sombra mais orgânica e elevada, com destaque verde profundo */
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.4), 0 0 20px rgba(27, 94, 32, 0.9); 
            padding: 40px;
            text-align: center;
            /* Borda Verde Floresta Escura */
            border: 5px solid #1B5E20; 
            position: relative;
            z-index: 10; 
            margin: 20px; /* Adicionado margem para garantir que o container não encoste nas bordas */
        }

        /* DECORAÇÕES DE FOLHAGEM ABSTRATA AO REDOR DO QUIZ */
        .decoration-leaf {
            position: absolute;
            width: 30px;
            height: 30px;
            border-radius: 0 50% 50% 50%; 
            transform: rotate(45deg);
            opacity: 0.6; /* Aumentado levemente a opacidade para mais presença */
            z-index: 1;
            animation: float 10s infinite linear alternate;
        }
        /* Variações de folhas para profundidade (Cores mais intensas) */
        .leaf-primary { background-color: #4CAF50; width: 45px; height: 45px; opacity: 0.7; } /* Mais visível */
        .leaf-secondary { background-color: #81C784; width: 30px; height: 30px; opacity: 0.5; } /* Verde claro */
        .leaf-dark { background-color: #1E8449; width: 35px; height: 35px; opacity: 0.8; } /* Verde escuro */

