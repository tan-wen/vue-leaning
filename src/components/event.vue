<template>
    <div @click="handleAdd(2)">
        点击次数：{{ counter }}
        <button @click.stop="handleAdd()"> + 1</button>
        <button @click="handleAdd(10)"> + 10</button>
    </div>
</template>

<script>
export default {
    name: 'Event',
    desc: '5.4方法与事件',
    data(){
        return {counter : 0}
    },
    methods:{
        handleAdd: function(count){
            count = count || 1;
            this.counter += count;
        }
    }
}
</script>