<template>
    <div class="flex min-h-screen p-4 bg-gradient-to-br from-gray-300 to-gray-50 text-gray-800">
        <div class="flex flex-col justify-between min-h-full min-w-full pt-8 pb-4 lg:pt-16 pl-6 md:pl-16 lg:pl-24 pr-8 bg-white rounded-lg shadow">
            <div>
                <div class="relative z-20 flex justify-between items-center">
                    <div class="flex md:block lg:flex items-center max-w-full">
                        <div class="mb-0 md:mb-4 lg:mb-0 flex flex-no-shrink pr-4 md:pr-6 lg:pr-14">
                            <a href="/" class="flex items-center rounded-full shadow-lg border-4 border-white">
                                <img src="https://avatars.githubusercontent.com/u/11693661" alt="profile picture" class="h-10 w-10 md:h-16 md:w-16 lg:h-24 lg:w-24 rounded-full">
                            </a>
                        </div>

                        <div>
                            <a href="/" class="block no-underline text-2xl lg:text-3xl font-extrabold">Timothé Pearce</a>

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

                    <!-- <div class="block md:hidden">
                        <button class="block">
                            <svg fill="currentColor" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" class="block text-black h-6 w-6 block" style="display: block;">
                                <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z"></path>
                            </svg>
                            <svg fill="currentColor" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" class="text-black h-6 w-6 hidden" style="display: none;">
                                <path d="M10 8.586L2.929 1.515 1.515 2.929 8.586 10l-7.071 7.071 1.414 1.414L10 11.414l7.071 7.071 1.414-1.414L11.414 10l7.071-7.071-1.414-1.414L10 8.586z"></path>
                            </svg>
                        </button>
                    </div> -->
                </div>

                <!-- <div class="md:hidden z-10 bg-white fixed pin pt-24 hidden" style="display: none;">
                    <div class="spaced-y-8 overflow-y-auto pt-6 pb-8 px-12 max-h-full overflow-y-auto">
                        <a href="/articles" class="block text-black font-bold no-underline">Articles</a>
                        <a href="/projects" class="block text-black font-bold no-underline">Projects</a>
                    </div>
                </div> -->

                <div class="lg:pl-40 mt-12">
                    <div class="max-w-xl">
                        <h1 class="text-2xl font-extrabold mb-4">Who am I?</h1>
                        <div class="text-lg text-gray-700 font-light space-y-6">
                            <p>Lorem ipsum dolor sin lorem ipsum dolor sin lorem ipsum dolor sin lorem ipsum dolor sin <a href="/about" class="text-black font-bold">about</a>, <a href="/articles" class="text-black font-bold">articles</a> and more and more...</p>
                            
                            <p>Donec tincidunt arcu non nunc luctus aliquet. In felis dui, pretium id est at, euismod finibus massa. Nunc ac molestie quam. Curabitur at lacinia magna. Praesent eget dignissim elit. Maecenas aliquam cursus enim, a condimentum mi. Nullam consectetur sollicitudin posuere.</p>

                            <p>Right now I'm working at <a href="/going-full-time-on-tailwind-css" class="text-black font-bold underline">Les petits bots</a> as a CTO, etc.</p>
                        </div>
                    </div>
                </div>
            </div>

            <div class="flex justify-end text-xs space-x-4 text-gray-400">
                <a href="mailto:timothe.pearce@gmail.com" class="font-semibold no-underline hover:text-black">timothe.pearce@gmail.com</a>
                <span>-</span>
                <a href="http" class="font-semibold no-underline hover:text-black">GitHub</a>
                <span>-</span>
                <a href="http" class="font-semibold no-underline hover:text-black">LinkedIn</a>
                <span>-</span>
                <a href="http" class="font-semibold no-underline hover:text-black">Twitter</a>
            </div>
        </div>
    </div>
</template>