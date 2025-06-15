<script setup>
import Hero from "@/components/Hero.vue";
import HomeCard from "@/components/HomeCard.vue";
import JobsListing from "@/components/JobsListing.vue";
</script>
<template>
  <Hero title="Become a Vue Job" />
  <HomeCard />
  <JobsListing :limit="3" :showButton="true" />
</template>
