<template>
    <div>
        <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
            <router-link class="navbar-brand" to="/">Recipe!</router-link>
            <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
            </button>
        
            <div class="collapse navbar-collapse" id="navbarSupportedContent">
                <ul class="navbar-nav mr-auto">
                    <li class="nav-item active">
                        <router-link to="/breakfast-recipe" class="nv-link">BreakFast Recipe</router-link>
                    </li>
                    <li class="nav-item">
                        <router-link to="/lunch-recipe" class="nv-link">Lunch Recipe</router-link>
                    </li>
                    <li class="nav-item">
                        <router-link to="/dinner-recipe" class="nv-link">Dinner Recipe</router-link>
                    </li>
                </ul>
                <div class="registration mr-5">
                    <!-- <span class="mr-3" style="color: #fff;">Welcome</span>
                    <a href="" class="mr-3 profile">Profile</a>
                    <a href="" class="mr-5 profile">Add Recipe</a>
                    <a href="" class="btn btn-danger">Logout</a> -->
                    <router-link to="/login" class="btn btn-success mr-2">Login</router-link>
                    <router-link to="/register" class="btn btn-success">Register</router-link>
                </div>
            </div>
        </nav>
    </div>
</template>

<script>
export default {
    name: 'Header',
}
</script>

<style scoped>
.bg-dark {
    background-color: #343a40!important;
    padding: 12px 100px;
}

.navbar-dark .navbar-brand{
    color: #c74e61;
    font-size: 30px;
    font-weight: bold;
    font-family: cursive;
    padding-right: 20px;
}

.navbar-dark .navbar-brand:hover{
    color: #c74e61;
}

.navbar .nv-link{
    color: #ffffff;
    padding-right: 20px;
    font-size: 16px;
}

.navbar .navbar-nav{
    padding-top: 8px;
}
</style>