<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portafolio de Proyectos</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 20px;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
            overflow: hidden;
        }

        .header {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 40px;
            text-align: center;
        }

        .header h1 {
            font-size: 2.5em;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.2);
        }

        .header p {
            font-size: 1.2em;
            opacity: 0.9;
        }

        .tabs {
            display: flex;
            background: #f8f9fa;
            border-bottom: 3px solid #667eea;
            overflow-x: auto;
        }

        .tab {
            padding: 20px 30px;
            cursor: pointer;
            background: transparent;
            border: none;
            font-size: 16px;
            font-weight: 600;
            color: #666;
            transition: all 0.3s ease;
            white-space: nowrap;
            position: relative;
        }

        .tab:hover {
            background: rgba(102, 126, 234, 0.1);
            color: #667eea;
        }

        .tab.active {
            color: #667eea;
            background: white;
        }

        .tab.active::after {
            content: '';
            position: absolute;
            bottom: -3px;
            left: 0;
            right: 0;
            height: 3px;
            background: #667eea;
        }

        .content {
            padding: 40px;
        }

        .tab-content {
            display: none;
            animation: fadeIn 0.5s ease;
        }

        .tab-content.active {
            display: block;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .project-card {
            background: white;
            border-radius: 15px;
            padding: 25px;
            margin-bottom: 25px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.15);
        }

        .project-card h3 {
            color: #667eea;
            margin-bottom: 15px;
            font-size: 1.5em;
        }

        .project-image {
            width: 100%;
            max-width: 600px;
            height: auto;
            border-radius: 10px;
            margin: 15px 0;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        .btn-link {
            display: inline-block;
            padding: 12px 25px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            text-decoration: none;
            border-radius: 25px;
            margin-top: 15px;
            font-weight: 600;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(102, 126, 234, 0.3);
        }

        .btn-link:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(102, 126, 234, 0.4);
        }

        .grid-images {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin: 20px 0;
        }

        .grid-images img {
            width: 100%;
            height: 250px;
            object-fit: cover;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }

        .grid-images img:hover {
            transform: scale(1.05);
        }

        .badge {
            display: inline-block;
            padding: 5px 15px;
            background: #667eea;
            color: white;
            border-radius: 20px;
            font-size: 0.85em;
            margin-right: 10px;
            margin-bottom: 10px;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>🚀 Portafolio de Proyectos</h1>
            <p>Ingeniería y Fabricación Digital - Semana 2</p>
        </div>

        <div class="tabs">
            <button class="tab active" onclick="openTab(event, 'solidworks')">SolidWorks</button>
            <button class="tab" onclick="openTab(event, 'idit')">Visita IDIT</button>
            <button class="tab" onclick="openTab(event, 'laser')">Corte Láser</button>
            <button class="tab" onclick="openTab(event, 'impresion3d')">Impresión 3D</button>
            <button class="tab" onclick="openTab(event, 'metal')">Corte de Lámina</button>
            <button class="tab" onclick="openTab(event, 'escaneo')">Escaneo 3D</button>
        </div>

        <div class="content">
            <!-- SolidWorks Tab -->
            <div id="solidworks" class="tab-content active">
                <div class="project-card">
                    <h3>📘 Syllabus del Curso</h3>
                    ![Diagrama del sistema](recursos/imgs/Whtssyll.jpg)
                </div>

                <div class="project-card">
                    <h3>📝 Tarea 1</h3>
                    <span class="badge">SolidWorks</span>
                    <img src="recursos/imgs/CapturaSldTarea1.png" alt="Tarea 1" class="project-image">
                    <a href="https://iberopuebla-my.sharepoint.com/:u:/g/personal/203599_iberopuebla_mx/Eb8R9IEmgOlIoTJIxipH2QUBdf1OQik5LTwOIDPUnIOe_w?e=Bknjgt" class="btn-link" target="_blank">Ver Archivo</a>
                </div>

                <div class="project-card">
                    <h3>🔧 Ejercicio 3</h3>
                    <span class="badge">SolidWorks</span>
                    <img src="recursos/imgs/CapturaSldEj3.png" alt="Ejercicio 3" class="project-image">
                    <a href="https://iberopuebla-my.sharepoint.com/:u:/g/personal/203599_iberopuebla_mx/EZqiuaQncBZAqdMaiTxne-sBO_lrMAziB6y18CshPJj4rg?e=t0laoq" class="btn-link" target="_blank">Ver Archivo</a>
                </div>

                <div class="project-card">
                    <h3>⚙️ Ejercicio 5</h3>
                    <span class="badge">SolidWorks</span>
                    <img src="recursos/imgs/CapturaSldEj5.png" alt="Ejercicio 5" class="project-image">
                    <a href="https://iberopuebla-my.sharepoint.com/:u:/g/personal/203599_iberopuebla_mx/EbFFcYND34pPuvw7OiX5H0YBzlhFvyqvbEXo9-txtcCt2g?e=iEIuX6" class="btn-link" target="_blank">Ver Archivo</a>
                </div>

                <div class="project-card">
                    <h3>🌺 Florero</h3>
                    <span class="badge">Diseño</span>
                    <img src="recursos/imgs/CapturaSldFlorero.png" alt="Florero" class="project-image">
                    <a href="https://iberopuebla-my.sharepoint.com/:u:/g/personal/203599_iberopuebla_mx/EZ1rLMzmvQpFmjqNYbOqnRgBzRmKy9k86GRMSvnz9RX0eA?e=BKbNcp" class="btn-link" target="_blank">Ver Archivo</a>
                </div>

                <div class="project-card">
                    <h3>🪴 Macetas</h3>
                    <span class="badge">Diseño</span>
                    <div class="grid-images">
                        <img src="recursos/imgs/CapturaSldMaceta1.png" alt="Maceta 1">
                        <img src="recursos/imgs/CapturaSldMaceta2.png" alt="Maceta 2">
                        <img src="recursos/imgs/CapturaSldMaceta3.png" alt="Maceta 3">
                    </div>
                    <a href="https://iberopuebla-my.sharepoint.com/:u:/g/personal/203599_iberopuebla_mx/ERqRGA3o2o9IsSqqOnfIw7gBV0Ob4TD_jhZCrPU3JgEKGA?e=MjuNGp" class="btn-link" target="_blank">Maceta 1</a>
                    <a href="https://iberopuebla-my.sharepoint.com/:u:/g/personal/203599_iberopuebla_mx/ESXg-GAfJgxEuvUuhufZMe4BfDe-Wp3OSsLXohviJ1W6AQ?e=CKRxE3" class="btn-link" target="_blank">Maceta 2</a>
                    <a href="https://iberopuebla-my.sharepoint.com/:u:/g/personal/203599_iberopuebla_mx/ES-6ij2070FLnzlO6EpYd8kBfsAaLL8qrRlJpNHIkPerxA?e=QBEB7B" class="btn-link" target="_blank">Maceta 3</a>
                </div>
            </div>

            <!-- IDIT Tab -->
            <div id="idit" class="tab-content">
                <div class="project-card">
                    <h3>🏭 Visita al IDIT</h3>
                    <span class="badge">Experiencia</span>
                    <p>Recorrido por las instalaciones del Instituto de Innovación y Desarrollo Tecnológico</p>
                    <div class="grid-images">
                        <img src="recursos/imgs/FotoIDIT1.jpeg" alt="IDIT 1">
                        <img src="recursos/imgs/FotoIDIT2.jpeg" alt="IDIT 2">
                        <img src="recursos/imgs/FotoIDIT3.jpeg" alt="IDIT 3">
                    </div>
                </div>

                <div class="project-card">
                    <h3>📱 Portacelulares</h3>
                    <span class="badge">Proyecto</span>
                    <img src="recursos/imgs/Portacelular.jpeg" alt="Portacelular" class="project-image">
                </div>
            </div>

            <!-- Laser Tab -->
            <div id="laser" class="tab-content">
                <div class="project-card">
                    <h3>🔥 Introducción al Corte Láser</h3>
                    <span class="badge">Capacitación</span>
                    <div class="grid-images">
                        <img src="recursos/imgs/Fotointroduccioncortelaser1.jpg" alt="Intro Láser 1">
                        <img src="recursos/imgs/Fotointroduccioncortelaser2.jpg" alt="Intro Láser 2">
                        <img src="recursos/imgs/Fotointroduccioncortelaser3.jpg" alt="Intro Láser 3">
                    </div>
                </div>

                <div class="project-card">
                    <h3>🦅 Ensamble de Corte Láser - Pájaro</h3>
                    <span class="badge">Fabricación</span>
                    <div class="grid-images">
                        <img src="recursos/imgs/Fotocortepajaro1.jpg" alt="Pájaro 1">
                        <img src="recursos/imgs/Fotocortepajaro2.jpg" alt="Pájaro 2">
                    </div>
                    <a href="recursos/archivos/PajaroEnsambleSolid.SLDPRT" class="btn-link" download>Descargar SLDPRT</a>
                    <a href="recursos/archivos/PajaroEnsambleSolid.DXF" class="btn-link" download>Descargar DXF</a>
                </div>

                <div class="project-card">
                    <h3>🎨 Grabado de Logo con Láser</h3>
                    <span class="badge">Grabado</span>
                    <img src="recursos/imgs/Fotologoplayboy.jpg" alt="Logo" class="project-image">
                    <a href="recursos/archivos/logodeplayboy.DXF" class="btn-link" download>Descargar DXF</a>
                </div>
            </div>

            <!-- Impresión 3D Tab -->
            <div id="impresion3d" class="tab-content">
                <div class="project-card">
                    <h3>🌐 Impresión 3D - Esfera</h3>
                    <span class="badge">3D Print</span>
                    <img src="recursos/imgs/Fotoesfera.jpg" alt="Esfera" class="project-image">
                    <a href="recursos/archivos/Solidpiezabna3d.SLDPRT" class="btn-link" download>Descargar Pieza 3D</a>
                </div>

                <div class="project-card">
                    <h3>🤖 Impresión 3D con IA - Perro Salchicha</h3>
                    <span class="badge">IA</span><span class="badge">3D Print</span>
                    <img src="recursos/imgs/FotoPerroSalchicha.jpg" alt="Perro" class="project-image">
                    <p>Modelo generado con inteligencia artificial e impreso en 3D</p>
                </div>
            </div>

            <!-- Metal Tab -->
            <div id="metal" class="tab-content">
                <div class="project-card">
                    <h3>⚒️ Introducción al Corte de Lámina</h3>
                    <span class="badge">Metales</span>
                    <div class="grid-images">
                        <img src="recursos/imgs/Fotointroduccionametal.jpg" alt="Metal 1">
                        <img src="recursos/imgs/Fotointroduccionametal2.jpg" alt="Metal 2">
                        <img src="recursos/imgs/Fotointroduccionametal3.jpg" alt="Metal 3">
                    </div>
                </div>
            </div>

            <!-- Escaneo Tab -->
            <div id="escaneo" class="tab-content">
                <div class="project-card">
                    <h3>📸 Escaneo 3D de Rostro</h3>
                    <span class="badge">Escaneo 3D</span>
                    <p>Proceso de captura y digitalización de rostro en 3D</p>
                    <div class="grid-images">
                        <img src="recursos/imgs/Fotoescaneocara.jpg" alt="Escaneo 1">
                        <img src="recursos/imgs/Fotoescaneodecara2.jpg" alt="Escaneo 2">
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        function openTab(evt, tabName) {
            const tabContents = document.getElementsByClassName("tab-content");
            for (let i = 0; i < tabContents.length; i++) {
                tabContents[i].classList.remove("active");
            }

            const tabs = document.getElementsByClassName("tab");
            for (let i = 0; i < tabs.length; i++) {
                tabs[i].classList.remove("active");
            }

            document.getElementById(tabName).classList.add("active");
            evt.currentTarget.classList.add("active");
        }
    </script>
</body>
</html>
