<template>
  <div class="max-w-5xl mx-auto px-8">
    <Header />
    <div class="mb-20 md:flex mt-10 lg:mt-6 items-baseline md:border-t md:border-gray-400 md:pt-2 lg:border-t-0 lg:pt-0">
      <div class="w-full md:w-1/3">
        <h2 class="font-medium sm:font-normal text-xl sm:text-2xl md:text-3xl lg:text-4xl text-gray-900">Projects</h2>
      </div>
      <div class="w-full md:w-2/3 mt-6">
        <p class="text-lg sm:text-xl lg:text-2xl text-gray-700">I've been a guest a handful of podcasts where I engaged in conversations about everything from design tips to my life's story. Here are some of my favorite interviews: </p>
        <div class="mt-6 lg:mt-10 border-b border-gray-400">
          <div class="border-t border-gray-400 py-6 sm:py-8 lg:py-10" v-for="project in projects">
            <div class="lg:flex items-center justify-between">
              <div>
                <h3 class="text-gray-900 sm:text-lg lg:text-xl"><a :href="project.projectUrl" class="hover:underline">{{ project.projectName }}</a></h3>
                <div class="flex text-gray-700 text-sm sm:text-base lg:text-lg mt-2 sm:mt-3 lg:mt-3">
                  {{ project.description }}
                </div>
              </div>
              <div class="flex flex-wrap text-gray-900 text-sm sm:text-base lg:text-lg mt-2 sm:mt-3 lg:mt-0">
                <div class="lg:ml-8">
                  <a :href="project.projectUrl" class="flex items-center group hover:underline">
                    <div class="relative w-6 h-6">
                      <svg class="absolute group-hover:opacity-0 w-6 h-6" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M19.5 11V21.5H2.5V4.5H13" stroke="#1A202C" />
                        <path d="M7.5 16.5L21.5 2.5" stroke="#1A202C" stroke-linecap="round" />
                        <path d="M15 2.5H21.5V9" stroke="#1A202C" />
                      </svg>
                      <svg class="absolute opacity-0 group-hover:opacity-100 w-6 h-6" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M7.5 16.5L21.5 2.5" stroke="#1A202C" stroke-linecap="round" />
                        <path d="M6.43934 15.4393C5.85355 16.0251 5.85355 16.9749 6.43934 17.5607C7.02512 18.1464 7.97487 18.1464 8.56066 17.5607L20 6.12132V22H2V4H17.8787L6.43934 15.4393Z" fill="#1A202C" />
                        <path d="M15 2.5H21.5V9" stroke="#1A202C" />
                      </svg>
                    </div>
                    <div class="mt-px ml-2 lg:hidden">Check out this project</div>
                  </a>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import Header from "../components/Header"
export default {
  components: { Header },
  data() {
    return {
      projects: [{
          projectName: 'Heroicons',
          description: 'Heroicons are a unique set of icons for your marketing website that make it easy to customize with CSS to better align to your brand.',
          projectUrl: 'http://www.heroicons.com/',
        },
        {
          projectName: 'Hero Patterns',
          description: 'A collection of repeatable SVG background patterns for you to use on your web projects.',
          projectUrl: 'https://www.heropatterns.com/',
        },
        {
          projectName: 'Zondicons',
          description: 'A set of free premium SVG icons for you to use on your digital products.',
          projectUrl: 'https://www.zondicons.com/',
        },
      ]
    }
  }
}

</script>
