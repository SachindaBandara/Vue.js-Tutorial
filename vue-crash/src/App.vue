<script setup>
import Hero from "./components/Hero.vue";
import HomeCard from "./components/HomeCard.vue";
import JobsListing from "./components/JobsListing.vue";
import Navbar from "./components/Navbar.vue";
</script>
<template>
  <Navbar />
  <Hero title="Become a Vue Job" />
  <HomeCard />
  <JobsListing :limit="3" :showButton="true"/>
</template>
