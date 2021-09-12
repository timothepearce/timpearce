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

                <div v-if="hasContent" class="flex-shrink-0 self-center flex">
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

                <div v-show="open" class="mt-4">
                    <div v-html="content"></div>

                    <div>
                        <agile class="mb-4" ref="main" :options="options1" :as-nav-for="asNavFor1">
                            <div class="slide" v-for="(slide, index) in slides" :key="index" :class="`slide--${index}`"><img :src="slide" /></div>
                        </agile>
                        
                        <agile class="thumbnails" ref="thumbnails" :options="options2" :as-nav-for="asNavFor2">
                            <div class="slide slide--thumbniail" v-for="(slide, index) in slides" :key="index" :class="`slide--${index}`" @click="$refs.thumbnails.goTo(index)"><img :src="slide" /></div><template slot="prevButton"><i class="fas fa-chevron-left"></i></template><template slot="nextButton"><i class="fas fa-chevron-right"></i></template>
                        </agile>
                    </div>
                </div>
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
        },

        content: {
            type: String,
        }
    },

    data() {
        return {
            open: false,
            asNavFor1: [],
			asNavFor2: [],
			options1: {
				dots: false,
				fade: true,
				navButtons: false
			},
			
			options2: {
				autoplay: true,
				centerMode: true,
				dots: false,
				navButtons: false,
				slidesToShow: 3,
				responsive: [
                {
                    breakpoint: 600,
                    settings: {
                        slidesToShow: 5
                    }
                },
                
                {
                    breakpoint: 1000,
                    settings: {
                        navButtons: true
                    }
                }
            ]
				
			},
			
			slides: [
					'https://images.unsplash.com/photo-1453831362806-3d5577f014a4?ixlib=rb-1.2.1&q=85&fm=jpg&crop=entropy&cs=srgb&w=1600&fit=max&ixid=eyJhcHBfaWQiOjE0NTg5fQ',
					'https://images.unsplash.com/photo-1496412705862-e0088f16f791?ixlib=rb-1.2.1&q=85&fm=jpg&crop=entropy&cs=srgb&w=1600&fit=max&ixid=eyJhcHBfaWQiOjE0NTg5fQ',
					'https://images.unsplash.com/photo-1506354666786-959d6d497f1a?ixlib=rb-1.2.1&q=85&fm=jpg&crop=entropy&cs=srgb&w=1600&fit=max&ixid=eyJhcHBfaWQiOjE0NTg5fQ',
					'https://images.unsplash.com/photo-1455619452474-d2be8b1e70cd?ixlib=rb-1.2.1&q=85&fm=jpg&crop=entropy&cs=srgb&w=1600&fit=max&ixid=eyJhcHBfaWQiOjE0NTg5fQ',
					'https://images.unsplash.com/photo-1504674900247-0877df9cc836?ixlib=rb-1.2.1&q=85&fm=jpg&crop=entropy&cs=srgb&w=1600&fit=max&ixid=eyJhcHBfaWQiOjE0NTg5fQ',
					'https://images.unsplash.com/photo-1472926373053-51b220987527?ixlib=rb-1.2.1&q=85&fm=jpg&crop=entropy&cs=srgb&w=1600&fit=max&ixid=eyJhcHBfaWQiOjE0NTg5fQ',
					'https://images.unsplash.com/photo-1497534547324-0ebb3f052e88?ixlib=rb-1.2.1&q=85&fm=jpg&crop=entropy&cs=srgb&w=1600&fit=max&ixid=eyJhcHBfaWQiOjE0NTg5fQ'
				]
        }
    },

    mounted () {
		this.asNavFor1.push(this.$refs.thumbnails);
		this.asNavFor2.push(this.$refs.main);
	},

    computed: {
        hasContent() {
            return this.content !== undefined;
        }
    },

    methods: {
        toggle() {
            this.open = !this.open;
        }
    }
}
</script>
