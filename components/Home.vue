<template>
    <div class="flex min-h-screen p-2 lg:p-4 bg-gradient-to-br from-gray-300 to-gray-50 text-gray-800">
        <div class="flex flex-col justify-between min-h-full min-w-full pt-8 pb-4 lg:pt-16 px-4 md:pl-16 lg:pl-24 bg-white rounded-lg shadow">
            <div class="mb-12">
                <Header />

                <div class="lg:pl-40 mt-12">
                    <div class="max-w-xl">
                        <h1 class="text-2xl font-extrabold mb-6">Who am I?</h1>
                        <div class="text-lg text-gray-700 font-light space-y-8">
                            <p>Hi, I’m <a target="_blank" href="https://twitter.com/TimothePearce" class="font-semibold underline text-black">@TimothePearce</a>, a software engineer (full-stack developer) based in Paris.
                            
                            <p>I spent the last seven years studying computer science, gaining a wide variety of skills, from front-end development to DevOps, and <a target="_blank" href="https://lepetitmartin.com" class="text-black font-semibold underline">building reliable software solutions</a>.</p>

                            <p>What do I do now? I am CTO for the French company <a target="_blank" href="https://lepetitmartin.com" class="text-black font-semibold underline">Les petits bots</a>, where I build chatbots and explore the wonderful <span class="line-through">but unfinished</span> world of Machine Learning, especially Natural Language Processing.</p>

                            <p>If you are interested in learning more about me, you can read my <a href="/about" class="font-semibold underline text-black">full resume</a>, <a href="/articles" class="font-semibold underline text-black">articles</a> or <a target="_blank" href="mailto:timothe.pearce@gmail.com" class="text-black font-semibold underline">email me</a>. If you’d like to work with me, I’m also available as a <a target="_blank" href="https://www.malt.fr/dashboard/freelancer" class="text-black font-semibold underline">freelancer</a>.</p>
                        </div>
                    </div>
                </div>
            </div>

            <div class="flex flex-wrap justify-end text-xs space-x-2 text-gray-400">
                <a target="_blank" href="mailto:timothe.pearce@gmail.com" class="font-semibold no-underline hover:text-black">Email</a>
                <span>-</span>
                <a target="_blank" href="https://github.com/TimothePearce" class="font-semibold no-underline hover:text-black">GitHub</a>
                <span>-</span>
                <a target="_blank" href="https://www.linkedin.com/in/timothepearce" class="font-semibold no-underline hover:text-black">LinkedIn</a>
                <span>-</span>
                <a target="_blank" href="https://twitter.com/TimothePearce" class="font-semibold no-underline hover:text-black">Twitter</a>
            </div>
        </div>
    </div>
</template>