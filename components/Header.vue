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
                    <a href="/" class="block no-underline text-xl md:text-2xl lg:text-3xl font-extrabold">Timothé Pearce</a>

                    <div class="hidden md:flex mt-6 uppercase tracking-wide text-xs space-x-6 text-gray-400">
                        <a href="/about" class="font-semibold no-underline hover:text-black">About</a>
                        <a href="/articles" class="font-semibold no-underline hover:text-black">Articles</a>
                        <a href="/projects" class="font-semibold no-underline hover:text-black">Projects</a>
                        <a href="/freelance" class="flex items-center font-semibold no-underline hover:text-black">
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
                    <svg v-if="!menuOpen" xmlns="http://www.w3.org/2000/svg" class="text-black h-7 w-7 md:hidden" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
                    </svg>

                    <svg v-else xmlns="http://www.w3.org/2000/svg" class="text-black h-7 w-7 md:hidden" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
                    </svg>
                </button>
            </div>
        </div>

        <!-- <div class="md:hidden z-10 bg-white fixed pin pt-24 hidden" style="display: none;">
            <div class="spaced-y-8 overflow-y-auto pt-6 pb-8 px-12 max-h-full overflow-y-auto">
                <a href="/articles" class="block text-black font-bold no-underline">Articles</a>
                <a href="/projects" class="block text-black font-bold no-underline">Projects</a>
            </div>
        </div> -->
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
        }
    }
}
</script>
