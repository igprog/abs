<template>
  <div>
    <div class="container pt-5">
      <h2 class="pt-5">{{ $t('contact') }}</h2>
      <hr>
      <div class="row mt-5">
        <div class="col-lg-4 pb-5">
          <c-contact :showIcon="true" aColor="#000" />
        </div>
        <div class="col-lg-4 text-center py-3">
          <img :src="require(`@/assets/img/street_view.png`)" alt="street_view" class="img-fluid" />
        </div>
        <div class="col-lg-4 py-3">
          <c-map />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import cContact from "../components/cContact.vue";
import cMap from "../components/cMap.vue";
export default {
  metaInfo () {
    return {
      title: this.$t('appName') + ', ' + this.$t('appDesc'),
      titleTemplate: '%s | ' + this.$t('contact'),
    }
  },
  components: {
    cContact,
    cMap,
  },
};
</script>