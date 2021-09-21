<template>
    <header>
            <nav v-if="header" class="navbar navbar-default navbar-fixed-top">
                <div class="container">
                    <div class="navbar-header">
                        <button type="button" data-toggle="collapse" data-target="#navbar-collapse-header" class="navbar-toggle collapsed"><span class="icon-bar"></span> <span class="icon-bar"></span> <span class="icon-bar"></span></button>
                        <a href="https://www.opencart.com/index.php?route=common/home" class="navbar-brand"><img src="~assets/opencart-logo.png" :title="header.opencartlogotitle" alt=""></a>
                    </div>
                    <div class="collapse navbar-collapse" id="navbar-collapse-header">
                            <ul class="nav navbar-nav">
                                <li><a href="https://www.opencart.com/index.php?route=cms/feature">{{header.Features}}</a></li>
                                <li><a href="https://www.opencart.com/index.php?route=cms/demo">{{header.Demo}}</a></li>
                                <li><a href="https://www.opencart.com/index.php?route=marketplace/extension">{{header.Marketplace}}</a></li>
                                <li><a href="https://www.opencart.com/blog">{{header.Blog}}</a></li>
                                <li><a href="https://www.opencart.com/index.php?route=cms/download">{{header.Download}}</a></li>
                                <li class="dropdown"><a href="#" data-toggle="dropdown">{{header.Resources}} <span class="caret"></span></a>
                            <ul class="dropdown-menu">
                                <li><a href="https://www.opencart.com/index.php?route=cms/showcase">{{header.Showcase}}</a></li>
                                <li><a href="https://www.opencart.com/index.php?route=support/contact">{{header.ContactUs}}</a></li>
                                <li><a href="https://www.opencart.com/index.php?route=cloud/landing">{{header.OpenCartCloud}}</a></li>
                                <li><a href="https://www.opencart.com/index.php?route=support/partner">{{header.OpenCartPartners}}</a></li>
                                <li><a href="https://forum.opencart.com">{{header.CommunityForums}}</a></li>
                                <li><a href="http://docs.opencart.com">{{header.OpenCartDocumentation}}</a></li>
                                <li><a href="http://docs.opencart.com/#additional-reading">{{header.OpenCartBooks}}</a></li>
                                <li><a href="https://github.com/opencart/opencart/issues">{{header.GithubBugTracker}}</a></li>
                                <li><a href="http://docs.opencart.com/developer/module/">{{header.Developer}}</a></li>
                            </ul>
                            </li>
                                <li class="visible-xs"><a href="https://www.opencart.com/index.php?route=account/login">{{header.Login}}</a></li>
                                <li class="visible-xs"><a href="https://www.opencart.com/index.php?route=account/register">{{header.Register}}</a></li>
                            </ul>
                        <div class="navbar-right hidden-xs">
                            <a href="https://www.opencart.com/index.php?route=account/login" class="btn btn-link navbar-btn">{{header.Login}}</a> 
                            <a href="https://www.opencart.com/index.php?route=account/register" class="btn btn-black navbar-btn">{{header.Register}}</a>
                        </div>
                    </div>
                        
                </div>
            </nav>
            <div v-else>Loading...</div>
        </header>
</template>

<script>

  export default {
    data(){
        return {
            header: null
        };

    },
    async mounted(){
        const header = await this.$content('header').fetch();
        this.header = header.header
    }
  }

</script>