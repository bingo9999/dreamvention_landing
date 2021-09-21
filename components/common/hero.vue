<template>
    <div v-if="hero" id="hero">
                <div class="container">
                    <div class="row">
                        <div class="col-md-6 col-xs-12">
                            <div class="hero-block">
                                <div>
                                    <p class="text-left">{{hero.Decided}}<br>{{hero.Support}}</p>
                                    <p class="text-left">{{hero.Gethelp}}<br>{{hero.Commercial}}</p>
                                </div>
                            </div>
                        </div>
                        <div class="col-md-6 col-xs-12">
                            <img src="~assets/banner-logo.png">
                        </div>
                    </div>
                </div>
            </div>
</template>

<script>

  export default {
    data(){
        return {
            hero: null
        };

    },
    async mounted(){
        const main = await this.$content('main').fetch();
        this.hero = main.hero
    }
  }

</script>