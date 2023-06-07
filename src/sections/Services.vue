<template>
  <PageSectionWrapper :id="servicesData.id" :title="servicesData.title" :subtitle="servicesData.subtitle">
    <div class="row text-center">
      <template v-for="item in servicesData.items">
            <h5 class="my-3">{{item.title}}</h5>
            <p class="text-muted" v-html="item.description"></p>
      </template>
    </div>
  </PageSectionWrapper>
</template>

<script setup>
import agencyData from '../data/agency.json'
import PageSectionWrapper from "../components/PageSectionWrapper.vue";
const servicesData = agencyData.services
</script>

<style scoped lang="scss">
@import "../scss/_theming.scss";

@include media-breakpoint-up(md) {
  .item {
    padding-left: 1rem;
    padding-right: 1rem;
  }
}

</style>
