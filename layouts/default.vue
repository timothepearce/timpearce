<template>
    <div class="flex min-h-screen p-2 lg:p-4 bg-gradient-to-br from-gray-300 to-gray-50 text-gray-800">
        <div class="flex flex-col justify-between min-h-full min-w-full pt-8 pb-4 lg:pt-16 px-4 md:pl-16 lg:pl-24 bg-white rounded-lg shadow">
            <div class="mb-12">
                <Header @toggle-menu="toggleMenu()"/>

                <div v-show="!menuOpen" class="lg:pl-40 mt-12">
                    <div class="max-w-xl">
                        <Nuxt />
                    </div>
                </div>
            </div>

            <div class="flex flex-wrap justify-end text-xs space-x-2 text-gray-400">
                <a target="_blank" href="mailto:timothe.pearce@gmail.com" class="font-semibold no-underline hover:text-gray-800">Email</a>
                <span>-</span>
                <a target="_blank" href="https://github.com/TimothePearce" class="font-semibold no-underline hover:text-gray-800">GitHub</a>
                <span>-</span>
                <a target="_blank" href="https://www.linkedin.com/in/timothepearce" class="font-semibold no-underline hover:text-gray-800">LinkedIn</a>
                <span>-</span>
                <a target="_blank" href="https://twitter.com/TimothePearce" class="font-semibold no-underline hover:text-gray-800">Twitter</a>
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
        }
    }
}
</script>
