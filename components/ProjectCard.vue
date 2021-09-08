<template>
    <div class="bg-white overflow-hidden rounded-lg shadow">
        <div class="bg-white px-4 py-5 sm:px-6">
            <div class="flex space-x-3">
                <div class="flex-shrink-0">
                    <img class="h-10 w-10 rounded-md" :src="logoUrl" alt="logo">
                </div>

                <div class="min-w-0 flex-1">
                    <p class="font-medium text-gray-800">
                        <a :href="externalLink" target="_blank" class="hover:underline">{{ name }}</a>
                    </p>

                    <p class="text-sm text-gray-500">{{ dates }}</p>
                </div>

                <div class="flex-shrink-0 self-center flex">
                    <div class="relative z-30 inline-block text-left">
                        <button @click="toggle()" type="button" class="-m-2 p-2 rounded-full flex items-center">
                            <svg v-if="!open" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-gray-400" viewBox="0 0 20 20" fill="currentColor">
                                <path fill-rule="evenodd" d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" clip-rule="evenodd" />
                            </svg>

                            <svg v-else xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-gray-400" viewBox="0 0 20 20" fill="currentColor">
                                <path fill-rule="evenodd" d="M14.707 12.707a1 1 0 01-1.414 0L10 9.414l-3.293 3.293a1 1 0 01-1.414-1.414l4-4a1 1 0 011.414 0l4 4a1 1 0 010 1.414z" clip-rule="evenodd" />
                            </svg>
                        </button>
                    </div>
                </div>
            </div>

            <div class="text-sm text-gray-800">
                <p class="mt-4" v-html="abstract"></p>

                <!-- <p v-if="open" class="mt-4" v-html="content"></p> -->
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        name: {
            type: String,
            required: true,
        },

        externalLink: {
            type: String,
            required: true,
        },

        logoUrl: {
            type: String,
            required: true,
        },

        dates: {
            type: String,
            required: true,
        },

        abstract: {
            type: String,
            required: true,
        }
    },

    data() {
        return {
            open: false,
        }
    },

    methods: {
        toggle() {
            this.open = !this.open;
        }
    }
}
</script>
