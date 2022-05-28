<template>
    <div>
        <header>
            <h1>我是傻逼</h1>
        </header>
    </div>
    <!-- 大容器 -->
    <section class="container">
        <!-- 左容器 -->
        <section class="itemLeft">
            <ItemPage>
                <ItemOne/>
            </ItemPage>
            <ItemPage>
                <ItemTwo/>
            </ItemPage>
        </section>
        <!-- 中容器 -->
        <section class="itemConter">
                哈哈哈
        </section>
        <!-- 右容器 -->
        <section class="itemRight">
            <ItemPage>
                <ItemThree/>
            </ItemPage>
            <ItemPage>
                <ItemFour/>
            </ItemPage>
        </section>

    </section>
</template>

<script>
import ItemPage from "@/components/itemPage.vue"
import ItemOne from "@/components/itemOne.vue"
import ItemTwo from "@/components/itemTwo.vue"
import ItemThree from "@/components/itemThree.vue"
import ItemFour from "@/components/itemFour.vue"

import {inject} from "vue"
export default {
    components:{
        ItemPage,ItemOne,ItemTwo,ItemThree,ItemFour
    },

    setup(){
        let $echarts=inject("echarts")
        let $http = inject("axios")
    }
};
</script>

<style lang="less">
header {
    height: 1rem;
    width: 100%;
    background-color: rgba(0, 0, 255, 0.2);
}

h1 {
    font-size: 0.375rem;
    color: #fff;
    text-align: center;
    line-height: 1rem;
}

.container {
    // 宽度
    min-width: 15rem;
    max-width: 25.6rem;
    margin: 0 auto;
    padding: .125rem .125rem 0;
    //background-color: gray;
    display: flex;
}

.itemLeft,.itemRight{
    flex: 3;
}

.itemConter{
    flex: 5;
    height: 10.5rem;
    border: 1px solid blue;
    padding: 0.125rem;
    margin: .25rem;
}
</style>