```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Agencia Creativa - Flyers, Videos y Agendas</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    },
                    colors: {
                        brand: {
                            50: '#f5f3ff',
                            100: '#ede9fe',
                            500: '#8b5cf6',
                            600: '#7c3aed',
                            900: '#4c1d95',
                        }
                    }
                }
            }
        }
    </script>
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #fafafa;
        }
        
        /* Ocultar scrollbar pero permitir scroll */
        .no-scrollbar::-webkit-scrollbar {
            display: none;
        }
        .no-scrollbar {
            -ms-overflow-style: none;
            scrollbar-width: none;
        }

        /* Notificaciones Toast */
        .toast {
            transition: all 0.3s cubic-bezier(0.68, -0.55, 0.265, 1.55);
            transform: translateY(150%);
            opacity: 0;
        }
        .toast.show {
            transform: translateY(0);
            opacity: 1;
        }

        /* Modales */
        .modal-backdrop {
            opacity: 0;
            pointer-events: none;
            transition: opacity 0.3s ease;
        }
        .modal-backdrop.open {
            opacity: 1;
            pointer-events: auto;
        }
        .modal-content {
            transform: scale(0.95) translateY(20px);
            opacity: 0;
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }
        .modal-backdrop.open .modal-content {
            transform: scale(1) translateY(0);
            opacity: 1;
        }
    </style>
</head>
<body class="text-slate-800 antialiased flex flex-col min-h-screen">

    <!-- Navbar -->
    <nav class="bg-white/80 backdrop-blur-md shadow-sm sticky top-0 z-40">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-center h-16 items-center">
                <div class="flex items-center gap-3">
                    <div class="w-10 h-10 bg-brand-600 rounded-xl flex items-center justify-center text-white shadow-lg shadow-brand-500/30 transform rotate-3">
                        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-6 h-6 -rotate-3">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M9.53 16.122a3 3 0 0 0-5.78 1.128 2.25 2.25 0 0 1-2.4 2.245 4.5 4.5 0 0 0 8.4-2.245c0-.399-.078-.78-.22-1.128Zm0 0a15.998 15.998 0 0 0 3.388-1.62m-5.043-.025a15.994 15.994 0 0 1 1.622-3.395m3.42 3.42a15.995 15.995 0 0 0 4.764-4.648l3.876-5.814a1.151 1.151 0 0 0-1.597-1.597L14.146 6.32a15.996 15.996 0 0 0-4.649 4.763m3.42 3.42a6.776 6.776 0 0 0-3.42-3.42" />
                        </svg>
                    </div>
                    <span class="font-extrabold text-2xl tracking-tight text-slate-900">Estudio Visual</span>
                </div>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <header class="bg-slate-900 text-white overflow-hidden relative">
        <div class="absolute inset-0 z-0">
            <!-- Patrón de fondo sutil -->
            <div class="absolute inset-0 bg-[url('data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjAiIGhlaWdodD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PGNpcmNsZSBjeD0iMiIgY3k9IjIiIHI9IjIiIGZpbGw9IiNmZmZmZmYiIGZpbGwtb3BhY2l0eT0iMC4wNSIvPjwvc3ZnPg==')] opacity-50"></div>
            <div class="absolute top-0 left-1/4 w-96 h-96 bg-brand-600 rounded-full mix-blend-multiply filter blur-[100px] opacity-40"></div>
            <div class="absolute bottom-0 right-1/4 w-96 h-96 bg-blue-600 rounded-full mix-blend-multiply filter blur-[100px] opacity-40"></div>
        </div>
        
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-20 lg:py-28 relative z-10 text-center">
            <h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold tracking-tight mb-6">
                Diseño profesional para tus <span class="text-brand-400">Eventos y Artistas</span>
            </h1>
            <p class="text-lg sm:text-xl text-slate-300 mb-10 max-w-2xl mx-auto">
                Especialistas en flyers de alto impacto, videos publicitarios y agendas musicales. Completa la información y recibe tu diseño directamente por WhatsApp.
            </p>
        </div>
    </header>

    <!-- Main Content (Servicios) -->
    <main class="flex-grow max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-16 w-full -mt-10 relative z-20">
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
            
            <!-- Servicio 1: Flyers -->
            <div class="bg-white rounded-2xl p-8 shadow-xl shadow-slate-200/50 border border-slate-100 flex flex-col items-center text-center hover:-translate-y-2 transition-transform duration-300">
                <div class="w-20 h-20 bg-blue-50 text-blue-600 rounded-full flex items-center justify-center mb-6">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-10 h-10">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 15.75l5.159-5.159a2.25 2.25 0 013.182 0l5.159 5.159m-1.5-1.5 1.409-1.409a2.25 2.25 0 013.182 0l2.909 2.909m-18 3.75h16.5a1.5 1.5 0 001.5-1.5V6a1.5 1.5 0 00-1.5-1.5H3.75A1.5 1.5 0 002.25 6v12a1.5 1.5 0 001.5 1.5zm10.5-11.25h.008v.008h-.008V8.25zm.375 0a.375.375 0 11-.75 0 .375.375 0 01.75 0z" />
                    </svg>
                </div>
                <h2 class="text-2xl font-bold text-slate-900 mb-3">Diseño de Flyers</h2>
                <p class="text-slate-500 mb-8 flex-grow">Para fiestas, conciertos, boliches y eventos corporativos. Alto impacto visual adaptado a redes sociales.</p>
                <button onclick="openModal('modal-flyer')" class="w-full py-3 px-6 bg-slate-900 hover:bg-brand-600 text-white font-semibold rounded-xl transition-colors shadow-md">
                    Solicitar Flyer
                </button>
            </div>

            <!-- Servicio 2: Videos -->
            <div class="bg-white rounded-2xl p-8 shadow-xl shadow-slate-200/50 border border-slate-100 flex flex-col items-center text-center hover:-translate-y-2 transition-transform duration-300 relative overflow-hidden">
                <div class="absolute top-0 inset-x-0 h-1 bg-gradient-to-r from-brand-400 to-brand-600"></div>
                <div class="w-20 h-20 bg-brand-50 text-brand-600 rounded-full flex items-center justify-center mb-6">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-10 h-10">
                        <path stroke-linecap="round" d="M15.75 10.5l4.72-4.72a.75.75 0 011.28.53v11.38a.75.75 0 01-1.28.53l-4.72-4.72M4.5 18.75h9a2.25 2.25 0 002.25-2.25v-9a2.25 2.25 0 00-2.25-2.25h-9A2.25 2.25 0 002.25 7.5v9a2.25 2.25 0 002.25 2.25z" />
                    </svg>
                </div>
                <h2 class="text-2xl font-bold text-slate-900 mb-3">Videos Publicitarios</h2>
                <p class="text-slate-500 mb-8 flex-grow">Flyers animados y spots para reels/historias. Ideal para captar la atención con música y movimiento.</p>
                <button onclick="openModal('modal-video')" class="w-full py-3 px-6 bg-brand-600 hover:bg-brand-700 text-white font-semibold rounded-xl transition-colors shadow-md shadow-brand-500/30">
                    Solicitar Video
                </button>
            </div>

            <!-- Servicio 3: Agenda -->
            <div class="bg-white rounded-2xl p-8 shadow-xl shadow-slate-200/50 border border-slate-100 flex flex-col items-center text-center hover:-translate-y-2 transition-transform duration-300">
                <div class="w-20 h-20 bg-emerald-50 text-emerald-600 rounded-full flex items-center justify-center mb-6">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-10 h-10">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M6.75 3v2.25M17.25 3v2.25M3 18.75V7.5a2.25 2.25 0 012.25-2.25h13.5A2.25 2.25 0 0121 7.5v11.25m-18 0A2.25 2.25 0 005.25 21h13.5A2.25 2.25 0 0021 18.75m-18 0v-7.5A2.25 2.25 0 015.25 9h13.5A2.25 2.25 0 0121 11.25v7.5m-9-6h.008v.008H12v-.008zM12 15h.008v.008H12V15zm0 2.25h.008v.008H12v-.008zM9.75 15h.008v.008H9.75V15zm0 2.25h.008v.008H9.75v-.008zM7.5 15h.008v.008H7.5V15zm0 2.25h.008v.008H7.5v-.008zm6.75-4.5h.008v.008h-.008v-.008zm0 2.25h.008v.008h-.008V15zm0 2.25h.008v.008h-.008v-.008zm2.25-4.5h.008v.008H16.5v-.008zm0 2.25h.008v.008H16.5V15z" />
                    </svg>
                </div>
                <h2 class="text-2xl font-bold text-slate-900 mb-3">Agenda de Artistas</h2>
                <p class="text-slate-500 mb-8 flex-grow">Diseños mensuales o semanales con tus fechas de presentación, lugares y horarios de manera profesional.</p>
                <button onclick="openModal('modal-agenda')" class="w-full py-3 px-6 bg-slate-900 hover:bg-brand-600 text-white font-semibold rounded-xl transition-colors shadow-md">
                    Solicitar Agenda
                </button>
            </div>

        </div>
    </main>

    <!-- MODAL: FLYERS -->
    <div id="modal-flyer" class="modal-backdrop fixed inset-0 z-50 flex items-center justify-center bg-slate-900/60 backdrop-blur-sm p-4 overflow-y-auto">
        <div class="modal-content bg-white w-full max-w-2xl rounded-2xl shadow-2xl relative my-auto">
            <!-- Header -->
            <div class="px-6 py-4 border-b border-slate-100 flex justify-between items-center bg-slate-50 rounded-t-2xl">
                <h3 class="text-xl font-bold text-slate-900 flex items-center gap-2">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-6 h-6 text-blue-600"><path stroke-linecap="round" stroke-linejoin="round" d="M2.25 15.75l5.159-5.159a2.25 2.25 0 013.182 0l5.159 5.159m-1.5-1.5 1.409-1.409a2.25 2.25 0 013.182 0l2.909 2.909" /></svg>
                    Detalles para el Flyer
                </h3>
                <button onclick="closeModal('modal-flyer')" class="text-slate-400 hover:text-slate-700 bg-white rounded-full p-1 shadow-sm border border-slate-200">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-5 h-5"><path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" /></svg>
                </button>
            </div>
            
            <!-- Body Form -->
            <form id="form-flyer" class="p-6 space-y-4 max-h-[70vh] overflow-y-auto no-scrollbar" onsubmit="event.preventDefault(); submitForm('flyer');">
                <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                    <div>
                        <label class="block text-sm font-medium text-slate-700 mb-1">Tu Nombre / Contacto *</label>
                        <input type="text" id="f-nombre" required class="w-full px-4 py-2 bg-slate-50 border border-slate-200 rounded-xl focus:ring-2 focus:ring-brand-500 outline-none">
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-slate-700 mb-1">Nombre del Evento / Título *</label>
                        <input type="text" id="f-evento" required class="w-full px-4 py-2 bg-slate-50 border border-slate-200 rounded-xl focus:ring-2 focus:ring-brand-500 outline-none" placeholder="Ej: Gran Fiesta Retro">
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-slate-700 mb-1">Fecha y Hora *</label>
                        <input type="text" id="f-fecha" required class="w-full px-4 py-2 bg-slate-50 border border-slate-200 rounded-xl focus:ring-2 focus:ring-brand-500 outline-none" placeholder="Ej: Sáb 15 Oct, 23:30hs">
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-slate-700 mb-1">Lugar / Boliche *</label>
                        <input type="text" id="f-lugar" required class="w-full px-4 py-2 bg-slate-50 border border-slate-200 rounded-xl focus:ring-2 focus:ring-brand-500 outline-none">
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-slate-700 mb-1">Organiza / Produce</label>
                        <input type="text" id="f-organiza" class="w-full px-4 py-2 bg-slate-50 border border-slate-200 rounded-xl focus:ring-2 focus:ring-brand-500 outline-none" placeholder="Opcional">
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-slate-700 mb-1">Valor de la Entrada</label>
                        <input type="text" id="f-entrada" class="w-full px-4 py-2 bg-slate-50 border border-slate-200 rounded-xl focus:ring-2 focus:ring-brand-500 outline-none" placeholder="Ej: Generales $5000">
                    </div>
                </div>
                
                <div>
                    <label class="block text-sm font-medium text-slate-700 mb-1">Grupos Musicales / DJs (Lineup) *</label>
                    <textarea id="f-grupos" required rows="2" class="w-full px-4 py-2 bg-slate-50 border border-slate-200 rounded-xl focus:ring-2 focus:ring-brand-500 outline-none resize-none" placeholder="Detalla quiénes se presentan..."></textarea>
                </div>
                
                <div>
                    <label class="block text-sm font-medium text-slate-700 mb-1">Ideas de Diseño / Estilo (Opcional)</label>
                    <textarea id="f-detalles" rows="2" class="w-full px-4 py-2 bg-slate-50 border border-slate-200 rounded-xl focus:ring-2 focus:ring-brand-500 outline-none resize-none" placeholder="Colores deseados, temática, si hay que incluir fotos, etc."></textarea>
                </div>

                <!-- Footer del form -->
                <div class="pt-4 border-t border-slate-100 mt-6">
                    <button type="submit" class="w-full bg-[#25D366] hover:bg-[#1ebd5a] text-white font-bold py-3.5 px-4 rounded-xl flex items-center justify-center gap-2 transition-transform transform hover:scale-[1.02] shadow-lg shadow-green-500/20">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51a12.8 12.8 0 0 0-.57-.01c-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 0 1-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 0 1-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 0 1 2.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0 0 12.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 0 0 5.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 0 0-3.48-8.413Z"/></svg>
                        Enviar Detalles por WhatsApp
                    </button>
                </div>
            </form>
        </div>
    </div>

    <!-- MODAL: VIDEOS PUBLICITARIOS -->
    <div id="modal-video" class="modal-backdrop fixed inset-0 z-50 flex items-center justify-center bg-slate-900/60 backdrop-blur-sm p-4 overflow-y-auto">
        <div class="modal-content bg-white w-full max-w-2xl rounded-2xl shadow-2xl relative my-auto">
            <div class="px-6 py-4 border-b border-slate-100 flex justify-between items-center bg-slate-50 rounded-t-2xl">
                <h3 class="text-xl font-bold text-slate-900 flex items-center gap-2">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-6 h-6 text-brand-600"><path stroke-linecap="round" d="M15.75 10.5l4.72-4.72a.75.75 0 011.28.53v11.38a.75.75 0 01-1.28.53l-4.72-4.72" /></svg>
                    Detalles para Video
                </h3>
                <button onclick="closeModal('modal-video')" class="text-slate-400 hover:text-slate-700 bg-white rounded-full p-1 shadow-sm border border-slate-200">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-5 h-5"><path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" /></svg>
                </button>
            </div>
            
            <form id="form-video" class="p-6 space-y-4 max-h-[70vh] overflow-y-auto no-scrollbar" onsubmit="event.preventDefault(); submitForm('video');">
                <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                    <div>
                        <label class="block text-sm font-medium text-slate-700 mb-1">Tu Nombre / Contacto *</label>
                        <input type="text" id="v-nombre" required class="w-full px-4 py-2 bg-slate-50 border border-slate-200 rounded-xl focus:ring-2 focus:ring-brand-500 outline-none">
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-slate-700 mb-1">Nombre del Evento/Campaña *</label>
                        <input type="text" id="v-evento" required class="w-full px-4 py-2 bg-slate-50 border border-slate-200 rounded-xl focus:ring-2 focus:ring-brand-500 outline-none">
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-slate-700 mb-1">Formato deseado *</label>
                        <select id="v-formato" class="w-full px-4 py-2 bg-slate-50 border border-slate-200 rounded-xl focus:ring-2 focus:ring-brand-500 outline-none">
                            <option value="Reel / Historia (Vertical 9:16)">Reel / Historia (Vertical 9:16)</option>
                            <option value="Post (Cuadrado 1:1)">Post (Cuadrado 1:1)</option>
                            <option value="Youtube / Pantalla (Horizontal 16:9)">Youtube / Pantalla (Horizontal 16:9)</option>
                        </select>
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-slate-700 mb-1">¿Requiere locución de voz?</label>
                        <select id="v-locucion" class="w-full px-4 py-2 bg-slate-50 border border-slate-200 rounded-xl focus:ring-2 focus:ring-brand-500 outline-none">
                            <option value="No">No, solo música de fondo</option>
                            <option value="Sí, enviar presupuesto">Sí, incluir presupuesto</option>
                        </select>
                    </div>
                </div>
                
                <div>
                    <label class="block text-sm font-medium text-slate-700 mb-1">Información principal a mostrar * (Lugar, fecha, artistas, precio)</label>
                    <textarea id="v-info" required rows="3" class="w-full px-4 py-2 bg-slate-50 border border-slate-200 rounded-xl focus:ring-2 focus:ring-brand-500 outline-none resize-none" placeholder="Toda la info clave que debe aparecer escrita en el video..."></textarea>
                </div>

                <div>
                    <label class="block text-sm font-medium text-slate-700 mb-1">Música de fondo sugerida (Opcional)</label>
                    <input type="text" id="v-musica" class="w-full px-4 py-2 bg-slate-50 border border-slate-200 rounded-xl focus:ring-2 focus:ring-brand-500 outline-none" placeholder="Ej: Canción X de Artista Y, o estilo 'Electrónica enérgica'">
                </div>

                <div class="pt-4 border-t border-slate-100 mt-6">
                    <button type="submit" class="w-full bg-[#25D366] hover:bg-[#1ebd5a] text-white font-bold py-3.5 px-4 rounded-xl flex items-center justify-center gap-2 transition-transform transform hover:scale-[1.02] shadow-lg shadow-green-500/20">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51a12.8 12.8 0 0 0-.57-.01c-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 0 1-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 0 1-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 0 1 2.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0 0 12.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 0 0 5.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 0 0-3.48-8.413Z"/></svg>
                        Enviar Detalles por WhatsApp
                    </button>
                </div>
            </form>
        </div>
    </div>

    <!-- MODAL: AGENDA DE ARTISTAS -->
    <div id="modal-agenda" class="modal-backdrop fixed inset-0 z-50 flex items-center justify-center bg-slate-900/60 backdrop-blur-sm p-4 overflow-y-auto">
        <div class="modal-content bg-white w-full max-w-2xl rounded-2xl shadow-2xl relative my-auto">
            <div class="px-6 py-4 border-b border-slate-100 flex justify-between items-center bg-slate-50 rounded-t-2xl">
                <h3 class="text-xl font-bold text-slate-900 flex items-center gap-2">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-6 h-6 text-emerald-600"><path stroke-linecap="round" stroke-linejoin="round" d="M6.75 3v2.25M17.25 3v2.25M3 18.75V7.5a2.25 2.25 0 012.25-2.25h13.5A2.25 2.25 0 0121 7.5v11.25m-18 0A2.25 2.25 0 005.25 21h13.5A2.25 2.25 0 0021 18.75m-18 0v-7.5A2.25 2.25 0 015.25 9h13.5A2.25 2.25 0 0121 11.25v7.5" /></svg>
                    Detalles para Agenda
                </h3>
                <button onclick="closeModal('modal-agenda')" class="text-slate-400 hover:text-slate-700 bg-white rounded-full p-1 shadow-sm border border-slate-200">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-5 h-5"><path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" /></svg>
                </button>
            </div>
            
            <form id="form-agenda" class="p-6 space-y-4 max-h-[70vh] overflow-y-auto no-scrollbar" onsubmit="event.preventDefault(); submitForm('agenda');">
                <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                    <div>
                        <label class="block text-sm font-medium text-slate-700 mb-1">Nombre del Artista / Banda *</label>
                        <input type="text" id="a-artista" required class="w-full px-4 py-2 bg-slate-50 border border-slate-200 rounded-xl focus:ring-2 focus:ring-brand-500 outline-none">
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-slate-700 mb-1">Periodo de la Agenda *</label>
                        <input type="text" id="a-periodo" required class="w-full px-4 py-2 bg-slate-50 border border-slate-200 rounded-xl focus:ring-2 focus:ring-brand-500 outline-none" placeholder="Ej: Octubre 2026, o Fin de semana largo">
                    </div>
                </div>
                
                <div class="bg-blue-50 border border-blue-100 p-4 rounded-xl">
                    <label class="block text-sm font-bold text-blue-900 mb-2">Fechas y Lugares *</label>
                    <p class="text-xs text-blue-700 mb-2">Formato sugerido: "Día - Lugar - Ciudad"</p>
                    <textarea id="a-fechas" required rows="4" class="w-full px-4 py-2 bg-white border border-blue-200 rounded-xl focus:ring-2 focus:ring-blue-500 outline-none resize-none" placeholder="Ej:&#10;Viernes 14 - Club del Arte - CABA&#10;Sábado 15 - Festival X - Rosario&#10;Domingo 16 - Bar Cultural - Córdoba"></textarea>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                    <div>
                        <label class="block text-sm font-medium text-slate-700 mb-1">Redes Sociales a incluir</label>
                        <input type="text" id="a-redes" class="w-full px-4 py-2 bg-slate-50 border border-slate-200 rounded-xl focus:ring-2 focus:ring-brand-500 outline-none" placeholder="Ej: @mi.banda">
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-slate-700 mb-1">Teléfono de Booking/Contrataciones</label>
                        <input type="text" id="a-booking" class="w-full px-4 py-2 bg-slate-50 border border-slate-200 rounded-xl focus:ring-2 focus:ring-brand-500 outline-none" placeholder="Opcional">
                    </div>
                </div>

                <div class="pt-4 border-t border-slate-100 mt-6">
                    <button type="submit" class="w-full bg-[#25D366] hover:bg-[#1ebd5a] text-white font-bold py-3.5 px-4 rounded-xl flex items-center justify-center gap-2 transition-transform transform hover:scale-[1.02] shadow-lg shadow-green-500/20">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51a12.8 12.8 0 0 0-.57-.01c-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 0 1-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 0 1-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 0 1 2.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0 0 12.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 0 0 5.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 0 0-3.48-8.413Z"/></svg>
                        Enviar Detalles por WhatsApp
                    </button>
                </div>
            </form>
        </div>
    </div>

    <!-- Custom Notification Toast Container -->
    <div id="toast-container" class="fixed bottom-6 left-1/2 transform -translate-x-1/2 z-[100] flex flex-col gap-2 pointer-events-none w-full max-w-sm px-4"></div>

    <!-- Footer -->
    <footer class="bg-white border-t border-slate-200 mt-auto">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-8 text-center">
            <p class="text-slate-500 text-sm">© 2026 Estudio Visual. Servicios de diseño profesional.</p>
        </div>
    </footer>

    <script>
        // --- CONFIGURACIÓN IMPORTANTE ---
        // Reemplaza con tu número. Código de país + número (Sin el '+'). Ej: 549112345678
        const NUMERO_WHATSAPP = "5491100000000"; 

        // Funciones para Modales
        function openModal(id) {
            document.getElementById(id).classList.add('open');
            document.body.style.overflow = 'hidden'; // Evita scroll de fondo
        }

        function closeModal(id) {
            document.getElementById(id).classList.remove('open');
            document.body.style.overflow = 'auto';
        }

        // Cerrar modal al hacer clic fuera del contenido
        document.querySelectorAll('.modal-backdrop').forEach(modal => {
            modal.addEventListener('click', function(e) {
                if (e.target === this) {
                    closeModal(this.id);
                }
            });
        });

        // Notificaciones
        function mostrarNotificacion(mensaje) {
            const container = document.getElementById('toast-container');
            const toast = document.createElement('div');
            
            toast.className = `toast px-4 py-3 rounded-xl shadow-xl text-white text-sm font-medium flex items-center gap-3 bg-slate-900 mx-auto w-full`;
            toast.innerHTML = `
                <div class="bg-green-500/20 p-1 rounded-full">
                    <svg class="w-5 h-5 text-green-400" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"/></svg>
                </div>
                <span>${mensaje}</span>
            `;
            container.appendChild(toast);
            
            setTimeout(() => toast.classList.add('show'), 10);
            setTimeout(() => {
                toast.classList.remove('show');
                setTimeout(() => toast.remove(), 300);
            }, 4000);
        }

        // Lógica de Envío por Formulario
        function submitForm(tipo) {
            let mensaje = "";

            if (tipo === 'flyer') {
                const nombre = document.getElementById('f-nombre').value;
                const evento = document.getElementById('f-evento').value;
                const fecha = document.getElementById('f-fecha').value;
                const lugar = document.getElementById('f-lugar').value;
                const organiza = document.getElementById('f-organiza').value;
                const entrada = document.getElementById('f-entrada').value;
                const grupos = document.getElementById('f-grupos').value;
                const detalles = document.getElementById('f-detalles').value;

                mensaje = `*🎨 NUEVA SOLICITUD: DISEÑO DE FLYER*\n\n`;
                mensaje += `*👤 Cliente:* ${nombre}\n`;
                mensaje += `*📌 Evento:* ${evento}\n`;
                mensaje += `*📅 Fecha/Hora:* ${fecha}\n`;
                mensaje += `*📍 Lugar:* ${lugar}\n`;
                if(organiza) mensaje += `*🏢 Organiza:* ${organiza}\n`;
                if(entrada) mensaje += `*🎟️ Entrada:* ${entrada}\n`;
                mensaje += `\n*🎸 Lineup / Artistas:*\n_${grupos}_\n`;
                if(detalles) mensaje += `\n*💡 Detalles extra de diseño:*\n_${detalles}_\n`;

                closeModal('modal-flyer');
                document.getElementById('form-flyer').reset();

            } else if (tipo === 'video') {
                const nombre = document.getElementById('v-nombre').value;
                const evento = document.getElementById('v-evento').value;
                const formato = document.getElementById('v-formato').value;
                const locucion = document.getElementById('v-locucion').value;
                const info = document.getElementById('v-info').value;
                const musica = document.getElementById('v-musica').value;

                mensaje = `*🎬 NUEVA SOLICITUD: VIDEO PUBLICITARIO*\n\n`;
                mensaje += `*👤 Cliente:* ${nombre}\n`;
                mensaje += `*📌 Evento/Campaña:* ${evento}\n`;
                mensaje += `*📱 Formato:* ${formato}\n`;
                mensaje += `*🎙️ Locución:* ${locucion}\n`;
                mensaje += `\n*📝 Información a mostrar en el video:*\n_${info}_\n`;
                if(musica) mensaje += `\n*🎵 Música sugerida:* ${musica}\n`;

                closeModal('modal-video');
                document.getElementById('form-video').reset();

            } else if (tipo === 'agenda') {
                const artista = document.getElementById('a-artista').value;
                const periodo = document.getElementById('a-periodo').value;
                const fechas = document.getElementById('a-fechas').value;
                const redes = document.getElementById('a-redes').value;
                const booking = document.getElementById('a-booking').value;

                mensaje = `*🗓️ NUEVA SOLICITUD: AGENDA DE ARTISTA*\n\n`;
                mensaje += `*🎸 Artista/Banda:* ${artista}\n`;
                mensaje += `*📅 Periodo:* ${periodo}\n`;
                mensaje += `\n*📍 Fechas y Lugares:*\n${fechas}\n`;
                if(redes) mensaje += `\n*📱 Redes a incluir:* ${redes}\n`;
                if(booking) mensaje += `*📞 Booking:* ${booking}\n`;

                closeModal('modal-agenda');
                document.getElementById('form-agenda').reset();
            }

            mensaje += `\n_Hola, te envío los datos para consultar presupuesto y disponibilidad._`;

            // Enviar a WhatsApp
            const urlWhatsApp = `https://wa.me/${NUMERO_WHATSAPP}?text=${encodeURIComponent(mensaje)}`;
            window.open(urlWhatsApp, '_blank');
            
            mostrarNotificacion('¡Redirigiendo a WhatsApp con tus datos!');
        }
    </script>
</body>
</html>
```
