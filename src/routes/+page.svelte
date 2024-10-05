<script>
    const profile = {
        name: "Tomás Maritano",
        description:
            "A product designer with a proven track record of creating innovative and user-centric designs in the IT and software development sectors. Skilled in working in startups and adept at collaborating with cross-functional teams to deliver exceptional products on time and budget.",
        image: "https://media.licdn.com/dms/image/v2/D4D03AQH0MyoFc_QYOw/profile-displayphoto-shrink_800_800/profile-displayphoto-shrink_800_800/0/1706897249816?e=1733356800&v=beta&t=E5HQCkLCW2P72_pgL_-AiRQUa58dHWg8JbVfr4wRqaU",
        verified: true,
    };

    const links = [
        {
            platform: "X",
            username: "@maritanodev",
            description: "Daily notes about daily tasks",
            link: "https://x.com/maritanodev",
            icon: "https://upload.wikimedia.org/wikipedia/commons/6/6f/X_icon.svg",
        },
        {
            platform: "Website",
            username: "www.tomymaritano.com",
            description: "My portfolio website",
            link: "https://www.tomymaritano.com",
            icon: "https://via.placeholder.com/50?text=W",
        },
        {
            platform: "Blink Wave 2.0",
            username: "Music upcoming",
            description: "Music upcoming",
            link: "https://blinkwave.com",
            icon: "https://via.placeholder.com/50?text=M",
        },
        {
            platform: "GitHub",
            username: "Github",
            description: "Some of my projects written.",
            link: "https://github.com/maritanodev",
            icon: "https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png",
        },
    ];
</script>

<div
    class="flex flex-col items-center justify-center min-h-screen bg-gray-900 text-white"
>
    <div class="text-center">
        <div class="flex justify-center">
            <img
                src={profile.image}
                alt={profile.name}
                class="w-32 h-32 rounded-full border-4 border-white mb-4"
            />
        </div>

        <h1 class="text-4xl font-bold mb-2">
            {profile.name}
            {#if profile.verified}
                <span class="text-blue-500 text-lg">✔</span>
            {/if}
        </h1>
        <p class="text-gray-400 max-w-xl mx-auto">{profile.description}</p>
    </div>

    <div class="mt-8 w-full max-w-lg">
        {#each links as link}
            <div
                class="flex items-center bg-gray-800 p-4 rounded-lg mb-4 hover:bg-gray-700 transition duration-300"
            >
                <img
                    src={link.icon}
                    alt={link.platform}
                    class="w-12 h-12 mr-4 rounded"
                />
                <div class="flex-grow">
                    <h2 class="text-lg font-semibold">{link.username}</h2>
                    <p class="text-gray-400">{link.description}</p>
                </div>
                <a
                    href={link.link}
                    target="_blank"
                    class="text-blue-500 text-2xl">🔗</a
                >
            </div>
        {/each}
    </div>
</div>
