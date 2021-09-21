<template>
    <div v-if="pricing" id="pricing">
        <h1 class="text-center">{{pricing.Pricing}}</h1>
        
        <div class="container">
            <div class="row pricing-row">
                <div class="pricing-cols col-md-3 text-center center-block">
                    <div class="pricing-col">
                        <div class="price-col-name">
                            <p class="pricename">{{pricing.Starter}}</p>
                        </div>
                        <div>
                            <p><span class="cost">{{pricing.Cost29}}</span><span class="mo">{{pricing.Mo}}</span></p>
                            <p class="pricing-description">{{pricing.Good}}</p>
                        </div>
                    </div>
                </div>
                <div class="pricing-cols-center col-md-4 text-center center-block">
                    <div class="col-md-12 text-center">
                        <img class="recommended" src="~assets/features/recommended.svg"/>
                    </div>
                    <div class="pricing-col-center">
                        <div class="price-col-name">
                            <p class="pricename_center">{{pricing.Startlorem}}</p>
                        </div>
                        <div>
                            <p><span class="cost cost-center">{{pricing.Cost49}}</span><span class="mo">{{pricing.Mo}}</span></p>
                            <p class="pricing-description-center">{{pricing.Design}}</p>
                        </div>
                    </div>
                </div>
                <div class="pricing-cols col-md-3 text-center center-block">
                    <div class="pricing-col">
                        <div class="price-col-name">
                            <p class="pricename">{{pricing.Advance}}</p>
                        </div>
                        <div>
                            <p><span class="cost">{{pricing.Cost288}}</span><span class="mo">{{pricing.Mo}}</span></p>
                            <p class="pricing-description">{{pricing.Great}}</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>

  export default {
    data(){
        return {
            pricing: null
        };

    },
    async mounted(){
        const main = await this.$content('main').fetch();
        this.pricing = main.pricing
    }
  }

</script> 