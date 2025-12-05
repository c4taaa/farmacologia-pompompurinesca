<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Módulo de Estudio Pompompurin</title>
    <!-- Carga de Tailwind CSS CDN para estilos -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Estilos personalizados para la estética Pompompurin */
        body {
            font-family: 'Inter', sans-serif;
            /* Fondo: Amarillo muy claro, color pastel de Pompompurin */
            background-color: #fff9e6; /* Creamy Yellow/Lightest Beige */
            scroll-behavior: smooth;
        }
        .text-pompom-main {
            color: #795548; /* Marrón de Pompompurin */
        }
        .bg-pompom-soft {
            background-color: #ffe082; /* Amarillo suave/Mantequilla */
        }
        .border-pompom-soft {
            border-color: #ffcc80; /* Naranja suave/Melocotón */
        }
        .bg-pompom-accent {
            background-color: #ffb74d; /* Naranja más fuerte, para botones */
        }
        .hover-bg-pompom-accent:hover {
            background-color: #ffa726; /* Tono de hover */
        }
        /* Estilos para asegurar que el contenido de la flashcard esté centrado */
        #flashcard {
            position: relative; /* Necesario para posicionar la respuesta */
        }
        #flashcard-answer {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        /* Estilos para el texto de contenido */
        .prose strong {
            font-weight: 700;
            color: #795548; /* Marrón para resaltar */
        }
        .prose ul, .prose ol {
            padding-left: 1.5em;
        }
        .prose li {
            margin-bottom: 0.5em;
        }
    </style>
    <!-- Configuración de Tailwind para usar el font 'Inter' -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    },
                    colors: {
                        'pompom-main': '#795548',
                        'pompom-soft': '#ffe082',
                        'pompom-accent': '#ffb74d',
                        'pompom-bg': '#fff9e6',
                    }
                }
            }
        }
    </script>
</head>
<body class="min-h-screen p-4 sm:p-8">

    <!-- Main Content Container -->
    <div id="app" class="max-w-5xl mx-auto bg-white shadow-xl rounded-3xl p-6 md:p-10 border-4 border-pompom-soft">

        <!-- Header Section -->
        <header class="mb-8 border-b-2 border-pompom-soft pb-4">
            <h1 class="text-4xl font-extrabold text-pompom-main tracking-tight">
                🌼 ¡A Estudiar con Pompompurin! 🍮
            </h1>
            <p id="topic-title" class="text-xl text-gray-500 mt-2">
                Reanimación Neonatal Completa (Algoritmo NRP 8ª Edición)
            </p>
        </header>

        <!-- Study Material Section -->
        <section id="study-material" class="mb-10 p-4 border border-pompom-soft rounded-xl bg-pompom-bg shadow-inner">
            <h2 class="text-2xl font-semibold text-pompom-main mb-4 flex items-center">
                <!-- Icono de libro, ahora con el color marrón de Pompompurin -->
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 mr-2 text-pompom-main" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6.253v13m0-13C10.832 5.414 9.382 5 8 5a4 4 0 000 8h4m-4-8v8m0-8h4m-4 8a4 4 0 110-8 4 4 0 010 8z" />
                </svg>
                Contenido de Estudio Detallado
            </h2>
            <div id="content-body" class="prose max-w-none text-gray-700 leading-relaxed space-y-6">
                
                <p>La reanimación neonatal (NRP) se divide en cuatro bloques secuenciales que deben respetarse, siendo los bloques A y B los más comunes y generalmente suficientes para la recuperación de la mayoría de los recién nacidos que necesitan asistencia.</p>

                <!-- BLOQUE A: Pasos Iniciales -->
                <h3 class="text-xl font-bold text-pompom-main border-b border-pompom-soft pb-1">1. 👶 Bloque A: Pasos Iniciales (Minuto de Oro)</h3>
                <p>Corresponde a los **primeros 60 segundos** de vida, cruciales para la transición. Estos pasos se realizan para evaluar y estabilizar al RN.</p>

                <h4 class="text-lg font-semibold text-pompom-main">Evaluación Inicial (3 Preguntas Clave):</h4>
                <ul class="list-disc list-inside ml-4 text-sm space-y-1">
                    <li>¿Gestación a término?</li>
                    <li>¿Buen tono?</li>
                    <li>¿Respira o llora?</li>
                </ul>
                <p class="text-sm italic text-gray-600">Si la respuesta a las 3 preguntas es **SÍ**, el RN permanece con la madre (cuidados de rutina y evaluación continua).</p>
                
                <h4 class="text-lg font-semibold text-pompom-main">Acciones (Si hay un NO):</h4>
                <ol class="list-decimal list-inside ml-4 text-sm space-y-1">
                    <li><strong>Proporcionar calor continuo y Secado</strong>.</li>
                    <li><strong>Estimular</strong> (frotar suavemente la espalda o extremidades para facilitar el esfuerzo respiratorio).</li>
                    <li><strong>Posicionar la vía aérea</strong> (posición de olfateo) .</li>
                    <li><strong>Aspirar secreciones</strong> si es necesario (Primero boca, luego nariz, con pera de goma o sonda a máx. 100 mmHg).</li>
                </ol>

                <h4 class="text-lg font-semibold text-pompom-main">Paso al Bloque B (Criterio de 30 segundos):</h4>
                <p class="text-sm">Si el RN tiene **apnea/jadeo/boqueo** o **FC &lt; 100 lpm** después de los pasos iniciales, se avanza a la ventilación (Bloque B).</p>

                <!-- BLOQUE B: VPP y MR. SOPA -->
                <h3 class="text-xl font-bold text-pompom-main border-b border-pompom-soft pb-1 mt-8">2. 🌬️ Bloque B: Ventilación a Presión Positiva (VPP)</h3>
                <p>El objetivo principal es lograr una ventilación efectiva para aumentar la FC, que es el indicador más importante de éxito.</p>
                <ul class="list-disc list-inside ml-4 text-sm space-y-1">
                    <li><strong>Indicación:</strong> FC &lt; 100 lpm o apnea/jadeo/boqueo.</li>
                    <li><strong>Frecuencia de VPP:</strong> 40 a 60 ventilaciones por minuto (Ritmo "Ventila... dos... tres").</li>
                    <li><strong>Presión Inicial (PIP):</strong> 20 a 25 cm H₂O.</li>
                    <li><strong>PEEP Inicial:</strong> 5 cm H₂O.</li>
                    <li><strong>Concentración de O₂:</strong>
                        <ul>
                            <li>RN a término (≥35 sem): 21% (Aire ambiente).</li>
                            <li>RN prematuro (&lt;35 sem): 21% a 30%.</li>
                        </ul>
                    </li>
                </ul>
                <p class="text-sm italic text-gray-600 mt-4">Si la FC no aumenta y el pecho no se mueve después de 15 segundos de VPP, se aplican los Pasos Correctivos (MR. SOPA).</p>
                
                <h4 class="text-lg font-semibold text-pompom-main">Pasos Correctivos: MR. SOPA</h4>
                <p class="text-sm">Secuencia utilizada para asegurar la ventilación:</p>
                <div class="overflow-x-auto">
                    <table class="min-w-full divide-y divide-pompom-soft rounded-lg overflow-hidden border border-pompom-accent">
                        <thead class="bg-pompom-soft">
                            <tr>
                                <th class="px-3 py-2 text-left text-xs font-medium text-pompom-main uppercase tracking-wider">Paso</th>
                                <th class="px-3 py-2 text-left text-xs font-medium text-pompom-main uppercase tracking-wider">Acción Detallada</th>
                            </tr>
                        </thead>
                        <tbody class="bg-white divide-y divide-pompom-soft text-sm">
                            <tr><td class="px-3 py-2 font-bold text-pompom-main">M (Mascara)</td><td class="px-3 py-2">Reajustar mascarilla, considerar técnica de dos manos.</td></tr>
                            <tr><td class="px-3 py-2 font-bold text-pompom-main bg-pompom-bg">R (Reposicionar)</td><td class="px-3 py-2 bg-pompom-bg">Colocar cabeza en posición neutra o ligeramente extendida.</td></tr>
                            <tr><td class="px-3 py-2 font-bold text-pompom-main">S (Succión)</td><td class="px-3 py-2">Aspirar boca y nariz.</td></tr>
                            <tr><td class="px-3 py-2 font-bold text-pompom-main bg-pompom-bg">O (Open/Abrir)</td><td class="px-3 py-2 bg-pompom-bg">Abrir la boca con cuidado.</td></tr>
                            <tr><td class="px-3 py-2 font-bold text-pompom-main">P (Presión)</td><td class="px-3 py-2">Aumentar la Presión (máx. 40 cm H₂O a término, 30 cm H₂O prematuro).</td></tr>
                            <tr><td class="px-3 py-2 font-bold text-pompom-main bg-pompom-bg">A (Alternativa)</td><td class="px-3 py-2 bg-pompom-bg">Colocar una Vía Aérea Alternativa (Tubo ET o Mascarilla Laríngea).</td></tr>
                        </tbody>
                    </table>
                </div>

                <h4 class="text-lg font-semibold text-pompom-main mt-6">Tabla de Saturación de O₂</h4>
                <div class="overflow-x-auto">
                    <table class="min-w-full divide-y divide-pompom-soft rounded-lg overflow-hidden border border-pompom-accent">
                        <thead class="bg-pompom-soft">
                            <tr>
                                <th class="px-3 py-2 text-left text-xs font-medium text-pompom-main uppercase tracking-wider">Minuto</th>
                                <th class="px-3 py-2 text-left text-xs font-medium text-pompom-main uppercase tracking-wider">Rango de Saturación (SpO₂)</th>
                            </tr>
                        </thead>
                        <tbody class="bg-white divide-y divide-pompom-soft text-sm">
                            <tr><td class="px-3 py-2">1 min</td><td class="px-3 py-2">60%–65%</td></tr>
                            <tr><td class="px-3 py-2 bg-pompom-bg">2 min</td><td class="px-3 py-2 bg-pompom-bg">65%–70%</td></tr>
                            <tr><td class="px-3 py-2">3 min</td><td class="px-3 py-2">70%–75%</td></tr>
                            <tr><td class="px-3 py-2 bg-pompom-bg">4 min</td><td class="px-3 py-2 bg-pompom-bg">75%–80%</td></tr>
                            <tr><td class="px-3 py-2">5 min</td><td class="px-3 py-2">80%–85%</td></tr>
                            <tr><td class="px-3 py-2 bg-pompom-bg">10 min</td><td class="px-3 py-2 bg-pompom-bg">85%–95%</td></tr>
                        </tbody>
                    </table>
                </div>


                <!-- BLOQUE C: Compresiones Torácicas -->
                <h3 class="text-xl font-bold text-pompom-main border-b border-pompom-soft pb-1 mt-8">3. 💪 Bloque C: Compresiones Torácicas</h3>
                <p>Se inicia si la FC es **&lt; 60 lpm** después de **30 segundos** de VPP efectiva y generalmente tras haber asegurado una vía aérea alternativa.</p>
                
                <ul class="list-disc list-inside ml-4 text-sm space-y-1">
                    <li><strong>Técnica:</strong> Dos pulgares, rodeando el torso (Técnica de los dos pulgares).</li>
                    <li><strong>Ubicación:</strong> Tercio inferior del esternón, entre la línea de los pezones y el apéndice xifoides. [Image of neonatal chest compression area]</li>
                    <li><strong>Profundidad:</strong> Deprimir 1/3 del diámetro anteroposterior del tórax.</li>
                    <li><strong>Coordinación (Ritmo):</strong> 3 Compresiones por 1 Ventilación (Ritmo 3:1).
                        <p class="mt-1 ml-4 italic">Ej: "Uno-y-dos-y-tres-y-ventila-y". Esto da 90 compresiones y 30 ventilaciones por minuto.</p>
                    </li>
                    <li><strong>Oxígeno:</strong> Se sube al 100% de O₂ al iniciar las compresiones.</li>
                    <li><strong>Evaluación:</strong> Se verifica la FC después de <strong>60 segundos</strong> de compresiones y ventilaciones coordinadas.</li>
                </ul>

                <!-- BLOQUE D: Medicamentos y Expansores -->
                <h3 class="text-xl font-bold text-pompom-main border-b border-pompom-soft pb-1 mt-8">4. 💉 Bloque D: Medicamentos y Expansores</h3>
                <p>Se llega a esta fase avanzada si la **FC persiste &lt; 60 lpm** después de 60 segundos del Bloque C.</p>

                <h4 class="text-lg font-semibold text-pompom-main">Adrenalina (Epinefrina)</h4>
                <ul class="list-disc list-inside ml-4 text-sm space-y-1">
                    <li><strong>Concentración requerida:</strong> 1:10.000. Se diluye 1 mg/1 ml en 9 ml de suero fisiológico.</li>
                    <li><strong>Vía preferida:</strong> Intravenosa (IV) a través de un Catéter Venoso Umbilical (CVU) o intraósea.</li>
                    <li><strong>Dosis IV inicial:</strong> 0.02 mg/kg (0.2 ml/kg).</li>
                    <li><strong>Administración:</strong> Rápida. Arrastrar con 3 ml de SSN si es IV. Se repite cada 3 a 5 minutos si la FC sigue &lt; 60 lpm.</li>
                </ul>

                <h4 class="text-lg font-semibold text-pompom-main">Expansor de Volumen</h4>
                <ul class="list-disc list-inside ml-4 text-sm space-y-1">
                    <li><strong>Indicación:</strong> Sospecha de pérdida de sangre aguda (shock hipovolémico) que no responde a reanimación avanzada.</li>
                    <li><strong>Solución:</strong> Solución salina normal (NaCl al 0.9%).</li>
                    <li><strong>Dosis:</strong> 10 ml/kg.</li>
                    <li><strong>Administración:</strong> Lenta (5 a 10 minutos), con extrema precaución en prematuros (&lt;32 semanas).</li>
                </ul>

            </div>
        </section>

        <!-- Interactive/Quiz Section -->
        <section id="quiz-section" class="mt-12 p-6 bg-pompom-soft border-4 border-pompom-accent rounded-3xl shadow-xl">
            <h2 class="text-2xl font-semibold text-pompom-main mb-4 flex items-center">
                <!-- Icono de bombilla (Interactivo) -->
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 mr-2 text-pompom-main" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M3.636 5.636l.707.707M7.707 10.293a1 1 0 010 1.414l-3 3a1 1 0 00-.293.707v3h3a1 1 0 00.707-.293l3-3a1 1 0 011.414 0l3 3a1 1 0 00.707.293h3v-3a1 1 0 00-.293-.707l-3-3a1 1 0 010-1.414l3-3A1 1 0 0021 7.21V4a1 1 0 00-1-1h-3.21a1 1 0 00-.707.293l-3 3a1 1 0 01-1.414 0l-3-3A1 1 0 003 4v3.21a1 1 0 00.293.707l3 3a1 1 0 010 1.414z" />
                </svg>
                ¡Flashcards del Flujograma Completo!
            </h2>
            <p class="text-pompom-main mb-4">¿Listo para recordar todos los pasos? Haz clic para probar tus conocimientos.</p>

            <!-- Interactive Flashcard Interface -->
            <div id="flashcard-container" class="mt-6 p-4 border-t border-pompom-accent">
                <div id="flashcard" class="bg-white p-6 rounded-xl shadow-lg cursor-pointer transform hover:scale-[1.01] transition duration-300 min-h-[120px] flex items-center justify-center text-center border-2 border-pompom-accent">
                    <p id="flashcard-content" class="text-lg font-medium text-pompom-main">
                        Haz clic en el botón para comenzar.
                    </p>
                    <p id="flashcard-answer" class="text-lg font-medium text-pompom-main hidden absolute bg-pompom-bg p-4 rounded-xl shadow-inner border border-pompom-accent">
                        <!-- Answer will be shown here -->
                    </p>
                </div>
                
                <div class="mt-4 flex flex-col sm:flex-row justify-center space-y-2 sm:space-y-0 sm:space-x-4">
                    <button id="next-card-btn" class="bg-pompom-accent hover-bg-pompom-accent text-pompom-main font-bold py-2 px-6 rounded-lg transition duration-300 shadow-md hover:shadow-lg focus:outline-none focus:ring-4 focus:ring-pompom-soft">
                        Siguiente Tarjeta
                    </button>
                    <button id="show-answer-btn" class="bg-pompom-main hover:bg-gray-700 text-white font-bold py-2 px-6 rounded-lg transition duration-300 shadow-md hover:shadow-lg focus:outline-none focus:ring-4 focus:ring-pompom-accent">
                        Mostrar Respuesta
                    </button>
                </div>
            </div>
        </section>

    </div>

    <script>
        // JavaScript Logic for the interactive Pompompurin learning page
        
        document.addEventListener('DOMContentLoaded', () => {
            const topicTitleElement = document.getElementById('topic-title');
            const contentBodyElement = document.getElementById('content-body');
            const flashcardContainer = document.getElementById('flashcard-container');
            const flashcardElement = document.getElementById('flashcard');
            const flashcardContent = document.getElementById('flashcard-content');
            const flashcardAnswer = document.getElementById('flashcard-answer');
            const nextCardBtn = document.getElementById('next-card-btn');
            const showAnswerBtn = document.getElementById('show-answer-btn');

            // --- 1. Flashcard Data (Key Concepts from all Blocks) ---
            const flashcards = [
                { question: "Bloque A: ¿Bajo qué condiciones de las 3 preguntas iniciales se inicia la Reanimación (no rutinaria)?", answer: "Si el RN NO está a término, NO tiene buen tono, o NO respira/llora." },
                { question: "Bloque A: ¿Cuál es la secuencia correcta de succión de secreciones?", answer: "Primero boca, luego nariz." },
                { question: "Bloque B: ¿Cuál es el principal indicador de éxito de la VPP?", answer: "El aumento de la Frecuencia Cardíaca (FC)." },
                { question: "Bloque B: ¿Cuál es la indicación principal para iniciar la VPP?", answer: "FC menor a 100 lpm, o si hay apnea/jadeo/boqueo." },
                { question: "Bloque B: ¿Qué presión (P) de MR. SOPA es la máxima para un RN a término?", answer: "40 cm H₂O (máximo, se aumenta en incrementos de 5 a 10 cm H₂O)." },
                { question: "Bloque C: ¿En qué punto de FC se comienza con Compresiones Torácicas?", answer: "Si la FC persiste menor a 60 lpm después de 30 segundos de VPP efectiva." },
                { question: "Bloque C: ¿Cuál es la coordinación (ritmo) entre Compresiones y Ventilación?", answer: "3 Compresiones por 1 Ventilación (Ritmo 3:1)."},
                { question: "Bloque C: ¿Qué concentración de O₂ se debe usar al iniciar las Compresiones?", answer: "100% de Oxígeno." },
                { question: "Bloque D: ¿Cuál es la concentración requerida para la Adrenalina IV en RN?", answer: "1:10.000 (0.1 mg/ml, diluyendo 1 ampolla de 1:1.000 en 9ml de SSN)." },
                { question: "Bloque D: ¿Cuál es la dosis IV inicial de Adrenalina?", answer: "0.02 mg/kg (0.2 ml/kg)." },
                { question: "Bloque D: ¿Cuál es la dosis de Expansor de Volumen (Solución Salina Normal)?", answer: "10 ml/kg, administrado lentamente (5 a 10 minutos)." },
            ];

            let currentCardIndex = -1;
            let showingAnswer = false;

            // --- 2. Flashcard Logic ---

            function displayCard() {
                // Check if we are starting for the first time
                if (currentCardIndex === -1) {
                    flashcardContent.textContent = "Haz clic en 'Siguiente Tarjeta' para empezar.";
                    flashcardAnswer.textContent = "Presiona 'Mostrar Respuesta' para ver la solución.";
                    return;
                }

                // Loop back to the start if we finished all cards
                if (currentCardIndex >= flashcards.length) {
                    currentCardIndex = 0; // Loop back to the first card
                }
                
                flashcardContent.textContent = flashcards[currentCardIndex].question;
                flashcardAnswer.textContent = flashcards[currentCardIndex].answer;

                // Reset display state
                flashcardAnswer.classList.add('hidden');
                flashcardContent.classList.remove('hidden');
                showAnswerBtn.textContent = "Mostrar Respuesta";
                showingAnswer = false;
            }
            
            function showAnswer() {
                if (currentCardIndex === -1) {
                    // Start the game if not started on 'Show Answer' button click
                    currentCardIndex = 0;
                    displayCard();
                    return;
                }
                
                flashcardContent.classList.add('hidden');
                flashcardAnswer.classList.remove('hidden');
                showAnswerBtn.textContent = "Respuesta Mostrada";
                showingAnswer = true;
            }

            // Event Listeners
            nextCardBtn.addEventListener('click', () => {
                if (currentCardIndex === -1) {
                    currentCardIndex = 0; // Start at first card
                } else {
                    currentCardIndex++; // Move to next card
                }
                displayCard();
            });

            showAnswerBtn.addEventListener('click', showAnswer);
            
            // Initial state setup
            displayCard();
        });
    </script>
</body>
</html>
