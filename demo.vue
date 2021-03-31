<template>
    <div class="demo">
        <div>
            <summer-note id="summerNote" ref="summerNote"></summer-note>
        </div>
        <div>
            <summer-note id="summerNote2" ref="summerNote2"></summer-note>
        </div>
        <div @click="getContent">ssss</div>
    </div>
</template>
<script>
import summerNote from './index.vue'
export default {
    components:{
        summerNote
    },
    data(){
        return{}
    },
    mounted(){
    },
    methods:{
        /**
         * @method  获取值
         */
        getContent(){
            console.log( this.$refs.summerNote.getContent() )
            console.log( this.$refs.summerNote2.getContent() )
        },
        /**
         * @method  设置值
         */
        setContent(){
            this.$summerNote.setContent('sssss')
        },
    }
}
</script>