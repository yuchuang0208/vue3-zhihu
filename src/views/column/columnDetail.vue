<template>
    <div class="columnDetail">
        <div class="column-detail-page w-75 mx-auto">
            <div class="column-info row mb-4 border-bottom pb-4 align-items-center" v-if="column">
            <div class="col-3 text-center">
                <img :src="column.avatar" :alt="column.title" class="rounded-circle border ">
            </div>
            <div class="col-9">
                <h4>{{column.title}}</h4>
                <p class="text-muted">{{column.description}}</p>
            </div>
            </div>
            <post-list :list="list"></post-list>
        </div>
    </div>
</template>

<script lang="ts">
    import { defineComponent } from 'vue'
    import { useRoute } from 'vue-router'
    import { testData, testPosts } from '@/data/testData'
    import PostList from '@/views/column/PostList.vue'

    export default defineComponent({
        name: 'columnDetail',
        components: {
            PostList
        },
        setup () {
            const route = useRoute()
            const currentId = +route.params.id
            const column = testData.find(c => c.id === currentId)
            const list = testPosts.filter(post => post.columnId === currentId)
            return {
                route,
                column,
                list
            }
        }
    })
</script>

<style scoped>
    .columnDetail {

    }
</style>
<style>
    .columnDetail {

    }
</style>
