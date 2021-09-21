<template>
    <div v-if="reviews" id="reviews">
        <h1 class="text-center">{{reviews.centertext}} <br/> {{reviews.centertext2}}</h1>
        <div class="col-xs-4 col-md-12">
            <div class="row">
                <div class="review-block review-transform-1 review-margin-center col-md-2 text-center">
                    <div class="review-col review-padding-1 ">
                        <img src="~assets/avatar-13.png"/>
                        <p class="review-text">{{reviews.reviewtextlong}}</p>
                        <div>
                            <p class="review-name">{{reviews.nameMorris}}</p>
                            <p class="review-text">{{reviews.coowner}}</p>
                        </div>
                    </div>
                </div> 
                <div class="review-block review-transform-2 review-position-left col-md-2 text-center">
                    <div class="review-col">
                        <img src="~assets/avatar-10.png"/>
                        <p class="review-text">{{reviews.reviewtext}}</p>
                        <div>
                            <p class="review-name">{{reviews.nameMichael}}</p>
                            <p class="review-text">{{reviews.coowner}}</p>
                        </div>
                    </div>
                </div>
                <div class="review-block review-transform-1 review-margin-bottom col-md-2 text-center">
                    <div class="review-col">
                        <img src="~assets/avatar-11.png"/>
                        <p class="review-text">{{reviews.reviewtext}}</p>
                        <div>
                            <p class="review-name">{{reviews.nameMichael}}</p>
                            <p class="review-text">{{reviews.coowner}}</p>
                        </div>
                    </div>
                </div>
                <div class="review-block review-transform-2 review-margin-center col-md-2 text-center">
                    <div class="review-col review-padding-1">
                    <img src="~assets/avatar-14.png"/>
                        <p class="review-text">{{reviews.reviewtextlong}}</p>
                        <div>
                            <p class="review-name">{{reviews.nameMorris}}</p>
                            <p class="review-text">{{reviews.coowner}}</p>
                        </div>
                    </div>
                </div>
                <div class="review-block review-transform-1 review-position-right col-md-2 text-center">
                    <div class="review-col">
                        <img src="~assets/avatar-15.png"/>
                        <p class="review-text">{{reviews.reviewtext}}</p>
                        <div>
                            <p class="review-name">{{reviews.nameMichael}}</p>
                            <p class="review-text">{{reviews.coowner}}</p>
                        </div>
                    </div>
                </div>
                <div class="review-block review-transform-2 review-margin-bottom col-md-2 text-center">
                    <div class="review-col">
                    <img src="~assets/avatar-12.png"/>
                        <p class="review-text">{{reviews.reviewtext}}</p>
                        <div>
                            <p class="review-name">{{reviews.nameKaren}}</p>
                            <p class="review-text">{{reviews.coowner}}</p>
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
            reviews: null
        };

    },
    async mounted(){
        const main = await this.$content('main').fetch();
        this.reviews = main.reviews
    }
  }

</script>