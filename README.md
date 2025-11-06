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

