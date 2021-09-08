<template>
    <div>
        <h1 class="text-2xl font-extrabold">Projects</h1>
        <div class="text-lg text-gray-700 font-light mt-6">
            <p>Here you’ll find a list of the most important projects I worked on during the past years.</p>
        </div>

        <div class="mt-6 space-y-6">
            <ProjectCard
                name="Les petits bots"
                dates="From June 2018 until now"
                external-link="https://lespetitsbots.com"
                logoUrl="https://avatars.githubusercontent.com/u/39500458?s=200&v=4"
                abstract="Les petits bots is a startup I co-founded. We built a SaaS product allowing customers to create chatbots based on a Natural Language Understanding technology."
            ></ProjectCard>

            <ProjectCard
                name="HUSH"
                dates="From October 2019 to January 2020"
                external-link="https://hush-news.com"
                logoUrl="/img/hush.svg"
                abstract="HUSH is a news media targetting communication students, composed of a website and a CMS with advanced editing and notifications features."
            ></ProjectCard>

            <ProjectCard
                name="Evaneos"
                dates="From September 2017 to October 2019"
                external-link="https://evaneos.fr"
                logoUrl="https://avatars.githubusercontent.com/u/344797?s=200&v=4"
                abstract="Evaneos is a platform connecting local travel agents and users wishing to create a tailor-made trip. I worked there with a large team of 35 developers."
            ></ProjectCard>

            <ProjectCard
                name="Doplr"
                dates="From March 2017 to June 2017"
                external-link="https://github.com/doplr-app"
                logoUrl="https://avatars.githubusercontent.com/u/23485669?s=200&v=4"
                abstract="Doplr is an iOS app developed with <a href='https://github.com/rgehan' target='_blank' class='font-semibold underline'>@rgehan</a>. The product aims to notify the user when a nearby concert matches his musical profile."
            ></ProjectCard>
        </div>
    </div>
</template>