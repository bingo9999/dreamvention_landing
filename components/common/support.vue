<template>
    <div v-if="support" id="support-features">
        <h1 class="text-center">{{support.features}}</h1>
        <div class="container">
            <div class="row">
                <div class="col-md-6 col-xs-12 centered-block">
                    <div class="row">
                        <div class="col-md-2 text-center">
                            <img src="~assets/features/gear.svg"/>
                        </div>
                        <div class="col-md-10">
                            <p>{{support.DebuggingFixing}}</p>
                            <span>
                                {{support.ThorougVerification}}
                            </span>
                        </div>
                    </div>
                </div>
                <div class="col-md-6 col-xs-12 centered-block">
                    <div class="row">
                        <div class="col-md-2 text-center">
                            <img src="~assets/features/website.svg"/>
                        </div>
                        <div class="col-md-10">
                            <p>{{support.WebDev}}</p>
                            <span>
                                {{support.WeAreReady}}
                            </span>
                        </div>
                    </div>
                </div>
            </div>
            <div class="row">
                <div class="col-md-6 col-xs-12 centered-block">
                    <div class="row">
                        <div class="col-md-2 text-center">
                            <img src="~assets/features/cloud.svg"/>
                        </div>
                        <div class="col-md-10">
                            <p>{{support.ConsulAssist}}</p>
                            <span>
                                {{support.WeHappy}}
                            </span>
                        </div>
                    </div>
                </div>
                <div class="col-md-6 col-xs-12 centered-block">
                    <div class="row">
                        <div class="col-md-2 text-center">
                            <img src="~assets/features/puzzle.svg"/>
                        </div>
                        <div class="col-md-10">
                            <p>{{support.ModDesDev}}</p>
                            <span>
                                {{support.WeHappy}}
                            </span>
                        </div>
                    </div>
                </div>
            </div>
            <div class="row">
                <div class="col-md-6 col-xs-12 centered-block">
                    <div class="row">
                        <div class="col-md-2 text-center">
                            <img src="~assets/features/upgrade.svg"/>
                        </div>
                        <div class="col-md-10">
                            <p>{{support.OpenUpgrad}}</p>
                            <span>
                                {{support.WeProvideUp}}
                            </span>
                        </div>
                    </div>
                </div>
                <div class="col-md-6 col-xs-12 centered-block">
                    <div class="row">
                        <div class="col-md-2 text-center">
                            <img src="~assets/features/fulltime.svg"/>
                        </div>
                        <div class="col-md-10">
                            <p>{{support.WeAreAlways}}</p>
                            <span>
                                {{support.AnythingCanHap}}
                            </span>
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
            support: null
        };

    },
    async mounted(){
        const main = await this.$content('main').fetch();
        this.support = main.support
    }
  }

</script>