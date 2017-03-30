<template>
    <div>
        <div class="parallax-container">
            <div class="parallax">
                <img class="parallax-bg" src="http://img08.deviantart.net/fb9b/i/2015/182/c/a/fallout_4___vault_111_wallpaper_by_grindone-d8zheki.jpg">
            </div>
        </div>
        <div class="section blue darken-3 center yellow-text">
            <div class="row container">
                <h3 class="header">The things you love will survive the apocalypse, even if you don't!</h3>
                <div class="col s12 m4">
                    <h5><i class="fa fa-bolt"></i> Create Keeps</h5>
                    <p>Immortalize the things you love in keeps and store them safely away in different vaults.</p>
                </div>
                <div class="col s12 m4">
                    <h5><i class="fa fa-cog"></i> Store in Vaults</h5>
                    <p>Our vaults are built to withstand the most powerful atomic blasts, and definitely aren't covers for screwed up experiments.</p>
                </div>
                <div class="col s12 m4">
                    <h5><i class="fa fa-thumbs-up"></i> Prepared for the Future</h5>
                    <p>Vault-Tec is here for you. Revolutionizing safety for an uncertain future.</p>
                </div>
            </div>
        </div>
        <div class="parallax-container">
            <div class="parallax">
                <img class="parallax-bg" src="https://i.ytimg.com/vi/axy4ZakRqPw/maxresdefault.jpg">
            </div>
            <div class="center">
                <router-link to="/register" class="sign-up waves-effect waves-indigo btn btn-large blue darken-2 hoverable raised">Sign Up Today</router-link>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'landing-page',
        mounted: function () {
            $('.parallax').parallax();
        }
    }

</script>

<style>
    .parallax-container {
        height: 500px;
    }
    
    .sign-up {
        margin-top: 70px;
    }
    
    .parallax-bg {
        width: 100%;
    }
    /*.parallax {
        background-image: url("https://cdn0.vox-cdn.com/uploads/chorus_image/image/53522233/Nintendo_Switch_2.0.0.jpg");
        min-width: 100%;
        background-attachment: fixed;
        background-position: center;
        background-repeat: no-repeat;
        background-size: cover;
    }
    
    .bgimg-2 {
        background-image: url("http://unsplash.com/photos/CuFYW1c97w8/download?force=true");
        min-height: 100%;
        background-attachment: fixed;
        background-position: center;
        background-repeat: no-repeat;
        background-size: cover;
    }*/
    
    .section {
        padding-top: 20px;
        padding-bottom: 20px;
        color: white;
    }
    
    hr {
        margin-top: 5px;
        margin-bottom: 5px;
    }
</style>