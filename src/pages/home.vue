<template>
  <div>
    <c-header />
    <div class="container">
      <h2 class="pt-4">{{ $t('homePage') }}</h2>
      <hr>
      <!-- <div class="row">
          <div class="col-md-6 text-justify lead">
            {{ $t('mainDesc')}}
          </div>
          <div class="col-md-6">
            <img :src="require(`@/assets/img/home1.png`)" alt="" class="img-fluid" />
          </div>
      </div> -->
      <div class="clearfix">
        <img :src="require(`@/assets/img/home1.png`)" alt="home1" class="img-fluid float-right pl-0 pl-sm-4" width="470" />
        <div class="lead text-justify">{{ $t('mainDesc')}}</div>

      </div>

  
      <div class="row pt-5">
          <div class="col-md-6 text-justify lead">
            <img :src="require(`@/assets/img/home2.png`)" alt="" class="img-fluid pt-2 pb-4" />
          </div>
          <div class="col-md-6">
            <h3 class="font-weight-bold">{{$t('whatOurPlaceOffers')}}</h3>
            <hr/>
            <div v-for="(x, idx) in offers" :key="idx" class="p-1 pl-3">
              <icon :name="x.icon" scale="2" class="text-secondary"></icon>
              <span class="lead text-secondary pl-2">{{ $t(x.title)}}</span>
            </div>
          </div>
      </div>
    </div>
  </div>
</template>

<script>
import cHeader from "../components/cHeader.vue";
export default {
  metaInfo () {
    return {
      title: this.$t('appName') + ', ' + this.$t('appDesc'),
      titleTemplate: '%s | ' + this.$t('homePage'),
    }
  },
  data() {
    return {
      offers: [
        { icon: "utensils", title: "kitchen" },
        { icon: "wifi", title: "wifi" },
        // { icon: "car", title: "freeParkingOnPremises" },
        // { icon: "dog", title: "petsAllowed" },
        { icon: "tv", title: "smartTV" },
        // { icon: "charging-station", title: "eVCharger" },
        { icon: "stop-circle", title: "washer" },
        { icon: "snowflake", title: "airConditioning" }
      ],
    };
  },
  components: {
    cHeader,
  },
};
</script>