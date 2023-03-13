<template>
    <div>hello test2</div>
    <ul>
        <li v-for="(item, index) in testArr" :key="index"> 
        <!-- in 要素の数 -->
        {{item}}
        <span v-if="`${item}`=== 'C'">これはCです</span>
        </li>
        <div>{{add}}</div>
    </ul>
    <!-- <div v-text="text"></div> -->
        <!-- <div v-text="`${text}`"></div> -->
</template>
<script>
export default {
    data(){
        return{
            testArr:  ["A","B","C"],
            text: "あ",
            num1: 1,
            num2: 3
        }
    },
    computed:{
        add(){
            return this.num1 + this.num2
            // computedでdataから変数を使う時はthiss
        }
    }
}
</script>