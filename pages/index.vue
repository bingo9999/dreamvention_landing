<template>
    <div>
        <CommonHeader />
        <main>
            <CommonHero />
            <CommonSupport />
            <CommonDreamvention />
            <CommonReviews />
            <CommonPricing />
            <CommonFrequently />
            <CommonFooter />
        </main>

    </div>
</template>

<script>
import CommonHeader from '@/components/common/header.vue';
import CommonHero from '@/components/common/hero.vue';
import CommonSupport from '@/components/common/support.vue';
import CommonDreamvention from '@/components/common/dreamvention.vue';
import CommonReviews from '@/components/common/reviews.vue';
import CommonPricing from '@/components/common/pricing.vue';
import CommonFrequently from '@/components/common/frequently.vue';
import CommonFooter from '@/components/common/footer.vue';

  export default {
    components: {
        CommonHeader,
        CommonHero,
        CommonSupport,
        CommonDreamvention,
        CommonReviews,
        CommonPricing,
        CommonFrequently,
        CommonFooter
    },
    async asyncData({ $content }) {
      const header = await $content('header').fetch();
      const main = await $content('main').fetch();
      
      return {
        header,
        main
      }
    }
  }

</script>
