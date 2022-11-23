<template>
    <div class="journal">
        <JournalComponentVue msg="Журнал"/>
    </div>
</template>

<script>
import JournalComponentVue from '@/components/JournalComponent.vue';

export default {
name: 'JournalComponent',
components: {
    JournalComponentVue
}
}
</script>