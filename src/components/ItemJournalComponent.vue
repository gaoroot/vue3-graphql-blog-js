<template>
    <div>
        <div class="card" style="width: 18rem;">
            <div class="card-body">
                <h5 class="card-title">{{ post.title }}</h5>
                <h6 class="card-subtitle mb-2 text-muted">ID: {{ post.id }}</h6>
                <h6 class="card-subtitle mb-2 text-muted">Дата: {{ post.date }}</h6>
                <p class="card-text">{{ post.body }}</p>
                <!-- <button class="btn btn-light" @click="$router.push(`/journal/${post.id}`)">Посмотреть</button> -->
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        post: {
            type: Object,
            required: true,
        }
    }
}
</script>

<style scoped lang="scss">
@import "~bootstrap/scss/bootstrap";

</style>