<template>
  <div class="max-w-5xl mx-auto px-8">
    <Header/>
    <div class="mb-20 md:flex mt-10 lg:mt-6 items-baseline md:border-t md:border-gray-400 md:pt-2 lg:border-t-0 lg:pt-0">
      <div class="w-full md:w-1/3">
        <h2 class="font-medium sm:font-normal text-xl sm:text-2xl md:text-3xl lg:text-4xl text-gray-900">Interviews</h2>
      </div>
      <div class="w-full md:w-2/3 mt-6">
        <p class="text-lg sm:text-xl lg:text-2xl text-gray-700">I've been a guest a handful of podcasts where I engaged in conversations about everything from design tips to my life's story. Here are some of my favorite interviews: </p>
        <div class="mt-6 lg:mt-10 border-b border-gray-400">
          <div class="border-t border-gray-400 py-6 sm:py-8 lg:py-10" v-for="interview in interviews">
            <div class="lg:flex items-center justify-between">
              <div>
                <h3 class="text-gray-900 sm:text-lg lg:text-xl"><a :href="interview.podcastUrl" class="hover:underline">{{ interview.podcast }} <span class="text-gray-700">{{ interview.episode }}</span></a></h3>
                <div class="flex text-gray-700 text-sm sm:text-base lg:text-lg mt-2 sm:mt-3 lg:mt-3">
                  <div><span class="italic">with</span> <a :href="interview.hostUrl" class="hover:underline">{{ interview.host }}</a></div>
                  <div class="mx-3 lg:mx-4 text-gray-500">•</div>
                  <div>{{ interview.date }}</div>
                </div>
              </div>
              <div class="flex flex-wrap text-gray-900 text-sm sm:text-base lg:text-lg mt-2 sm:mt-3 lg:mt-0">
                <div class="lg:ml-8">
                  <a :href="interview.podcastUrl" class="flex items-center group">
                    <div class="relative w-6 h-6">
                      <svg class="absolute group-hover:opacity-0 w-6 h-6" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M18.5711 17.5711C22.4763 13.6658 22.4763 7.33418 18.5711 3.42893C14.6658 -0.47631 8.33418 -0.476311 4.42893 3.42893C0.523689 7.33418 0.523689 13.6658 4.42893 17.5711M15.7426 14.7426C18.0858 12.3995 18.0858 8.60051 15.7426 6.25736C13.3995 3.91421 9.60051 3.91421 7.25736 6.25736C4.91421 8.60051 4.91421 12.3995 7.25736 14.7426" stroke="#1A202C" stroke-linecap="round" />
                        <path d="M13.5 10.5C13.5 11.6046 12.6046 12.5 11.5 12.5C10.3954 12.5 9.5 11.6046 9.5 10.5C9.5 9.39543 10.3954 8.5 11.5 8.5C12.6046 8.5 13.5 9.39543 13.5 10.5Z" stroke="#1A202C" />
                        <path d="M9.5 14.5H13.5L12.5 22.5H10.5L9.5 14.5Z" stroke="#1A202C" stroke-linejoin="round" />
                      </svg>
                      <svg class="absolute opacity-0 group-hover:opacity-100 w-6 h-6" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M18.5711 17.5711C22.4763 13.6658 22.4763 7.33418 18.5711 3.42893C14.6658 -0.47631 8.33418 -0.476311 4.42893 3.42893C0.523689 7.33418 0.523689 13.6658 4.42893 17.5711M15.7426 14.7426C18.0858 12.3995 18.0858 8.60051 15.7426 6.25736C13.3995 3.91421 9.60051 3.91421 7.25736 6.25736C4.91421 8.60051 4.91421 12.3995 7.25736 14.7426" stroke="#1A202C" stroke-linecap="round" />
                        <path d="M14 10.5C14 11.8807 12.8807 13 11.5 13C10.1193 13 9 11.8807 9 10.5C9 9.11929 10.1193 8 11.5 8C12.8807 8 14 9.11929 14 10.5Z" fill="#1A202C" />
                        <path d="M9.12516 14.1691C9.22008 14.0616 9.35659 14 9.5 14H13.5C13.6434 14 13.7799 14.0616 13.8748 14.1691C13.9698 14.2766 14.0139 14.4197 13.9961 14.562L12.9961 22.562C12.9649 22.8122 12.7522 23 12.5 23H10.5C10.2478 23 10.0351 22.8122 10.0039 22.562L9.00386 14.562C8.98608 14.4197 9.03025 14.2766 9.12516 14.1691Z" fill="#1A202C" />
                      </svg>
                    </div>
                    <div class="mt-px ml-2 lg:hidden">Listen to this episode</div>
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
      interviews: [{
          podcast: 'Yo! Podcast',
          episode: '#005',
          host: 'Rob Hope',
          hostUrl: 'https://twitter.com/robhope',
          date: 'May 15, 2019',
          podcastUrl: 'https://onepagelove.com/podcast-005',
        },
        {
          podcast: 'The Laravel Podcast',
          episode: 'Episode 17',
          host: 'Matt Stauffer',
          hostUrl: 'https://twitter.com/stauffermatt',
          date: 'February 8, 2019',
          podcastUrl: 'https://laravelpodcast.com/episodes/89e3758b',
        },
        {
          podcast: 'Fullstack Radio',
          episode: 'Episode 103: Design Q&A + Refactoring UI Details',
          host: 'Adam Wathan',
          hostUrl: 'https://twitter.com/adamwathan',
          date: 'December 5, 2019',
          podcastUrl: 'http://www.fullstackradio.com/103',
        },
        {
          podcast: 'Fullstack Radio',
          episode: 'Episode 74: Tactical Design Advice for Developers',
          host: 'Adam Wathan',
          hostUrl: 'https://twitter.com/adamwathan',
          date: 'October 12, 2017',
          podcastUrl: 'http://www.fullstackradio.com/74',
        },
      ]
    }
  }
}
</script>
