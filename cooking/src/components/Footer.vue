<template>
    <div class="footer">
        <div class="container">
            <div class="row">
                <div class="col-md-6">
                    <router-link class="home-logo" to="/">Recipe!</router-link>
                </div>

                <div class="col-md-6 list text-right">
                    <ul>
                        <li><router-link to="" class="lst_link">Terms</router-link></li>
                        <li><router-link to="" class="lst_link">Blog</router-link></li>
                        <li><router-link to="" class="lst_link">About</router-link></li>
                        <li><router-link to="" class="lst_link">FAQ</router-link></li>
                        <li><router-link to="" class="lst_link">Contact</router-link></li>
                    </ul>
                </div>
            </div>
            <hr>
            <div class="row">
                <div class="col-md-6">
                    <span>&copy;2021 Sam's Recipe App. All rights reserved.</span>
                </div>

                <div class="col-md-6 social text-right">
                    <ul>
                        <li><router-link to="" class="social_link"><i class="fab fa-facebook-square"></i></router-link></li>
                        <li><router-link to="" class="social_link"><i class="fab fa-instagram-square"></i></router-link></li>
                        <li><router-link to="" class="social_link"><i class="fab fa-linkedin"></i></router-link></li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Footer'
}
</script>

<style scoped>
.footer{
    background-color: #343a40;
    color: #ffffff;
    padding: 10px 0;
}

.footer .home-logo{
    color: #c74e61;
    font-size: 30px;
    font-weight: bold;
    font-family: cursive;
    text-decoration: none;
    padding-right: 20px;
}

.footer .home-logo:hover{
    color: #c74e61;
}

.footer .list ul{
    list-style-type: none;
    padding-top: 12px;
}

.footer .list ul li{
    display: inline-block;
    padding: 0 15px;
}

.footer .list ul li .lst_link{
    color: #ffffff;
}

.footer .social ul{
    list-style-type: none;
}

.footer .social ul li{
    display: inline-block;
}

.footer .social ul li i{
    color: #ffffff;
    padding: 0 20px;
    font-size: 25px;
}
</style>
