<template>
    <Hero/>
    <About id='about'/>
    <Features id='features'/>
    <Programs id='programs'/>
    <Partnerships id='partnerships'/>
    <Donate id='donate'/>
    <Contact id='contact'/>
    <Footer/>
</template>

<script setup>

useSeoMeta({
  title: 'Harmony Health Foundation',
  ogTitle: 'Harmony Health Foundation',
  description: 'Empowering Healthcare. Supporting Communities.',
  ogDescription: 'Empowering Healthcare. Supporting Communities.',
  ogImage: '/logo.jpg',
  twitterCard: 'summary_large_image',
})

</script>