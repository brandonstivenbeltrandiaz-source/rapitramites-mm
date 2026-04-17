# rapitramites-mm
Página web Rapitrámites M&amp;M - Curití
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rapitrámites M&M - Tu vehículo legal y protegido</title>
    <meta name="description" content="Trámites de tránsito, SOAT, revisiones técnicas y más en Curití. ¡Tu vehículo siempre legal!">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            color: #333;
            overflow-x: hidden;
        }

        header {
            background: linear-gradient(135deg, #1a1a1a 0%, #2d2d2d 100%);
            color: #c5a059;
            padding: 2rem 1rem;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 10"><defs><pattern id="grain" width="100" height="10" patternUnits="userSpaceOnUse"><circle cx="25" cy="5" r="1" fill="rgba(197,160,89,0.1)"/><circle cx="75" cy="5" r="0.5" fill="rgba(197,160,89,0.05)"/></pattern></defs><rect width="100" height="10" fill="url(%23grain)"/></svg>');
            opacity: 0.5;
        }

        header h1 {
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
            font-weight: 700;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
            position: relative;
            z-index: 1;
        }

        header p {
            font-size: 1.2rem;
            opacity: 0.9;
            position: relative;
            z-index: 1;
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
            padding: 2rem 1rem;
        }

        .alerta {
            background: linear-gradient(135deg, #ff6b6b 0%, #ee5a52 100%);
            color: white;
            padding: 1.5rem;
            text-align: center;
            border-radius: 15px;
            margin-bottom: 2rem;
            box-shadow: 0 10px 30px rgba(255,107,107,0.3);
            animation: pulse 2s infinite;
            position: relative;
            overflow: hidden;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.02); }
        }

        .alerta::before {
            content: '⚠️';
            font-size: 2rem;
            margin-right: 0.5rem;
            display: inline-block;
            animation: bounce 2s infinite;
        }

        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% { transform: translateY(0); }
            40% { transform: translateY(-10px); }
            60% { transform: translateY(-5px); }
        }

        .alerta strong {
            font-size: 1.3rem;
            display: block;
            margin-bottom: 0.5rem;
        }

        h2 {
            color: #1a1a1a;
            text-align: center;
            margin: 3rem 0 2rem;
            font-size: 2rem;
            position: relative;
        }

        h2::after {
            content: '';
            display: block;
            width: 60px;
            height: 4px;
            background: linear-gradient(90deg, #c5a059, #d4af37);
            margin: 0.5rem auto;
            border-radius: 2px;
        }

        .servicios-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.5rem;
            margin-bottom: 3rem;
        }

        .tarjeta {
            background: rgba(255,255,255,0.95);
            backdrop-filter: blur(10px);
            padding: 2rem;
            border-radius: 20px;
            border: 1px solid rgba(197,160,89,0.2);
            box-shadow: 0 15px 35px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .tarjeta::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, #c5a059, #d4af37, #c5a059);
        }

        .tarjeta:hover {
            transform: translateY(-10px);
            box-shadow: 0 25px 50px rgba(0,0,0,0.15);
        }

        .tarjeta i {
            font-size: 3rem;
            color: #c5a059;
            margin-bottom: 1rem;
            display: block;
        }

        .tarjeta h3 {
            color: #1a1a1a;
            margin-bottom: 1rem;
            font-size: 1.5rem;
        }

        .contacto {
            text-align: center;
        }

        .contacto p {
            font-size: 1.1rem;
            margin: 0.5rem 0;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.5rem;
        }

        .boton-ws {
            display: block;
            background: linear-gradient(135deg, #25D366 0%, #128C7E 100%);
            color: white;
            text-align: center;
            padding: 1.2rem 2rem;
            text-decoration: none;
            font-weight: 700;
            font-size: 1.2rem;
            border-radius: 50px;
            margin: 2rem auto;
            width: 100%;
            max-width: 300px;
            box-shadow: 0 10px 30px rgba(37,211,102,0.4);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .boton-ws:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 40px rgba(37,211,102,0.5);
        }

        .boton-ws::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.3), transparent);
            transition: left 0.5s;
        }

        .boton-ws:hover::before {
            left: 100%;
        }

        .boton-ws i {
            margin-right: 0.5rem;
        }

        footer {
            text-align: center;
            padding: 2rem;
            color: #666;
            background: rgba(26,26,26,0.8);
            margin-top: 3rem;
        }

        @media (max-width: 768px) {
            header h1 {
                font-size: 2rem;
            }
            
            .servicios-grid {
                grid-template-columns: 1fr;
            }
            
            .container {
                padding: 1rem;
            }
        }

        /* Animaciones de entrada */
        .tarjeta {
            opacity: 0;
            transform: translateY(30px);
            animation: fadeInUp 0.6s ease forwards;
        }

        .tarjeta:nth-child(2) { animation-delay: 0.1s; }
        .tarjeta:nth-child(3) { animation-delay: 0.2s; }

        @keyframes fadeInUp {
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
    </style>
</head>
<body>
    <header>
        <h1><i class="fas fa-car"></i> Rapitrámites M&M</h1>
        <p><strong>Tu vehículo legal y protegido</strong> • Curití - Santander</p>
    </header>

    <div class="container">
        <div class="alerta">
            <strong>¡URGENTE!</strong> Paga tu impuesto vehicular antes del <strong>30 de junio</strong> 
            <br><small>¡Evita multas y comparendos!</small>
        </div>

        <h2><i class="fas fa-tools"></i> Nuestros Servicios</h2>
        
        <div class="servicios-grid">
            <div class="tarjeta">
                <i class="fas fa-id-card"></i>
                <h3>Trámites de Tránsito</h3>
                <p><strong>Matrículas</strong> • <strong>Traspasos</strong> • <strong>Traslado de cuenta</strong></p>
                <p>¡Todo rápido y sin complicaciones!</p>
            </div>

            <div class="tarjeta">
                <i class="fas fa-shield-alt"></i>
                <h3>Seguros y Revisiones</h3>
                <p><strong>SOAT</strong> al mejor precio • <strong>Técnico-Mecánica</strong></p>
                <p>Vigencia inmediata para tu tranquilidad</p>
            </div>

            <div class="tarjeta contacto">
                <i class="fas fa-map-marker-alt"></i>
                <h3>Encuéntranos</h3>
                <p><i class="fas fa-location-dot"></i> Cra. 9 #3-69 Altos de San Jorge, Curití</p>
                <p><i class="fas fa-phone"></i> <strong>311 2487901</strong></p>
                <p><i class="fas fa-clock"></i> Lunes a Sábado • 8am - 6pm</p>
            </div>
        </div>

        <a href="https://wa.me/573112487901?text=¡Hola!%20Quiero%20información%20sobre%20mis%20trámites" 
           class="boton-ws" target="_blank">
            <i class="fab fa-whatsapp"></i> ¡Contáctanos por WhatsApp!
        </a>
    </div>

    <footer>
        <p>&copy; 2024 Rapitrámites M&M. Todos los derechos reservados. | Curití - Santander</p>
    </footer>

    <script>
        // Efecto de scroll suave
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Copiar número al hacer clic
        document.querySelectorAll('.contacto p:has(.fa-phone)').forEach(p => {
            p.style.cursor = 'pointer';
            p.addEventListener('click', () => {
                navigator.clipboard.writeText('3112487901');
                p.innerHTML = '<i class="fas fa-phone"></i> <strong>¡Número copiado!</strong>';
                setTimeout(() => {
                    p.innerHTML = '<i class="fas fa-phone"></i> <strong>311 2487901</strong>';
                }, 2000);
            });
        });
    </script>
</body>
</html>
