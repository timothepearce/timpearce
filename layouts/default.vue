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

            <Footer />
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
