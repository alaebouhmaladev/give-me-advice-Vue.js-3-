<template>
    <div class="root">
        <div class="logo">
            <img :src="image" alt="">
            <div class="image-title">{{title}}</div>
        </div>
        <div class="menu">
            <a href="#" class="page-link-menu">Home</a>
            <a href="#" class="page-link-menu">Works</a>
            <a href="#" class="page-link-menu">About us</a>
            <a href="#" class="page-link-menu">Contact us</a>
        </div>
        <div class="account">
            <div class="login">
                <p>login</p>
            </div>
            <div class="singup">
                <p>singup</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'HeaderPage',
    props:['title','image'],
    }

</script>

<style lang="css" scoped>
    .root{
        width: 100%;
        display: inline-flex;
        justify-content: space-around;
        background: rgba(206, 206, 206, 0.842);
    }
    .logo,.menu{
        display: inline-flex;
        justify-content: space-evenly;
        width: 40%;
    }
    .account{
        display: inline-flex;
        justify-content: space-evenly;
        width: 18%;
    }
    .image-title,.login p,.singup p{
        padding: 6px 12px;
        margin: 0px 6px;
        text-decoration: none;
        color: #2c3e50;
        font-size: 16px;
        font-weight: 600;
    }
    .page-link-menu {
        padding: 8px 20px;
        margin: 0px 6px;
        text-decoration: none;
        color: #2c3e50;
        font-size: 16px;
        font-weight: 600;
        border: 1px solid #fff;
        border-radius: 12px;
        transition: border 0.6 ease-in-out;
    }

    .page-link-menu:hover{
        border: 1px solid #2c3e50;
    }
    

</style>