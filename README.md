<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tutigrito - Conectando Expertos con Clientes</title>
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Google Fonts: Inter -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">

    <style>
        /* Estilos personalizados para la fuente y mejoras visuales */
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f3f4f6; /* gris claro de fondo */
        }
        .brand-orange {
            color: #F97316;
        }
        .bg-brand-orange {
            background-color: #F97316;
        }
        .hover-bg-brand-orange:hover {
            background-color: #EA580C;
        }
        .border-brand-orange {
            border-color: #F97316;
        }
        /* Animación sutil para las tarjetas */
        .service-card {
            transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
        }
        .service-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
        }
    </style>
</head>
<body class="text-gray-800">

    <!-- Header -->
    <header class="bg-gray-800 shadow-lg">
        <div class="container mx-auto px-6 py-4 flex justify-between items-center">
            <div class="flex items-center space-x-3">
                <!-- Logo SVG de Tigre -->
                <svg class="h-10 w-10 text-orange-500" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M15.362 5.214A8.252 8.252 0 0112 21 8.25 8.25 0 016.038 7.048 8.287 8.287 0 009 9.6a8.983 8.983 0 013.362-3.797A8.222 8.222 0 0012 6a8.222 8.222 0 00-3.362-1.203 8.252 8.252 0 016.724.417zM12 21a8.25 8.25 0 005.962-13.952 8.287 8.287 0 01-2.6 2.55A8.983 8.983 0 0012 14.4a8.983 8.983 0 00-3.362-3.797 8.287 8.287 0 01-2.6-2.55A8.25 8.25 0 0012 21z" />
                </svg>
                <h1 class="text-2xl font-bold text-white">Tutigrito</h1>
            </div>
            <a href="#registro-form" class="hidden md:inline-block bg-brand-orange text-white font-semibold px-4 py-2 rounded-lg hover-bg-brand-orange transition-colors">
                Ofrecer un Servicio
            </a>
        </div>
    </header>

    <!-- Main Content -->
    <main class="container mx-auto p-4 md:p-8">

        <!-- Sección de Bienvenida -->
        <section class="text-center mb-12">
            <h2 class="text-3xl md:text-4xl font-bold mb-2">Encuentra al experto que necesitas</h2>
            <p class="text-gray-600 max-w-2xl mx-auto">Conectamos a profesionales de confianza con personas que necesitan soluciones. Rápido, fácil y seguro.</p>
        </section>

        <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
            
            <!-- Columna de Registro -->
            <div class="lg:col-span-1" id="registro-form">
                <div class="bg-white p-6 rounded-xl shadow-md border border-gray-200">
                    <h3 class="text-2xl font-bold mb-4 flex items-center">
                        <svg class="h-6 w-6 mr-2 brand-orange" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor">
                           <path stroke-linecap="round" stroke-linejoin="round" d="M12 4.5v15m7.5-7.5h-15" />
                        </svg>
                        Ofrece tus Servicios
                    </h3>
                    <p class="text-gray-600 mb-6">Completa el formulario para aparecer en nuestro directorio.</p>
                    <form id="serviceForm" class="space-y-4">
                        <div>
                            <label for="nombre" class="block text-sm font-medium text-gray-700">Nombre Completo</label>
                            <input type="text" id="nombre" name="nombre" required class="mt-1 block w-full px-3 py-2 bg-white border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-orange-500 focus:border-orange-500">
                        </div>
                        <div>
                            <label for="servicio" class="block text-sm font-medium text-gray-700">Tipo de Servicio</label>
                            <select id="servicio" name="servicio" required class="mt-1 block w-full px-3 py-2 bg-white border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-orange-500 focus:border-orange-500">
                                <option value="" disabled selected>Selecciona una categoría</option>
                                <option value="Albañilería">Albañilería</option>
                                <option value="Plomería">Plomería</option>
                                <option value="Electricidad">Electricidad</option>
                                <option value="Limpieza">Limpieza</option>
                                <option value="Costura">Costura</option>
                                <option value="Jardinería">Jardinería</option>
                                <option value="Carpintería">Carpintería</option>
                                <option value="Pintura">Pintura</option>
                                <option value="Refrigeración">Refrigeración</option>
                            </select>
                        </div>
                        <div>
                            <label for="telefono" class="block text-sm font-medium text-gray-700">Número de Contacto (WhatsApp)</label>
                            <input type="tel" id="telefono" name="telefono" required placeholder="Ej: 04121234567" class="mt-1 block w-full px-3 py-2 bg-white border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-orange-500 focus:border-orange-500">
                        </div>
                        <div>
                            <label for="descripcion" class="block text-sm font-medium text-gray-700">Describe tu trabajo (opcional)</label>
                            <textarea id="descripcion" name="descripcion" rows="3" placeholder="Ej: Especialista en remodelaciones y acabados." class="mt-1 block w-full px-3 py-2 bg-white border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-orange-500 focus:border-orange-500"></textarea>
                        </div>
                        <button type="submit" class="w-full bg-brand-orange text-white font-bold py-3 px-4 rounded-lg hover-bg-brand-orange transition-colors duration-300 shadow-md">
                            Registrar mi Servicio
                        </button>
                    </form>
                    <div id="successMessage" class="hidden mt-4 p-3 bg-green-100 border border-green-400 text-green-700 rounded-md">
                        ¡Servicio registrado con éxito!
                    </div>
                </div>
            </div>

            <!-- Columna de Directorio -->
            <div class="lg:col-span-2">
                <div class="bg-white p-6 rounded-xl shadow-md border border-gray-200">
                    <h3 class="text-2xl font-bold mb-4">Directorio de Servicios</h3>
                    <!-- Filtro -->
                    <div class="mb-6">
                        <label for="filterService" class="block text-sm font-medium text-gray-700">Filtrar por servicio:</label>
                        <select id="filterService" class="mt-1 block w-full md:w-1/2 px-3 py-2 bg-white border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-orange-500 focus:border-orange-500">
                            <option value="todos">Todos los servicios</option>
                        </select>
                    </div>

                    <!-- Contenedor de las tarjetas -->
                    <div id="serviceDirectory" class="grid grid-cols-1 md:grid-cols-2 gap-6">
                        <!-- Las tarjetas de servicio se insertarán aquí -->
                    </div>
                     <div id="noResults" class="hidden text-center py-10">
                        <p class="text-gray-500">No se encontraron servicios para esta categoría.</p>
                    </div>
                </div>
            </div>
        </div>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-800 mt-12">
        <div class="container mx-auto px-6 py-4 text-center text-gray-400">
            <p>&copy; 2024 Tutigrito. Todos los derechos reservados.</p>
            <p class="text-sm">Conectando a la comunidad.</p>
        </div>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            // --- ELEMENTOS DEL DOM ---
            const serviceForm = document.getElementById('serviceForm');
            const serviceDirectory = document.getElementById('serviceDirectory');
            const filterService = document.getElementById('filterService');
            const successMessage = document.getElementById('successMessage');
            const noResults = document.getElementById('noResults');

            // --- DATOS (Simulación de base de datos) ---
            let services = [
                {
                    id: 1,
                    nombre: 'Carlos Rodríguez',
                    servicio: 'Plomería',
                    telefono: '04141234567',
                    descripcion: 'Instalaciones y reparaciones de tuberías. Atención de emergencias 24/7.'
                },
                {
                    id: 2,
                    nombre: 'Ana Pérez',
                    servicio: 'Limpieza',
                    telefono: '04247654321',
                    descripcion: 'Servicios de limpieza profunda para hogares y oficinas. Personal de confianza.'
                },
                {
                    id: 3,
                    nombre: 'José Altuve',
                    servicio: 'Albañilería',
                    telefono: '04129876543',
                    descripcion: 'Construcción de paredes, frisos y remodelaciones en general. Presupuestos sin compromiso.'
                },
                 {
                    id: 4,
                    nombre: 'Maria Garcia',
                    servicio: 'Costura',
                    telefono: '04162345678',
                    descripcion: 'Arreglos de ropa, confección a medida y diseños personalizados.'
                }
            ];

            // --- FUNCIONES ---

            /**
             * Renderiza las tarjetas de servicio en el directorio.
             * @param {Array} servicesToRender - El array de servicios a mostrar.
             */
            const renderServices = (servicesToRender) => {
                serviceDirectory.innerHTML = ''; // Limpiar el directorio

                if (servicesToRender.length === 0) {
                    noResults.classList.remove('hidden');
                } else {
                    noResults.classList.add('hidden');
                }

                servicesToRender.forEach(service => {
                    const card = document.createElement('div');
                    card.className = 'service-card bg-gray-50 p-5 rounded-lg border border-gray-200 flex flex-col';
                    
                    card.innerHTML = `
                        <h4 class="text-xl font-bold text-gray-900">${service.nombre}</h4>
                        <p class="text-sm font-semibold brand-orange bg-orange-100 px-2 py-1 rounded-full self-start my-2">${service.servicio}</p>
                        <p class="text-gray-600 flex-grow">${service.descripcion || 'No hay descripción disponible.'}</p>
                        <div class="mt-4 pt-4 border-t border-gray-200">
                             <a href="https://wa.me/58${service.telefono.substring(1)}?text=Hola%20${service.nombre.split(' ')[0]},%20te%20contacto%20desde%20Tutigrito%20por%20el%20servicio%20de%20${service.servicio}" target="_blank" class="w-full text-center bg-green-500 text-white font-bold py-2 px-4 rounded-lg hover:bg-green-600 transition-colors flex items-center justify-center space-x-2">
                                <svg class="h-5 w-5" xmlns="http://www.w3.org/2000/svg" fill="currentColor" viewBox="0 0 16 16">
                                    <path d="M13.601 2.326A7.854 7.854 0 0 0 7.994 0C3.627 0 .068 3.558.064 7.926c0 1.399.366 2.76 1.057 3.965L0 16l4.204-1.102a7.933 7.933 0 0 0 3.79.965h.004c4.368 0 7.926-3.558 7.93-7.93A7.898 7.898 0 0 0 13.6 2.326zM7.994 14.521a6.573 6.573 0 0 1-3.356-.92l-.24-.144-2.494.654.666-2.433-.156-.251a6.56 6.56 0 0 1-1.007-3.505c0-3.626 2.957-6.584 6.591-6.584a6.56 6.56 0 0 1 4.66 1.931 6.557 6.557 0 0 1 1.928 4.66c-.004 3.639-2.961 6.592-6.592 6.592zm3.615-4.934c-.197-.099-1.17-.578-1.353-.646-.182-.065-.315-.099-.445.099-.133.197-.513.646-.627.775-.114.133-.232.148-.43.05-.197-.1-.836-.308-1.592-.985-.59-.525-.985-1.175-1.103-1.372-.114-.198-.011-.304.088-.403.087-.088.197-.232.296-.346.1-.114.133-.198.198-.33.065-.134.034-.248-.015-.347-.05-.099-.445-1.076-.612-1.47-.16-.389-.323-.335-.445-.34-.114-.007-.247-.007-.38-.007a.729.729 0 0 0-.529.247c-.182.198-.691.677-.691 1.654 0 .977.71 1.916.81 2.049.098.133 1.394 2.132 3.383 2.992.47.205.84.326 1.129.418.475.152.904.129 1.246.08.38-.058 1.171-.48 1.338-.943.164-.464.164-.86.114-.943-.049-.084-.182-.133-.38-.232z"/>
                                </svg>
                                <span>Contactar por WhatsApp</span>
                            </a>
                        </div>
                    `;
                    serviceDirectory.appendChild(card);
                });
            };

            /**
             * Actualiza las opciones del menú desplegable de filtro.
             */
            const updateFilterOptions = () => {
                const existingOptions = new Set(Array.from(filterService.options).map(o => o.value));
                const serviceTypes = new Set(services.map(s => s.servicio));
                
                serviceTypes.forEach(type => {
                    if (!existingOptions.has(type)) {
                        const option = document.createElement('option');
                        option.value = type;
                        option.textContent = type;
                        filterService.appendChild(option);
                    }
                });
            };

            // --- MANEJADORES DE EVENTOS ---

            // Manejar el envío del formulario de registro
            serviceForm.addEventListener('submit', (e) => {
                e.preventDefault();
                
                const formData = new FormData(serviceForm);
                const newService = {
                    id: Date.now(),
                    nombre: formData.get('nombre'),
                    servicio: formData.get('servicio'),
                    telefono: formData.get('telefono'),
                    descripcion: formData.get('descripcion')
                };

                // Añadir el nuevo servicio al array
                services.push(newService);
                
                // Resetear el filtro para mostrar todo, incluido el nuevo
                filterService.value = 'todos';
                renderServices(services);
                updateFilterOptions();

                // Limpiar el formulario y mostrar mensaje de éxito
                serviceForm.reset();
                successMessage.classList.remove('hidden');
                setTimeout(() => {
                    successMessage.classList.add('hidden');
                }, 3000); // Ocultar el mensaje después de 3 segundos
            });

            // Manejar el cambio en el filtro
            filterService.addEventListener('change', () => {
                const selectedService = filterService.value;
                if (selectedService === 'todos') {
                    renderServices(services);
                } else {
                    const filtered = services.filter(s => s.servicio === selectedService);
                    renderServices(filtered);
                }
            });

            // --- INICIALIZACIÓN ---
            renderServices(services);
            updateFilterOptions();
        });
    </script>

</body>
</html>
