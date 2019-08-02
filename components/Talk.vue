<template>
  <div class="border-t border-gray-400 py-6 sm:py-8 lg:py-10">
    <div class="lg:flex items-center justify-between">
      <div>
        <h3 class="text-gray-900 sm:text-lg lg:text-xl">
        	<span v-if="link === null">{{ talk.talkTitle }}</span>
        	<a v-if="link !== null" :href="link" class="hover:underline">{{ talk.talkTitle }}</a>
        </h3>
        <div class="flex flex-wrap text-gray-700 text-sm sm:text-base lg:text-lg mt-2 sm:mt-3 lg:mt-3">
          <a :href="talk.conferenceUrl" class="hover:underline hover:text-gray-900">{{ talk.conference }}</a>
          <div class="mx-3 text-gray-500">•</div>
          <div>{{ talk.location }}</div>
          <div class="mx-3 text-gray-500">•</div>
          <div>{{ talk.date }}</div>
        </div>
      </div>
      <div class="flex text-gray-900 text-sm sm:text-base lg:text-lg mt-2 sm:mt-3 lg:mt-0">
        <div v-if="talk.videoUrl !== null" class="lg:ml-8">
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
        <div v-if="talk.slidesUrl !== null" :class="{ 'ml-8': talk.videoUrl !== null }">
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
</template>

<script>
	export default {
		props: [ "talk" ],
		computed: {
			link() {
				if (this.talk.videoUrl !== null) {
					return this.talk.videoUrl
				}
				if (this.talk.slidesUrl !== null) {
					return this.talk.slidesUrl
				}
				return null
			}
		}
	}
</script>
