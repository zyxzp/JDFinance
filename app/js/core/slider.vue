<template lang="html">
    <section :class="cname">
        <swiper :options="options" :not-next-tick="options.notNextTick">
            <swiper-slide v-for="item in items" :key="item.href">
                <router-link :to="{name:item.href}">
                   <img :src="item.src" alt="">
                </router-link>
            </swiper-slide>
            <div class="swiper-pagination" v-if="options.pagination" slot="pagination"></div>
        </swiper>
    </section>
</template>

<script>
import {swiper,swiperSlide} from "vue-awesome-swiper"
    export default {
         props:{
            cname:{
                type:String,
                default:''
            },
            items:{
                type:Array,
                default:[]
            },
            options:{
                type:Object,
                default(){
                    return {
                        autoplay:true,
                        loop:true,
                        pagination: {
                            el: '.swiper-pagination',
                        },
                        notNextTick:false
                    }
                }
            }
        },
        components:{
           swiper,
           swiperSlide 
        }
    }
</script>

<style scoped>

</style>