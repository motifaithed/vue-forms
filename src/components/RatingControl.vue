<template>
    <ul>
        <li :class="{active: selectOption === 'poor'}"><button type="button" @click="setOption('poor')">Poor</button></li>
        <li :class="{active: selectOption === 'average'}"><button type="button" @click="setOption('average')">Average</button></li>
        <li :class="{active: selectOption === 'great'}"><button type="button" @click="setOption('great')">Great</button></li>
    </ul>
</template>
<script>
    export default{
        data(){
            return{
                selectOption: null
            }
        },
        methods:{
            setOption(option){
                this.selectOption = option
            }
        }
    }
</script>
<style scoped>
    .active{
        border-color: #a00078;
    }

    .active button {
        color: #a00078;
    }

    ul{
        list-style: none;
        margin: 0.5rem 0;
        padding: 0;
        display: flex;
    }

    li{
        margin: 0 1 rem;
        border: 1px solid #ccc;
        padding: 1rem;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    button{
        font: inherit;
        border: none;
        background-color: transparent;
        cursor: pointer;
    }
</style>