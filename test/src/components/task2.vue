<template>
    <div class="task2 task">
        <h2>Task 2</h2>
        <div class="detail">
            <p>设计一个任务队列，实现1s、3s、4s后打印" 1 "、" 2 "、" 3 "</p>
            <br>
            <p>{{ arr }}</p>
            <div>第 {{ t2time }} 秒</div>
            <div class="btn" @click='t2'>测试</div>
            <div class="btnstop" @click='t2stop'>停止</div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'task2',
        data(){
            return {
                t2timer: '',
                t2time: 0,
                arr: []
            }
        },
        methods: {
            t2stop(){
                // console.log(this.t2timer)
                let a = clearInterval(this.t2timer);
                this.arr = []
                console.log('t2 stop');
            },
            t2(){
                let i = 1;
                this.t2timer = setInterval(e=>{
                    this.t2time = i++;
                },1000)
                this.Queue();
            },
            Queue(){
                setTimeout(e=>{
                    console.log(' 1 ');
                    this.arr.push(' 1 ')
                },1000,
                
                    setTimeout(e=>{
                        console.log(' 2 ');
                        this.arr.push(' 2 ')
                    },3000,
                        
                        setTimeout(e=>{
                            console.log(' 3 ');
                            this.arr.push(' 3 ')
                        },4000)
                    )
                )
            }
        },
        mounted(){
            
        }
    }
</script>

<style>
    .btnstop {
        width: 100px;
        height: 40px;
        background-color: rgb(255, 51, 91);
        line-height: 40px;
        text-align: center;
        color: #fafafa;
        cursor: pointer;
        display: inline-block;
    }
</style>