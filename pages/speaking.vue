<template>
  <div class="max-w-5xl mx-auto px-8">
    <Header/>
    <div class="mb-20 md:flex mt-10 lg:mt-6 items-baseline md:border-t md:border-gray-400 md:pt-2 lg:border-t-0 lg:pt-0">
      <div class="w-full md:w-1/3">
        <h2 class="font-medium sm:font-normal text-xl sm:text-2xl md:text-3xl lg:text-4xl text-gray-900">Speaking</h2>
      </div>
      <div class="w-full md:w-2/3 mt-6">
        <p class="text-lg sm:text-xl lg:text-2xl text-gray-700">I’ve had the pleasure of speaking at design and front-end conferences all around the world. <a href="mailto:&#115;&#109;&#046;&#115;&#099;&#104;&#111;&#103;&#101;&#114;&#064;&#103;&#109;&#097;&#105;&#108;&#046;&#099;&#111;&#109;" class="border-b border-gray-900 pb-px text-gray-900">Contact me</a> if you think I would make a great fit at your conference. </p>
        <div class="mt-6 lg:mt-10 border-b border-gray-400">
          <Talk :talk="talk" v-for="talk in talks"/>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
    import Header from "../components/Header"
    import Talk from "../components/Talk"
export default {
    components: { Header, Talk },
  data() {
    return {
      talks: [{
          talkTitle: 'How to Think Like a Visual Designer',
          conference: 'Laracon US',
          conferenceUrl: 'https://laracon.us/',
          location: 'New York, USA',
          date: 'July 24 - 25, 2019',
          videoUrl: null,
          slidesUrl: 'https://speakerdeck.com/steveschoger/how-to-think-like-a-visual-designer',
        },
        {
          talkTitle: 'Practical Solutions to Common UI Design Problems',
          conference: 'CSSDay',
          conferenceUrl: 'https://cssday.nl/2019',
          location: 'Amsterdam, NL',
          date: 'June 13 - 14, 2019',
          videoUrl: 'https://youtu.be/7Z9rrryIOC4',
          slidesUrl: null,
        },
        {
          talkTitle: 'Practical Solutions to Common UI Design Problems (no slides)',
          conference: 'Smashing Conference',
          conferenceUrl: 'https://smashingconf.com/',
          location: 'San Francisco, USA',
          date: 'April 21 - 22, 2019',
          videoUrl: null,
          slidesUrl: null,
        },
        {
          talkTitle: 'Practical Solutions to Common UI Design Problems',
          conference: 'Laracon Online',
          conferenceUrl: 'https://laracon.net/',
          location: 'Online',
          date: 'March 6, 2019',
          videoUrl: null,
          slidesUrl: null,
        },
        {
          talkTitle: 'Refactoring UI',
          conference: 'Laracon AU',
          conferenceUrl: '/',
          location: 'Sydney, AU',
          date: 'October 17 - 18, 2018',
          videoUrl: null,
          slidesUrl: null,
        },
        {
          talkTitle: '15 Practical Tips for Cheating at Design',
          conference: 'Fluxible',
          conferenceUrl: '/',
          location: 'Waterloo, CA',
          date: 'September 22 - 23, 2018',
          videoUrl: null,
          slidesUrl: 'https://speakerdeck.com/steveschoger/fluxible-15m',
        },
        {
          talkTitle: 'The Little Details of UI Design',
          conference: 'Laracon Online',
          conferenceUrl: 'https://laracon.net/',
          location: 'Online',
          date: 'February 2, 2019',
          videoUrl: 'https://laracon.net/2018',
          slidesUrl: 'https://speakerdeck.com/sschoger/the-little-details-of-ui-design',
        },
      ]
    }
  }
}
</script>
