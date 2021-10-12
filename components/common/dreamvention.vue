<template>
    <div v-if="dreamvention" id="dreamvention">
    <h1 class="text-center">{{dreamvention.centertext}}</h1>
    <p class="text-center">{{dreamvention.partners}}</p>
    <div class="container">
        <div class="row">
            <div class="col-sm-12 col-xs-12">
                <div class="text-center">
                    <img src="~assets/dreamvention.png"/>
                </div>
                <div class="text-center dreamvention-text">
                    <span>
                        {{dreamvention.text}}
                    </span>
                </div>
                <div class="text-center">
                    <img src="~assets/opencart-puzzle.png"/>
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
            dreamvention: null
        };

    },
    async mounted(){
        const main = await this.$content('main').fetch();
        this.dreamvention = main.dreamvention
    }
  }

</script>