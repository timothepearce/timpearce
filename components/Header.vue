<template>
    <div>
        <div class="relative z-20 flex justify-between items-center">
            <div class="flex md:block lg:flex items-center max-w-full">
                <div class="mb-0 md:mb-4 lg:mb-0 flex flex-no-shrink pr-2 md:pr-6 lg:pr-14">
                    <a href="/" class="flex items-center rounded-full shadow-lg border-4 border-white">
                        <img src="https://avatars.githubusercontent.com/u/11693661" alt="profile picture" class="h-10 w-10 md:h-16 md:w-16 lg:h-24 lg:w-24 rounded-full">
                    </a>
                </div>

                <div>
                    <NuxtLink to="/" class="block no-underline text-xl md:text-2xl lg:text-3xl font-extrabold">Timothé Pearce</NuxtLink>

                    <div class="hidden md:flex mt-6 uppercase tracking-wide text-xs space-x-6 text-gray-400">
                        <NuxtLink to="/about" class="font-semibold no-underline hover:text-gray-800">About</NuxtLink>
                        <NuxtLink to="/articles" class="font-semibold no-underline hover:text-gray-800">Articles</NuxtLink>
                        <NuxtLink to="/projects" class="font-semibold no-underline hover:text-gray-800">Projects</NuxtLink>
                        <a href="https://www.malt.fr/profile/timothepearce" target="_blank" class="flex items-center font-semibold no-underline hover:text-gray-800">
                            Hire me
                            <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 ml-1" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14" />
                            </svg>
                        </a>
                    </div>
                </div>
            </div>

            <div class="block md:hidden">
                <button @click="toggleMenu()" class="block">
                    <svg v-if="!menuOpen" xmlns="http://www.w3.org/2000/svg" class="text-gray-800 h-7 w-7 md:hidden" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
                    </svg>

                    <svg v-else xmlns="http://www.w3.org/2000/svg" class="text-gray-800 h-7 w-7 md:hidden" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
                    </svg>
                </button>
            </div>
        </div>

        <div v-if="menuOpen" class="mt-12 ml-6">
            <div class="text-2xl space-y-10">
                <NuxtLink to="/about" @click.native="toggleMenu()" class="block font-bold no-underline text-gray-800">About</NuxtLink>
                <NuxtLink to="/articles" @click.native="toggleMenu()" class="block font-bold no-underline text-gray-800">Articles</NuxtLink>
                <NuxtLink to="/projects" @click.native="toggleMenu()" class="block font-bold no-underline text-gray-800">Projects</NuxtLink>
                <a @click="toggleMenu()" href="https://www.malt.fr/profile/timothepearce" target="_blank" class="flex items-center font-bold no-underline text-gray-800">
                    Hire me
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 ml-1" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14" />
                    </svg>
                </a>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            menuOpen: false,
        }
    },

    methods: {
        toggleMenu() {
            this.menuOpen = !this.menuOpen;
            this.$emit('toggle-menu');
        }
    }
}
</script>
