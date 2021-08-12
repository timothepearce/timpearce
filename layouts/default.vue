<template>
    <div class="flex flex-col justify-between min-h-screen min-w-full pt-8 pb-4 lg:pt-16 px-4 md:pl-16 lg:pl-24 bg-gray-100 text-gray-800">
        <div class="mb-12">
            <Header
                @close-menu="closeMenu()"
                @toggle-menu="toggleMenu()"
            />

            <div v-show="!menuOpen" class="lg:pl-40 mt-12">
                <div class="max-w-xl">
                    <Nuxt />
                </div>
            </div>
        </div>

        <Footer />
    </div>
</template>

<script>
export default {
    head: {
        bodyAttrs: {
            class: 'bg-gray-50',
        }
    },

    data() {
        return {
            menuOpen: false,
        }
    },

    methods: {
        closeMenu() {
            this.menuOpen = false;
        },

        toggleMenu() {
            this.menuOpen = !this.menuOpen;
        },
    }
}
</script>
