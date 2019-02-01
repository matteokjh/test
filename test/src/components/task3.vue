<template>
    <div class="task3 task">
        <h2>Task 3</h2>
        <div class="detail">
            <p>给定一个升序序列，求它们的连续区间</p>
            <br>
            <p>Array: {{ arr }}</p>
            <br>
            <p>newArray => {{ arr2 }}</p>
            <div class="btn" @click='t3'>测试</div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'task3',
        data(){
            return {
                arr: [
                    0,1,2,4,5,7,13,15,16
                ],
                arr2: [],
                starter: ''
            }
        },
        methods: {
            t3(){
                this.arr2 = []
                let arr = this.arr
                arr.forEach( (e, idx)=>{
                    if(arr[idx + 1] - 1 === e){
                        if(this.starter === ''){
                            this.starter = e;
                        }
                    }else {
                        this.end = arr[idx];
                        if(this.starter !== ''){
                            this.arr2.push(`${this.starter}->${this.end}`)
                            this.starter = '';
                        }else {
                            this.arr2.push(`${this.end}`)
                        }
                    }
                })
                console.log(this.arr2)
            }
        },
        mounted(){
            
        }
    }
</script>

<style>

</style>