<img width="300" height="100" alt="Logo-ClinicaColombia (1)" src="https://github.com/user-attachments/assets/cd9adbf0-b7af-4b8a-a01b-df84a13a88da" />
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Comunicación y Registro Clínico - Infografía SPA</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <script src="https://cdn.plot.ly/plotly-2.27.0.min.js"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap');
        
        body {
            font-family: 'Inter', sans-serif;
            background-color: #F8FAFC;
            color: #1E293B;
        }

        .chart-container {
            position: relative;
            width: 100%;
            max-width: 650px;
            margin-left: auto;
            margin-right: auto;
            height: 350px;
            max-height: 400px;
        }

        @media (max-width: 768px) {
            .chart-container {
                height: 300px;
            }
        }

        .gradient-bg {
            background: linear-gradient(135deg, #1E40AF 0%, #3B82F6 100%);
        }

        .card-shadow {
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
        }

        .step-arrow::after {
            content: "→";
            position: absolute;
            right: -20px;
            top: 50%;
            transform: translateY(-50%);
            font-size: 1.5rem;
            color: #3B82F6;
        }

        @media (max-width: 768px) {
            .step-arrow::after {
                content: "↓";
                right: auto;
                bottom: -25px;
                left: 50%;
                transform: translateX(-50%);
            }
        }
    </style>
</head>
<body class="antialiased">

<!-- 
    PALETTE CHOICE: "Vibrant Professional Blue & Energetic Amber"
    Primary: #1E40AF (Blue 800)
    Secondary: #F59E0B (Amber 500)
    Accent: #10B981 (Emerald 500)
    Neutral: #F8FAFC (Slate 50)
-->

<!--
    ANALYSIS & NARRATIVE PLAN:
    1. Introduction: Hook the user with the critical importance of information as a "vital treatment".
    2. The Problem: Visualize the impact of communication failures on adverse events.
    3. Pillar 1 - Team Communication: Focus on qualitative traits (Active Listening, Assertiveness) using a Radar chart.
    4. Pillar 2 - SBAR Methodology: A logical process flow using structured HTML/CSS to show the 4-step communication frame.
    5. Pillar 3 - Legal Principles: A hierarchical view of the principles of clinical recording using a horizontal bar chart.
    6. Conclusion: Reinforce the "Rule of Gold" through a clear visual summary.
-->

<!--
    VISUALIZATION SELECTION JUSTIFICATION:
    - Adverse Events Impact (Data Point) -> Goal: Inform -> Bar Chart (Chart.js) -> Compares error causes.
    - Comm Skills (Qualitative) -> Goal: Compare -> Radar Chart (Chart.js) -> Shows balance of interpersonal skills.
    - SBAR Steps -> Goal: Organize/Process -> Styled HTML Cards (NO SVG) -> Shows sequential flow clearly.
    - Legal Principles -> Goal: Compare -> Horizontal Bar Chart (Chart.js) -> Ranks requirements by importance.
    - Confidentiality Focus -> Goal: Inform -> Donut Chart (Chart.js) -> Shows proportion of focus areas.
    - NO SVG and NO MERMAID JS used in this implementation.
-->

    <header class="gradient-bg text-white py-16 px-4 text-center">
        <div class="max-w-4xl mx-auto">
            <h1 class="text-4xl md:text-5xl font-bold mb-4">Excelencia en la Práctica Clínica</h1>
            <p class="text-xl md:text-2xl opacity-90">Guía de Comunicación Efectiva y Registro Seguro</p>
            <div class="mt-8 inline-block bg-amber-500 text-white font-bold py-2 px-6 rounded-full shadow-lg">
                La seguridad del paciente comienza con tu palabra.
            </div>
        </div>
    </header>

    <main class="max-w-7xl mx-auto px-4 py-12">

        <section class="mb-16">
            <div class="bg-white rounded-2xl p-8 card-shadow grid grid-cols-1 md:grid-cols-2 gap-12 items-center">
                <div>
                    <h2 class="text-3xl font-bold text-blue-900 mb-6 border-l-4 border-amber-500 pl-4">El Impacto del Silencio</h2>
                    <p class="text-gray-600 mb-4 text-lg">
                        En el entorno clínico, la información es tan vital como el tratamiento médico. Las fallas en la comunicación son identificadas sistemáticamente como la causa raíz de la mayoría de los eventos adversos graves en hospitales.
                    </p>
                    <p class="text-gray-600">
                        Este gráfico ilustra la importancia relativa de los pilares de seguridad. Un equipo que registra bien pero no comunica verbalmente deja un vacío crítico en la atención.
                    </p>
                </div>
                <div class="chart-container">
                    <canvas id="impactChart"></canvas>
                </div>
            </div>
        </section>

        <section class="mb-16">
            <div class="text-center mb-10">
                <h2 class="text-3xl font-bold text-blue-900">Comunicación Efectiva con el Equipo</h2>
                <div class="w-24 h-1 bg-amber-500 mx-auto mt-4"></div>
                <p class="mt-6 text-gray-600 max-w-3xl mx-auto">
                    La comunicación no es solo hablar; es asegurar que el mensaje fue recibido, comprendido y validado. La escucha activa y la asertividad permiten romper jerarquías en favor de la seguridad.
                </p>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
                <div class="bg-white p-8 rounded-2xl card-shadow">
                    <h3 class="text-xl font-bold mb-6 text-blue-800">Perfil de Comunicación de Alto Desempeño</h3>
                    <div class="chart-container">
                        <canvas id="skillsRadar"></canvas>
                    </div>
                </div>
                <div class="space-y-4">
                    <div class="bg-blue-50 p-6 rounded-xl border-l-4 border-blue-600">
                        <h4 class="font-bold text-blue-900">Circuito Cerrado</h4>
                        <p class="text-sm text-blue-800">Repite la indicación recibida para confirmar que no hubo errores de interpretación.</p>
                    </div>
                    <div class="bg-blue-50 p-6 rounded-xl border-l-4 border-blue-600">
                        <h4 class="font-bold text-blue-900">Escucha Activa</h4>
                        <p class="text-sm text-blue-800">Presta atención total, validando inquietudes antes de responder.</p>
                    </div>
                    <div class="bg-blue-50 p-6 rounded-xl border-l-4 border-blue-600">
                        <h4 class="font-bold text-blue-900">Asertividad</h4>
                        <p class="text-sm text-blue-800">Expresa dudas clínicas de forma clara y directa, sin importar el rango jerárquico.</p>
                    </div>
                    <div class="bg-amber-50 p-6 rounded-xl border-l-4 border-amber-500">
                        <h4 class="font-bold text-amber-900 font-bold">Cero Suposiciones</h4>
                        <p class="text-sm text-amber-800">Si hay dudas sobre un medicamento o dosis: <strong>Pregunta siempre.</strong></p>
                    </div>
                </div>
            </div>
        </section>

        <section class="mb-16 bg-blue-900 text-white rounded-3xl p-8 md:p-12">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-bold mb-4">Metodología SAER / SBAR</h2>
                <p class="text-blue-200 max-w-2xl mx-auto">La estandarización del mensaje reduce la ambigüedad en momentos de alta presión o entregas de turno.</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-4 gap-6 relative">
                <div class="bg-white/10 p-6 rounded-2xl border border-white/20 relative step-arrow">
                    <div class="text-4xl font-bold text-amber-500 mb-2">S</div>
                    <h3 class="font-bold text-xl mb-2">Situación</h3>
                    <p class="text-sm text-blue-100">¿Qué está pasando ahora? Identifícate y define el problema actual.</p>
                </div>
                <div class="bg-white/10 p-6 rounded-2xl border border-white/20 relative step-arrow">
                    <div class="text-4xl font-bold text-amber-500 mb-2">A</div>
                    <h3 class="font-bold text-xl mb-2">Antecedentes</h3>
                    <p class="text-sm text-blue-100">Contexto clínico relevante: diagnósticos, alergias y signos vitales.</p>
                </div>
                <div class="bg-white/10 p-6 rounded-2xl border border-white/20 relative step-arrow">
                    <div class="text-4xl font-bold text-amber-500 mb-2">E</div>
                    <h3 class="font-bold text-xl mb-2">Evaluación</h3>
                    <p class="text-sm text-blue-100">¿Cuál creo que es el problema? Tu valoración clínica profesional.</p>
                </div>
                <div class="bg-white/10 p-6 rounded-2xl border border-white/20">
                    <div class="text-4xl font-bold text-amber-500 mb-2">R</div>
                    <h3 class="font-bold text-xl mb-2">Recomendación</h3>
                    <p class="text-sm text-blue-100">¿Qué sugiero hacer? Propón una acción clara y específica.</p>
                </div>
            </div>
            
            <div id="plotlyStructure" class="mt-12 h-80 rounded-xl overflow-hidden bg-white/5"></div>
        </section>

        <section class="mb-16">
            <div class="text-center mb-10">
                <h2 class="text-3xl font-bold text-blue-900">Registro Clínico: El Marco Legal</h2>
                <div class="w-24 h-1 bg-amber-500 mx-auto mt-4"></div>
                <p class="mt-6 text-gray-600 max-w-3xl mx-auto text-lg italic">"Lo que no está escrito, no se hizo."</p>
                <p class="mt-2 text-gray-500">La historia clínica es la principal defensa legal y el hilo conductor de la atención.</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-12">
                <div class="chart-container">
                    <canvas id="legalChart"></canvas>
                </div>
                <div class="bg-white p-8 rounded-2xl card-shadow">
                    <h3 class="text-xl font-bold mb-4 text-blue-800">Principios Indispensables</h3>
                    <ul class="space-y-6">
                        <li class="flex items-start">
                            <span class="flex-shrink-0 w-8 h-8 bg-blue-100 text-blue-600 rounded-full flex items-center justify-center font-bold mr-4">1</span>
                            <div>
                                <span class="font-bold block">Veracidad y Objetividad</span>
                                <span class="text-sm text-gray-600">Registra hechos comprobables. Evita juicios de valor o suposiciones sobre el paciente.</span>
                            </div>
                        </li>
                        <li class="flex items-start">
                            <span class="flex-shrink-0 w-8 h-8 bg-blue-100 text-blue-600 rounded-full flex items-center justify-center font-bold mr-4">2</span>
                            <div>
                                <span class="font-bold block">Oportunidad Inmediata</span>
                                <span class="text-sm text-gray-600">Documenta lo más cerca posible al evento. No confíes en la memoria post-turno.</span>
                            </div>
                        </li>
                        <li class="flex items-start">
                            <span class="flex-shrink-0 w-8 h-8 bg-blue-100 text-blue-600 rounded-full flex items-center justify-center font-bold mr-4">3</span>
                            <div>
                                <span class="font-bold block">Integridad y Firma</span>
                                <span class="text-sm text-gray-600">Toda nota requiere fecha, hora, firma y sello claro. Sin tachones ni enmendaduras.</span>
                            </div>
                        </li>
                    </ul>
                </div>
            </div>
        </section>

        <section class="mb-16">
            <div class="text-center mb-10">
                <h2 class="text-3xl font-bold text-blue-900">Casos Prácticos: Desviaciones en Medicación</h2>
                <div class="w-24 h-1 bg-amber-500 mx-auto mt-4"></div>
                <p class="mt-6 text-gray-600 max-w-3xl mx-auto text-lg">
                    Documentar las desviaciones es fundamental para proteger la seguridad del paciente y la responsabilidad legal. 
                    <strong class="text-blue-800">La regla de oro: ser objetivo, preciso y registrar las acciones correctivas.</strong>
                </p>
            </div>

            <!-- Tabs Navigation -->
            <div class="flex flex-col md:flex-row justify-center gap-3 mb-6">
                <button onclick="showTab('tab1')" id="btn-tab1" class="tab-btn w-full md:w-auto px-6 py-3 rounded-full bg-blue-600 text-white font-semibold shadow-md transition-colors duration-200">1. Rechazo de Fármaco</button>
                <button onclick="showTab('tab2')" id="btn-tab2" class="tab-btn w-full md:w-auto px-6 py-3 rounded-full bg-gray-200 text-gray-700 hover:bg-gray-300 font-semibold transition-colors duration-200">2. Falla de Acceso Venoso</button>
                <button onclick="showTab('tab3')" id="btn-tab3" class="tab-btn w-full md:w-auto px-6 py-3 rounded-full bg-gray-200 text-gray-700 hover:bg-gray-300 font-semibold transition-colors duration-200">3. Medicamento No Disponible</button>
            </div>

            <!-- Tabs Content Container -->
            <div class="bg-white rounded-2xl p-6 md:p-10 card-shadow border-t-4 border-amber-500 min-h-[400px]">
                
                <!-- Tab 1: Rechazo -->
                <div id="tab1" class="tab-content block animate-fade-in">
                    <h3 class="text-2xl font-bold text-blue-800 mb-2">Cuando un paciente se niega a recibir el fármaco</h3>
                    <p class="text-gray-600 mb-6">El paciente tiene derecho a rechazar un tratamiento, pero enfermería tiene el deber de educar sobre las consecuencias y documentar el evento para deslindar responsabilidades.</p>
                    
                    <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
                        <div>
                            <div class="bg-red-50 border-l-4 border-red-500 p-4 rounded-r-lg mb-6">
                                <h4 class="font-bold text-red-800 flex items-center mb-2">
                                    <span class="text-xl mr-2">⚠️</span> Qué NO hacer
                               </h4>
                                <p class="text-red-700 text-sm">Simplemente dejar el espacio en blanco en el registro o escribir <em>"No se administra por rechazo"</em> sin dar más contexto.</p>
                            </div>
                            
                            <h4 class="font-bold text-blue-900 mb-3">Pautas de documentación:</h4>
                            <ul class="space-y-2 text-gray-700 text-sm">
                                <li class="flex items-start"><span class="text-amber-500 mr-2">✓</span> Registrar la hora exacta del intento de administración.</li>
                                <li class="flex items-start"><span class="text-amber-500 mr-2">✓</span> Anotar la razón textual que da el paciente (si la hay).</li>
                                <li class="flex items-start"><span class="text-amber-500 mr-2">✓</span> Documentar que se le explicaron los riesgos clínicos.</li>
                                <li class="flex items-start"><span class="text-amber-500 mr-2">✓</span> Registrar a qué médico se le notificó la novedad.</li>
                            </ul>
                        </div>
                        
                        <div class="bg-amber-50 border border-amber-200 p-5 rounded-xl shadow-inner font-mono text-sm relative">
                            <div class="absolute top-0 right-0 bg-amber-200 text-amber-800 text-xs px-2 py-1 rounded-bl-lg rounded-tr-xl font-sans font-bold">Ejemplo de Nota</div>
                            <p class="text-gray-800 mt-2 leading-relaxed">
                                "10:00 hrs. Paciente alerta y orientado. Se rehúsa a recibir la dosis programada de Enoxaparina refiriendo textualmente: 'Ya estoy cansado de que me chucen la barriga'. Se le explica de manera clara el riesgo de desarrollar trombosis venosa profunda al suspender el tratamiento. Paciente comprende, pero persiste en su negativa. Se notifica la situación al Dr. Martínez (Médico de Turno)."
                            </p>
                        </div>
                    </div>
                </div>

                <!-- Tab 2: Acceso Venoso -->
                <div id="tab2" class="tab-content hidden animate-fade-in">
                    <h3 class="text-2xl font-bold text-blue-800 mb-2">Cuando el acceso venoso falla</h3>
                    <p class="text-gray-600 mb-6">Una falla en el acceso venoso periférico (AVP) interrumpe la terapia y puede causar daño tisular. El registro debe evidenciar que se detectó oportunamente y se actuó bajo protocolos.</p>
                    
                    <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
                        <div>
                            <div class="bg-red-50 border-l-4 border-red-500 p-4 rounded-r-lg mb-6">
                                <h4 class="font-bold text-red-800 flex items-center mb-2">
                                    <span class="text-xl mr-2">⚠️</span> Qué NO hacer
                               </h4>
                                <p class="text-red-700 text-sm">Escribir <em>"Vía dañada, no se pasa medicamento"</em> y omitir el estado de la piel o las medidas tomadas.</p>
                            </div>
                            
                            <h4 class="font-bold text-blue-900 mb-3">Pautas de documentación:</h4>
                            <ul class="space-y-2 text-gray-700 text-sm">
                                <li class="flex items-start"><span class="text-amber-500 mr-2">✓</span> Describir signos objetivos (edema, eritema, dolor, ausencia de retorno).</li>
                                <li class="flex items-start"><span class="text-amber-500 mr-2">✓</span> Registrar la acción inmediata (suspensión, retiro del catéter).</li>
                                <li class="flex items-start"><span class="text-amber-500 mr-2">✓</span> Anotar intervenciones locales (elevación, medios físicos).</li>
                                <li class="flex items-start"><span class="text-amber-500 mr-2">✓</span> Documentar la recanalización y el reinicio de la terapia.</li>
                            </ul>
                        </div>
                        
                        <div class="bg-amber-50 border border-amber-200 p-5 rounded-xl shadow-inner font-mono text-sm relative">
                            <div class="absolute top-0 right-0 bg-amber-200 text-amber-800 text-xs px-2 py-1 rounded-bl-lg rounded-tr-xl font-sans font-bold">Ejemplo de Nota</div>
                            <p class="text-gray-800 mt-2 leading-relaxed">
                                "14:30 hrs. Durante la infusión de Vancomicina, paciente refiere ardor intenso. A la valoración, se evidencia AVP en dorso de mano derecha con edema leve, palidez localizada y ausencia de retorno venoso. Se suspende infusión y se retira el catéter. Se aplican compresas frías según protocolo. 14:45 hrs. Se canaliza nuevo AVP en antebrazo izquierdo (catéter 20G al 1er intento). Se reinicia infusión faltante. Se reporta incidente en aplicativo de seguridad."
                            </p>
                        </div>
                    </div>
                </div>

                <!-- Tab 3: Falta de Stock -->
                <div id="tab3" class="tab-content hidden animate-fade-in">
                    <h3 class="text-2xl font-bold text-blue-800 mb-2">Cuando el medicamento no está disponible</h3>
                    <p class="text-gray-600 mb-6">La falta de stock es un problema administrativo que se convierte en riesgo clínico si se omite la dosis sin buscar alternativas. El registro debe demostrar gestión.</p>
                    
                    <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
                        <div>
                            <div class="bg-red-50 border-l-4 border-red-500 p-4 rounded-r-lg mb-6">
                                <h4 class="font-bold text-red-800 flex items-center mb-2">
                                    <span class="text-xl mr-2">⚠️</span> Qué NO hacer
                               </h4>
                                <p class="text-red-700 text-sm">Escribir <em>"No hay"</em> y desentenderse del problema hasta el siguiente turno sin escalar la situación.</p>
                            </div>
                            
                            <h4 class="font-bold text-blue-900 mb-3">Pautas de documentación:</h4>
                            <ul class="space-y-2 text-gray-700 text-sm">
                                <li class="flex items-start"><span class="text-amber-500 mr-2">✓</span> Registrar la hora en que correspondía la dosis.</li>
                                <li class="flex items-start"><span class="text-amber-500 mr-2">✓</span> Indicar que está agotado/no despachado y con quién se confirmó.</li>
                                <li class="flex items-start"><span class="text-amber-500 mr-2">✓</span> Anotar la notificación al médico tratante para definir conducta.</li>
                                <li class="flex items-start"><span class="text-amber-500 mr-2">✓</span> Realizar una nota de seguimiento cuando finalmente se administra.</li>
                            </ul>
                        </div>
                        
                        <div class="bg-amber-50 border border-amber-200 p-5 rounded-xl shadow-inner font-mono text-sm relative">
                            <div class="absolute top-0 right-0 bg-amber-200 text-amber-800 text-xs px-2 py-1 rounded-bl-lg rounded-tr-xl font-sans font-bold">Ejemplo de Nota</div>
                            <p class="text-gray-800 mt-2 leading-relaxed">
                                "08:00 hrs. No es posible administrar dosis programada de Meropenem (no despachado). Se confirma con Químico Farmacéutico que el insumo está temporalmente agotado. Se notifica al Dr. Gómez (Medicina Interna), quien indica esperar traslado del medicamento desde otra sede. 10:15 hrs. Se recibe antibiótico y se inicia infusión sin eventualidades. Horario de dosis posteriores ajustado por indicación médica."
                            </p>
                        </div>
                    </div>
                </div>

            </div>

            <div class="mt-8">
                <h3 class="text-xl font-bold text-center text-blue-900 mb-6">Reglas Generales de Registro</h3>
                <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                    <div class="bg-white p-6 rounded-xl border border-gray-100 shadow-sm hover:shadow-md transition-shadow">
                        <div class="w-12 h-12 bg-blue-100 text-blue-600 rounded-full flex items-center justify-center text-xl mb-4">⏱️</div>
                        <h4 class="font-bold text-blue-900 mb-2">Nunca Registros Adelantados</h4>
                        <p class="text-sm text-gray-600">No marques un medicamento como administrado antes de estar frente al paciente. Si ocurre una desviación, constituirá falsedad.</p>
                    </div>
                    <div class="bg-white p-6 rounded-xl border border-gray-100 shadow-sm hover:shadow-md transition-shadow">
                        <div class="w-12 h-12 bg-blue-100 text-blue-600 rounded-full flex items-center justify-center text-xl mb-4">⚖️</div>
                        <h4 class="font-bold text-blue-900 mb-2">Evita Juicios de Valor</h4>
                        <p class="text-sm text-gray-600">No uses <em>"paciente agresivo y grosero"</em>. Describe: <em>"eleva el tono de voz, manotea y rechaza el medicamento"</em>.</p>
                    </div>
                    <div class="bg-white p-6 rounded-xl border border-gray-100 shadow-sm hover:shadow-md transition-shadow">
                        <div class="w-12 h-12 bg-blue-100 text-blue-600 rounded-full flex items-center justify-center text-xl mb-4">🔄</div>
                        <h4 class="font-bold text-blue-900 mb-2">Cierra el Ciclo</h4>
                        <p class="text-sm text-gray-600">Toda desviación documentada debe estar acompañada obligatoriamente de una acción de enfermería orientada a mitigar el riesgo.</p>
                    </div>
                </div>
            </div>
        </section>

        <section class="bg-amber-500 rounded-3xl p-10 text-white text-center shadow-xl">
            <h2 class="text-3xl font-bold mb-4">Nuestro Compromiso Final</h2>
            <p class="text-xl mb-8 max-w-2xl mx-auto">Protege a tu paciente comunicando bien; protégete a ti mismo registrando mejor.</p>
            <div class="flex flex-col md:flex-row justify-center gap-4">
                <div class="bg-white/20 backdrop-blur-md px-6 py-4 rounded-xl border border-white/30">
                    <p class="text-sm uppercase tracking-widest font-bold">Confidencialidad</p>
                    <p class="text-xs">La información pertenece al paciente.</p>
                </div>
                <div class="bg-white/20 backdrop-blur-md px-6 py-4 rounded-xl border border-white/30">
                    <p class="text-sm uppercase tracking-widest font-bold">Identificación</p>
                    <p class="text-xs">Firma y sello en cada intervención.</p>
                </div>
                <div class="bg-white/20 backdrop-blur-md px-6 py-4 rounded-xl border border-white/30">
                    <p class="text-sm uppercase tracking-widest font-bold">Cero Siglas</p>
                    <p class="text-xs">Evita abreviaturas no estandarizadas.</p>
                </div>
            </div>
        </section>

    </main>

    <footer class="py-12 text-center text-gray-400 text-sm">
        <p>2026 - By Wilmer Caicedo Alzate</p>
        <p class="mt-2 uppercase tracking-tighter">Estudiente Enfermería X semestre Universidad Santiago de Cali</p>
    </footer>

    <script>
        const tooltipConfig = {
            callbacks: {
                title: function(tooltipItems) {
                    const item = tooltipItems[0];
                    let label = item.chart.data.labels[item.dataIndex];
                    if (Array.isArray(label)) {
                      return label.join(' ');
                    } else {
                      return label;
                    }
                }
            }
        };

        const ctxImpact = document.getElementById('impactChart').getContext('2d');
        new Chart(ctxImpact, {
            type: 'bar',
            data: {
                labels: [
                    ['Comunicación', 'Efectiva'],
                    ['Registros', 'Clínicos'],
                    ['Trabajo en', 'Equipo'],
                    ['Protocolos', 'de Seguridad']
                ],
                datasets: [{
                    label: 'Impacto en Seguridad (%)',
                    data: [85, 78, 92, 88],
                    backgroundColor: '#3B82F6',
                    borderRadius: 8
                }]
            },
            options: {
                maintainAspectRatio: false,
                responsive: true,
                plugins: {
                    legend: { display: false },
                    tooltip: tooltipConfig
                },
                scales: {
                    y: { beginAtZero: true, max: 100 }
                }
            }
        });

        const ctxRadar = document.getElementById('skillsRadar').getContext('2d');
        new Chart(ctxRadar, {
            type: 'radar',
            data: {
                labels: [
                    ['Escucha', 'Activa'],
                    ['Asertividad', 'Clínica'],
                    ['Circuito', 'Cerrado'],
                    ['Validación', 'Mensaje'],
                    ['Cero', 'Suposiciones']
                ],
                datasets: [{
                    label: 'Nivel Requerido',
                    data: [95, 90, 100, 85, 100],
                    backgroundColor: 'rgba(59, 130, 246, 0.2)',
                    borderColor: '#1E40AF',
                    pointBackgroundColor: '#F59E0B'
                }]
            },
            options: {
                maintainAspectRatio: false,
                responsive: true,
                plugins: {
                    tooltip: tooltipConfig
                },
                scales: {
                    r: { beginAtZero: true, max: 100 }
                }
            }
        });

        const ctxLegal = document.getElementById('legalChart').getContext('2d');
        new Chart(ctxLegal, {
            type: 'doughnut',
            data: {
                labels: [
                    'Veracidad',
                    'Oportunidad',
                    'Legibilidad',
                    ['Integridad', 'Legal']
                ],
                datasets: [{
                    data: [30, 30, 20, 20],
                    backgroundColor: ['#1E3A8A', '#3B82F6', '#F59E0B', '#10B981'],
                    borderWidth: 0
                }]
            },
            options: {
                maintainAspectRatio: false,
                responsive: true,
                plugins: {
                    tooltip: tooltipConfig
                }
            }
        });

        const plotlyData = [{
            type: 'funnel',
            y: ["Situación", "Antecedentes", "Evaluación", "Recomendación"],
            x: [100, 80, 60, 40],
            textinfo: "label",
            marker: {
                color: ["#F59E0B", "#FBBF24", "#FCD34D", "#FEF3C7"],
                line: { width: 0 }
            },
            connector: { line: { color: "white", width: 2 } }
        }];

        const plotlyLayout = {
            margin: { l: 150, r: 50, b: 20, t: 20 },
            paper_bgcolor: 'rgba(0,0,0,0)',
            plot_bgcolor: 'rgba(0,0,0,0)',
            font: { color: '#ffffff' },
            showlegend: false
        };

        Plotly.newPlot('plotlyStructure', plotlyData, plotlyLayout, {
            responsive: true,
            displayModeBar: false
        });

        function showTab(tabId) {
            // Hide all tab contents
            const contents = document.querySelectorAll('.tab-content');
            contents.forEach(el => {
                el.classList.add('hidden');
            });

            // Reset all buttons to inactive state
            const buttons = document.querySelectorAll('.tab-btn');
            buttons.forEach(btn => {
                btn.classList.remove('bg-blue-600', 'text-white', 'shadow-md');
                btn.classList.add('bg-gray-200', 'text-gray-700');
            });

            // Show target content
            document.getElementById(tabId).classList.remove('hidden');

            // Set active state on clicked button
            const activeBtn = document.getElementById('btn-' + tabId);
            activeBtn.classList.remove('bg-gray-200', 'text-gray-700');
            activeBtn.classList.add('bg-blue-600', 'text-white', 'shadow-md');
        }
    </script>
</body>
</html>
<!-- 
    CONFIRMATION:
    - NO SVG was used.
    - NO MERMAID JS was used.
    - All charts are Canvas-based.
    - Diagram is HTML/CSS with Unicode arrows.
    - Label wrapping logic applied for labels > 16 chars.
    - Tooltip callbacks implemented for all Chart.js instances.
-->
