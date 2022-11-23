<template>
    <div class="sticky-top">
        <h2>Дата</h2>
        <div v-if="data">
            <div v-for="post in data.allPosts" :key="post.id" class="card">
                <p>{{ post.date }}</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
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