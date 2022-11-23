<template>
    <div class="journal">
        <h1>{{ msg }}</h1>
        <div class="container text-center">
            <div class="row">
                <div class="col">
                    <AddItemJournalComponentVue :data="data"/>
                </div>
                <div class="col">
                    <DateJournalComponentVue :data="data"/>
                </div>
                <div class="col">
                    <AllPostsJournalComponentVue :data="data"/>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import AddItemJournalComponentVue from '@/components/AddItemJournalComponent.vue';
import DateJournalComponentVue from '@/components/DateJournalComponet.vue';
import AllPostsJournalComponentVue from '@/components/AllPostsJournalComponent.vue';
import { useQuery } from 'villus'

export default {
    components: {
        AddItemJournalComponentVue,
        DateJournalComponentVue,
        AllPostsJournalComponentVue,
    },
  name: 'journalComponent',
  setup() {
    const allPosts = `
    query allPosts {
        allPosts {
          id
          title
          body
          date
        }
      }
    `;
    const { data } = useQuery({
        // query: '{ allPosts { id , title, body, date }}',
        query: allPosts
    });
    return { data };
  },
  created(){
        document.title = "Страница | Journal" //title
    },
  props: {
    msg: String
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
// Import all of Bootstrap's CSS
@import "~bootstrap/scss/bootstrap";

</style>
