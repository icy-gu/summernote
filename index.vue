<template>
    <div :id="id"></div>
</template>

<script>
export default {
    name: 'app',
     data(){
        return {
        }
    },
    components: {
    },
    props:{
        id:{
            type:String,
            default:'summernote'
        },
        placeholder:{
            type:String,
            default:'请输入'
        }
    },
    mounted:function () {
        this.initSummernote()
    },
    methods:{
       initSummernote(){
           document.emojiSource = 'static/public/images/tam-emoji/img'
           $('#' + this.id).summernote({
                lang: 'zh-CN',
                placeholder: this.placeholder,
                height: 200,
                width: 380,
                htmlMode: true,
                toolbar: [
                    ['insert', ['emoji','picture']],
                ],
            })
       },
       /**
        * @methods  获取值
        */
       getContent(){
           return $('#' + this.id).summernote('code') 
       },
       /**
        * @method   赋值
        */
       setContent(data){
           $('#' + this.id).summernote('code' , data) 
       },
    },
}
</script>

<style lang="scss">
#app {
    
}

</style>
