<template>
    <footer v-if="footer">
        <div class="container">
            <div class="row">
                <div class="col-sm-2">
                    <section>
                        <h5>{{footer.Op}}</h5>
                        <ul class="list-unstyled">
                        <li><a href="https://www.opencart.com/index.php?route=cms/feature">{{footer.Features}}</a></li>
                        <li><a href="https://www.opencart.com/index.php?route=cms/showcase">{{footer.Showcase}}</a></li>
                        <li><a href="https://www.opencart.com/index.php?route=cms/demo">{{footer.Demo}}</a></li>
                        <li><a href="https://www.opencart.com/index.php?route=cms/download">{{footer.Dwnld}}</a></li>
                        <li><a href="https://www.opencart.com/index.php?route=marketplace/extension">{{footer.MarkPlace}}</a></li>
                        <li><a href="https://www.opencart.com/index.php?route=account/login">{{footer.Login}}</a></li>
                        </ul>
                    </section>
                </div>
                <div class="col-sm-2">
                    <section>
                        <h5>{{footer.Company}}</h5>
                        <ul class="list-unstyled">
                        <li><a href="https://www.opencart.com/index.php?route=footer/contact">{{footer.ConUs}}</a></li>
                        <li><a href="https://www.opencart.com/index.php?route=cms/company">{{footer.AbUs}}</a></li>
                        <li><a href="https://www.opencart.com/index.php?route=cms/information&amp;information_id=2">{{footer.ExtDev}}</a></li>
                        </ul>
                    </section>
                </div>
                <div class="col-sm-2">
                    <section>
                        <h5>{{footer.Support}}</h5>
                        <ul class="list-unstyled">
                        <li><a href="https://forum.opencart.com">{{footer.CForum}}</a></li>
                        <li><a href="https://dedicated.opencart.com">{{footer.Dfooter}}</a></li>
                        <li><a href="https://www.opencart.com/index.php?route=footer/partner">{{footer.OCPartners}}</a></li>
                        <li><a href="https://www.opencart.com/index.php?route=footer/footer">{{footer.MPlacefooter}}</a></li>
                        <li><a href="https://www.opencart.com/index.php?route=cms/cart2cart">{{footer.MTOCart}}</a></li>
                        </ul>
                    </section>
                </div>
                <div class="col-sm-2">
                    <section>
                        <h5>{{footer.Resources}}</h5>
                        <ul class="list-unstyled">
                        <li><a href="https://www.opencart.com/blog">{{footer.OpenCartBlog}}</a></li>
                        <li><a href="http://docs.opencart.com">{{footer.OCDoc}}</a></li>
                        <li><a href="http://docs.opencart.com/#additional-reading">{{footer.OCBooks}}</a></li>
                        <li><a href="https://github.com/opencart/opencart/issues">{{footer.GBTracker}}</a></li>
                        <li><a href="http://docs.opencart.com/developer/module/">{{footer.Dev}}</a></li>
                        </ul>
                    </section>
                </div>
                <div class="col-sm-2 col-md-4">
                    <section id="newsletter">
                        <h5 class="newsletter">{{footer.Newlet}}</h5>
                        <p class="newsletter">{{footer.Subscribe}}</p>
                        <div class="input-group newsletter">
                            <input type="text" name="newsletter" value="" :placeholder="footer.PlachdEnterY" class="form-control">
                            <div class="input-group-btn">
                                <button type="button" class="btn btn-primary subscribe"><i class="fa fa-angle-right"></i></button>
                            </div>
                        </div>
                    </section>
                </div>
            </div>
            <div class="row">
                <div class="col-sm-6 col-md-6">
                    <div id="copyright">
                        <ul class="list-unstyled">
                            <li class="company-logo"><img src="~assets/opencart/opencart-logo-white.png" :alt="footer.Op" :title="footer.Op" /></li>
                            <li class="copyright-text"> {{footer.Cr}}</li>
                        </ul>
                    </div>
                </div>
                <div class="col-sm-6 col-md-6">
                    <div id="social">
                        <ul class="list-unstyled">
                        <li class="facebook-marketing-partner-logo"><a href="https://www.facebook.com/fmp/commerce/partner-badge" target="_blank"><img src="~assets/opencart/facebook_marketing_partner.png" :alt="footer.FaMaPart" :title="footer.FaMaPart" style="width: 100px; height: 40px;"  /></a></li>
                        <li><a href="https://www.linkedin.com/company/5224021/" target="_blank">{{footer.Li}}</a></li>
                        <li><a href="https://www.facebook.com/opencart/?ref=aymt_homepage_panel" target="_blank">{{footer.Fb}}</a></li>
                        <li><a href="https://twitter.com/opencart" target="_blank">{{footer.Tw}}</a></li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>


<script>

  export default {
    data(){
        return {
            footer: null
        };

    },
    async mounted(){
        const main = await this.$content('footer').fetch();
        this.footer = main.footer
    }
  }

</script>