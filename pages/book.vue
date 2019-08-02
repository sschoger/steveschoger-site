<template>
    <div class="max-w-5xl mx-auto px-8">
        <Header/>
        <div class="mb-20 md:flex mt-10 lg:mt-6 items-baseline md:border-t md:border-gray-400 md:pt-2 lg:border-t-0 lg:pt-0">
            <div class="w-full md:w-1/3">
                <h2 class="font-medium sm:font-normal text-xl sm:text-2xl md:text-3xl lg:text-4xl text-gray-900">Book</h2>
            </div>
            <div class="w-full md:w-2/3 mt-6">
                <div class="text-lg sm:text-xl lg:text-2xl text-gray-700">
                    <p>Learn how to design awesome UIs by yourself using specific tactics explained from a developer's point-of-view.</p>
                    <p class="mt-6"><a href="https://refactoringui.com/book/" class="border-b border-gray-900 pb-px md:pb-1 text-gray-900">Refactoring UI</a> is a book, video series, and a collection of resources I worked on with my friend <a href="https://twitter.com/adamwathan" class="border-b border-gray-900 pb-px md:pb-1 text-gray-900">Adam Wathan</a>. It teaches everything we know about designing for the web, packed into a single comprehensive resource.</p>
                    <p class="mt-6">We’ve already sold over 10,000 copies to developers and designers all around the world.</p>
                    <div class="mt-6">
                        <a href="https://refactoringui.com/book/" class="border-b border-gray-900 pb-px md:pb-1 text-gray-900 text-base sm:text-lg lg:text-xl">Check out Refactoring UI</a>
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
}
</script>