<template>
    <div class="home">
        <div class="container">
            <list :list="list"></list>
        </div>
    </div>
</template>

<script lang="ts">
    import List, { ColumnProps } from '@/components/List.vue'
    import { defineComponent } from 'vue'

    export default defineComponent({
        name: 'home',
        components: {
            List
        },
        setup () {
            const dataList: ColumnProps[] = [
                {
                    id: 1,
                    title: 'test1的专栏',
                    description: '这是的test1专栏，有一段非常有意思的简介，可以更新一下欧',
                    avatar: 'http://vue-maker.oss-cn-hangzhou.aliyuncs.com/vue-marker/5ee22dd58b3c4520912b9470.jpg?x-oss-process=image/resize,m_pad,h_100,w_100'
                },
                {
                    id: 2,
                    title: 'test2的专栏',
                    description: '这是的test2专栏，有一段非常有意思的简介，可以更新一下欧'
                    // avatar: 'http://vue-maker.oss-cn-hangzhou.aliyuncs.com/vue-marker/5ee22dd58b3c4520912b9470.jpg?x-oss-process=image/resize,m_pad,h_100,w_100'
                },
                {
                    id: 3,
                    title: 'test3的专栏',
                    description: '这是的test3专栏，有一段非常有意思的简介，可以更新一下欧',
                    avatar: 'http://vue-maker.oss-cn-hangzhou.aliyuncs.com/vue-marker/5ee22dd58b3c4520912b9470.jpg?x-oss-process=image/resize,m_pad,h_100,w_100'
                },
                {
                    id: 4,
                    title: 'test4的专栏',
                    description: '这是的test4专栏，有一段非常有意思的简介，可以更新一下欧'
                    // avatar: 'http://vue-maker.oss-cn-hangzhou.aliyuncs.com/vue-marker/5ee22dd58b3c4520912b9470.jpg?x-oss-process=image/resize,m_pad,h_100,w_100'
                }
            ]
            return {
                list: dataList
            }
        }
    })
</script>

<style scoped>
    .home {

    }
</style>
<style>
    .home {

    }
</style>
