<template>
    <div id="head-nav">
        <mt-header :title="title">
            <router-link to="/" slot="left">
                <mt-button icon="back" @click="goBack">返回</mt-button>
            </router-link>
            <mt-button icon="more" slot="right"></mt-button>
        </mt-header>
        <!-- <header>
            <a href="javascript:;" class="iconfont icon-fanhui2" @click="goBack">
                返回
            </a>
            <span>{{title}}</span>
            <a href="javascript:;" class="iconfont icon-diandian"></a>
        </header> -->
        <!--
            <mt-header >
                <router-link to="/" slot="left">
                    <mt-button icon="back">返回</mt-button>
                    {{title}}
                </router-link>

                <mt-button icon="more" slot="right"></mt-button>
            </mt-header>
        -->
    </div>
</template>

<script>
    export default {
        data() {
            return {
                title:''
            }
        },
        props:['title'], // 接收来自父级的参数
        created(){
            this.$axios.get('',{params:{
                title:'vueTitle'
            }}).then((res) => {
                if(res.statusText='OK'){
                    this.title=res.data
                }
            })
        },
        methods:{
            goBack(){

            }
        }
    }
</script>

<style scoped lang="less">
    
</style>
