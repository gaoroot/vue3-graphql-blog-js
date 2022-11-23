<template>
    <div class="sticky-top">
        <h2>Добавить запись</h2>
        <div class="mb-3">
            <label for="FormControlInput1" class="form-label">Title</label>
            <input type="title" class="form-control" id="FormControlInput1" placeholder="title">
        </div>
        <div class="mb-3">
            <label for="FormControlTextarea1" class="form-label">Body</label>
            <textarea class="form-control" id="FormControlTextarea1" rows="6" placeholder="body"></textarea>
        </div>
    </div>
</template>

<script>
  export default {

  }
// console.log(`🚀 Server ready at ${title}`);
</script>

<style scoped lang="scss">
@import "~bootstrap/scss/bootstrap";

</style>