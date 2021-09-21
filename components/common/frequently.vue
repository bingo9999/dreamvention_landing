<template>
    <div v-if="frequently" id="frequently">
        <h1 class="text-center">{{frequently.Frequently}}</h1>
        <div class="container">
            <div class="row">
                <div class="col-md-6 col-xs-12 centered-block">
                    <div class="row">
                        <div class="col-md-10">
                            <p class="frequently-question">{{frequently.QuestWhy}}</p>
                            <span class="frequently-answer">
                                {{frequently.Answerbig}}
                            </span>
                        </div>
                    </div>
                </div>
                <div class="col-md-6 col-xs-12 centered-block">
                    <div class="row">
                        <div class="col-md-10">
                            <p class="frequently-question">{{frequently.QuestHowBugs}}</p>
                            <span class="frequently-answer">
                                {{frequently.Answerlittle}}
                            </span>
                        </div>
                    </div>
                </div>
            </div>
            <div class="row">
                <div class="col-md-6 col-xs-12 centered-block">
                    <div class="row">
                        <div class="col-md-10">
                            <p class="frequently-question">{{frequently.QuestHowaProvide}}</p>
                            <span class="frequently-answer">
                                {{frequently.Answerlittle}}
                            </span>
                        </div>
                    </div>
                </div>
                <div class="col-md-6 col-xs-12 centered-block">
                    <div class="row">
                        <div class="col-md-10">
                            <p class="frequently-question">{{frequently.QuestLorem}}</p>
                            <span class="frequently-answer">
                                {{frequently.Answerbig}}
                            </span>
                        </div>
                    </div>
                </div>
            </div>
            <div class="row">
                <div class="col-md-6 col-xs-12 centered-block">
                    <div class="row">
                        <div class="col-md-10">
                            <p class="frequently-question">{{frequently.QuestWhy}}</p>
                            <span class="frequently-answer">
                                {{frequently.Answerlittle}}
                            </span>
                        </div>
                    </div>
                </div>
                <div class="col-md-6 col-xs-12 centered-block">
                    <div class="row">
                        <div class="col-md-10">
                            <p class="frequently-question">{{frequently.QuestWhy}}</p>
                            <span class="frequently-answer">
                                {{frequently.Answerlittle}}
                            </span>
                        </div>
                    </div>
                </div>
            </div>
            <div class="row">
                <div class="col-md-6 col-xs-12 centered-block">
                    <div class="row">
                        <div class="col-md-10">
                            <p class="frequently-question">{{frequently.QuestLorem}}</p>
                            <span class="frequently-answer">
                                {{frequently.Answerbig}}
                            </span>
                        </div>
                    </div>
                </div>
                <div class="col-md-6 col-xs-12 centered-block">
                    <div class="row">
                        <div class="col-md-10">
                            <p class="frequently-question">{{frequently.QuestLorem}}</p>
                            <span class="frequently-answer">
                                {{frequently.Answerlittle}}
                            </span>
                        </div>
                    </div>
                </div>
            </div>
            <div class="row">
                <div class="col-md-6 col-xs-12 centered-block">
                    <div class="row">
                        <div class="col-md-10">
                            <p class="frequently-question">{{frequently.QuestWhy}}</p>
                            <span class="frequently-answer">
                                {{frequently.Answerbig}}
                            </span>
                        </div>
                    </div>
                </div>
                <div class="col-md-6 col-xs-12 centered-block">
                    <div class="row">
                        <div class="col-md-10">
                            <p class="frequently-question">{{frequently.QuestLorem}}</p>
                            <span class="frequently-answer">
                                {{frequently.Answerlittle}}
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
            frequently: null
        };

    },
    async mounted(){
        const main = await this.$content('main').fetch();
        this.frequently = main.frequently
    }
  }

</script>