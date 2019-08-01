<template>
  <div class="max-w-5xl mx-auto px-8">
    <Header/>
    <div class="mb-20 md:flex mt-6 md:mt-10 lg:mt-6 items-baseline md:border-t md:border-gray-400 md:pt-2 lg:border-t-0 lg:pt-0">
      <div class="w-full md:w-1/3">
        <h2 class="font-medium sm:font-normal text-xl sm:text-2xl md:text-3xl lg:text-4xl text-gray-900">Speaking</h2>
      </div>
      <div class="w-full md:w-2/3 mt-6">
        <p class="text-lg sm:text-xl lg:text-2xl text-gray-700">I’ve had the pleasure of speaking at design and front-end conferences all around the world. <a href="mailto:&#115;&#109;&#046;&#115;&#099;&#104;&#111;&#103;&#101;&#114;&#064;&#103;&#109;&#097;&#105;&#108;&#046;&#099;&#111;&#109;" class="border-b border-gray-900 pb-px text-gray-900">Contact me</a> if you think I would make a great fit at your conference. </p>
        <div class="mt-6 lg:mt-10 border-b border-gray-400">
          <div class="border-t border-gray-400 py-6 sm:py-8 lg:py-10" v-for="talk in talks">
            <div class="lg:flex items-center justify-between">
              <div>
                <h3 class="text-gray-900 sm:text-lg lg:text-xl"><a href="/" class="hover:underline">{{ talk.talkTitle }}</a></h3>
                <div class="flex flex-wrap text-gray-700 text-sm sm:text-base lg:text-lg mt-2 sm:mt-3 lg:mt-3">
                  <a href="/" class="hover:underline hover:text-gray-900">{{ talk.conference }}</a>
                  <div class="mx-3 lg:mx-4 text-gray-500">•</div>
                  <div>{{ talk.location }}</div>
                  <div class="mx-3 lg:mx-4 text-gray-500">•</div>
                  <div>{{ talk.date }}</div>
                </div>
              </div>
              <div class="flex text-gray-900 text-sm sm:text-base lg:text-lg mt-2 sm:mt-3 lg:mt-0">
                <div class="lg:ml-8">
                  <a :href="talk.videoUrl" class="flex items-center group hover:underline">
                    <div class="relative w-6 h-6">
                      <svg class="absolute group-hover:opacity-0 w-6 h-6" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M22.5 11.5C22.5 17.5751 17.5751 22.5 11.5 22.5C5.42487 22.5 0.5 17.5751 0.5 11.5C0.5 5.42487 5.42487 0.5 11.5 0.5C17.5751 0.5 22.5 5.42487 22.5 11.5Z" stroke="#1A202C" />
                        <path d="M8.5 6.89153L16.0411 11.5L8.5 16.1085V6.89153Z" stroke="#1A202C" />
                      </svg>
                      <svg class="absolute opacity-0 group-hover:opacity-100 w-6 h-6" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path fill-rule="evenodd" clip-rule="evenodd" d="M11.5 23C17.8513 23 23 17.8513 23 11.5C23 5.14873 17.8513 0 11.5 0C5.14873 0 0 5.14873 0 11.5C0 17.8513 5.14873 23 11.5 23ZM17 11.5L8 17V6L17 11.5Z" fill="#1A202C" />
                      </svg>
                    </div>
                    <div class="mt-px ml-2 lg:hidden hover:border-b hover:border-gray-900">Watch Video</div>
                  </a>
                </div>
                <div class="ml-8">
                  <a :href="talk.slidesUrl" class="flex items-center group hover:underline">
                    <div class="relative w-6 h-6">
                      <svg class="absolute group-hover:opacity-0 w-6 h-6" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M0.5 2.5H17.5V15.5H0.5V2.5Z" stroke="#1A202C" />
                        <path d="M17 7.5H22.5V20.5H5.5V15" stroke="#1A202C" />
                      </svg>
                      <svg class="absolute opacity-0 group-hover:opacity-100 w-6 h-6" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M0 2H18V16H0V2Z" fill="#1A202C" />
                        <path d="M5 17V21H23V7H19V17H5Z" fill="#1A202C" />
                      </svg>
                    </div>
                    <div class="mt-px ml-2 lg:hidden">View Slides</div>
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
      talks: [{
          talkTitle: 'How to Think Like a Visual Designer',
          conference: 'Laracon US',
          conferenceUrl: '/',
          location: 'New York, USA',
          date: 'July 24 - 25, 2019',
          videoUrl: '/',
          slidesUrl: '/',
        },
        {
          talkTitle: 'Practical Solutions to Common UI Design Problems',
          conference: 'CSSDay',
          conferenceUrl: '/',
          location: 'Amsterdam, NL',
          date: 'June 13 - 14, 2019',
          videoUrl: '/',
          slidesUrl: '/',
        },
        {
          talkTitle: 'Practical Solutions to Common UI Design Problems (no slides)',
          conference: 'Smashing Conference',
          conferenceUrl: '/',
          location: 'San Francisco, USA',
          date: 'April 21 - 22, 2019',
          videoUrl: '/',
          slidesUrl: '/',
        },
        {
          talkTitle: 'Practical Solutions to Common UI Design Problems',
          conference: 'Laracon Online',
          conferenceUrl: '/',
          location: 'Online',
          date: 'March 6, 2019',
          videoUrl: '/',
          slidesUrl: '/',
        },
        {
          talkTitle: 'Refactoring UI',
          conference: 'Laracon AU',
          conferenceUrl: '/',
          location: 'Sydney, AU',
          date: 'October 17 - 18, 2018',
          videoUrl: '/',
          slidesUrl: '/',
        },
        {
          talkTitle: '15 UI Design Tips in 15 Minutes',
          conference: 'Fluxible',
          conferenceUrl: '/',
          location: 'Waterloo, CA',
          date: 'September 22 - 23, 2018',
          videoUrl: '/',
          slidesUrl: '/',
        },
        {
          talkTitle: 'The Little Details of UI Design',
          conference: 'Laracon Online',
          conferenceUrl: '/',
          location: 'Online',
          date: 'February 2, 2019',
          videoUrl: '/',
          slidesUrl: '/',
        },
      ]
    }
  }
}
</script>
