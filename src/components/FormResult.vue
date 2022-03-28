<template>
    <div class="form-root">
        {{message}}
        <div class="result-box">
            <p class="result-title">Here you Advice</p>
            <p class="result-text"
            :style="{color:color}"
            >{{advice}}</p>
        </div>
    </div>
</template>

<script>
export default {
    name:'FormResult',
    props:['advice','color'],
    inject: ['quotes','message'],
}
</script>

<style scoped>
 .result-box{
    margin: 12px 0;
    padding: 15px;
    border-radius: 12px;
    color: aliceblue;
    background: #0a0a77;
 }
 .result-title{
     font-size: 24px;
     font-weight: bold;
 }
 .result-text{
    font-size: 18px;
 }
</style>