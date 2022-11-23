<template>
    <div class="card" style="width: 18rem;">
        <h2>Записи</h2>
        <div v-if="data">
            <item-journal-component-vue v-for="post in data.allPosts" :key="post.id" :post="post"/>
        </div>
    </div>
</template>

<script>
import ItemJournalComponentVue from './ItemJournalComponent.vue';

export default {
    components: { 
        ItemJournalComponentVue,
        },
    props: {
        data: {
            type: Array,
            required: true
        }
    }
}
</script>

<style scoped lang="scss">
@import "~bootstrap/scss/bootstrap";

</style>