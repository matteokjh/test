<template>
    <div class="task1 task">
        <h2>Task 1</h2>
        <div class="detail">
            <div class="in">
                <h3>输入</h3>
                <input type="text" v-model='input1' spellcheck='false'>
                <input type="text" v-model='input2' spellcheck='false'>
            </div>
            <div class="out">
                <h3>输出</h3>
                <p class='output'>{{input1}} + {{input2}} = {{ output }}</p>
            </div>
            <div class="btn" @click='caculate'>测试</div>
        </div>
    </div>
</template>

<style>
* {

}
input { 
    height: 3vh;
}
.task {
    padding: 0 5vw;
    min-height: 30vh;
}
.detail {
    margin: 30px 0;
}
.detail > div {
    margin: 3vh 0; 
}
h3 {
    margin: 2vh 0;
}
.output {
    background-color: #fafafa;
    width: 300px;
    padding: 30px;
    border-radius: 5px;
    overflow: auto;
}
.btn {
    width: 100px;
    height: 40px;
    background-color: rgb(51,133,255);
    line-height: 40px;
    text-align: center;
    color: #fafafa;
    cursor: pointer;
    display: inline-block;
}
</style>

<script>
export default {
    data() {
        return {
            output: '2',
            input1: '1',
            input2: '1'
        }
    },
    methods: {
        caculate(){
            this.output = parseInt(this.input1) + parseInt(this.input2)
        }
    }
}
</script>