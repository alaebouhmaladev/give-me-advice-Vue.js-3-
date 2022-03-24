<template>
    <div class="root">
        <h1>From Page</h1>
        <form class="form">
            <fieldset class="form-fieldset">
                <legend class="form-legend">
                    Choose a number
                </legend>
                <label class="form-label">Luck Number</label>
                <input type="number" class="form-input" v-model="UserNumber"/> 
            </fieldset>
            <fieldset class="form-fieldset">
                <legend class="form-legend">
                    Color
                </legend>
                <label class="form-label">Color</label>
                <input type="color" class="form-input" v-model="UserColor"/> 
            </fieldset>
            <form-result></form-result>
            <div class="data">
                <span>{{UserNumber}}</span>
                <span>{{UserColor}}</span>
                <span>{{getAdvice}}</span>
            </div>
        </form>
    </div>
</template>

<script>
import FormResult from './FormResult.vue';
export default {
  components: { FormResult },
    name:'FormPage',
    data() {
        return {
            UserNumber: 0,
            UserColor:'#ffffff',
            quotes:['quotes 1','quotes 2','quotes 3','quotes 4','quotes 5','quotes 6'],
        }
    },
    computed:{
        getAdvice(){
            const Advice = this.quotes.find(
                (q,i) => i == this.UserNumber
            );
            console.log(Advice);
            if(!Advice){
                return 'unlucky enough, no quotes for you';
            }else{
                return Advice;
            }
        },
    }
}
</script>

<style lang="css" scoped>
    .form{
        margin: 20px auto;
        max-width: 70%;
    }
    .form-fieldset{
        margin: 12px 0;
        padding: 15px;
        border-radius: 12px;
        color: aliceblue;
        background: #0a0a77;
    }
    .form-legend{
        background: #0a0a77;
        padding: 12px 20px;
        border-radius: 12px;
    }
    .form-label{
        display: block;
        padding: 15px;
        font-size: 24px;
        font-weight: bold;
    }
    .form-input{
        outline: none;
        border: none;
        font-size: 24;
        color: tomato;
        text-align: center;
        max-width: 40%;
        height: 30px;
    }
    .data span {
        padding: 8px 15px;
        margin: 0px 10px;
        background: #2c3e50;
        color: #fff;
        border-radius: 4px;
        font-size:20px;
    }
</style>