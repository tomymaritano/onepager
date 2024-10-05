<script>
    const profile = {
        name: 'Tomás Maritano',
        description: 'Creador de productos digitales. Con experiencia en el diseño y desarrollo de soluciones innovadoras que aportan valor en startups y empresas tecnológicas.',
        image: 'https://media.licdn.com/dms/image/v2/D4D03AQH0MyoFc_QYOw/profile-displayphoto-shrink_800_800/profile-displayphoto-shrink_800_800/0/1706897249816?e=1733356800&v=beta&t=E5HQCkLCW2P72_pgL_-AiRQUa58dHWg8JbVfr4wRqaU',
        verified: true
    };

    const links = [
        {
            platform: 'Dripnex.app',
            username: 'Dripnex',
            description: 'Dashboard para seguimiento de onboarding en startups.',
            link: 'https://dripnex.app',
            icon: 'https://via.placeholder.com/50?text=D'
        },
        {
            platform: 'Dolar Gaucho',
            username: 'Dolar Gaucho',
            description: 'Aplicación para obtener información del dólar en Argentina.',
            link: 'https://dolargaucho.com',
            icon: 'https://via.placeholder.com/50?text=DG'
        },
        {
            platform: 'Hacklabdog',
            username: 'Hacklabdog',
            description: 'Portfolio personal y blog sobre tecnología.',
            link: 'https://hacklabdog.com',
            icon: 'https://hacklabdog.com/wp-content/uploads/2021/07/hacklabdog-logo.png'
        }
    ];
</script>

<!-- Contenedor principal con fondo animado -->
<div class="flex flex-col items-center justify-center min-h-screen text-white bg-gradient-to-r from-gray-800 via-gray-900 to-black bg-[length:200%] animate-gradient-x">
    <!-- Sección de perfil -->
    <div class="text-center">
        <!-- Imagen del perfil centrada -->
        <div class="flex justify-center">
            <img src={profile.image} alt={profile.name} class="w-32 h-32 rounded-full border-4 border-white mb-4" />
        </div>
        <!-- Nombre del perfil -->
        <h1 class="text-4xl font-bold mb-2">{profile.name} 
            {#if profile.verified} 
                <span class="text-blue-500 text-lg">✔</span> 
            {/if}
        </h1>
        <!-- Descripción del perfil actualizada -->
        <p class="text-gray-100 max-w-xl mx-auto">{profile.description}</p>
    </div>

    <!-- Sección de enlaces a proyectos -->
    <div class="mt-8 p-4 w-full max-w-lg">
        {#each links as link}
            <div class="flex items-center bg-gray-800 p-4 rounded-lg mb-4 hover:bg-gray-700 transition duration-300">
                <img src={link.icon} alt={link.platform} class="w-12 h-12 mr-4 rounded" />
                <div class="flex-grow">
                    <h2 class="text-lg font-semibold">{link.username}</h2>
                    <p class="text-gray-400">{link.description}</p>
                </div>
                <a href={link.link} target="_blank" class="text-blue-500 text-2xl">🔗</a>
            </div>
        {/each}
    </div>
</div>
