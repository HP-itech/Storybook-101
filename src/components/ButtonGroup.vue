<template>
        <Button v-for="button in buttons"
        :key="button.id"
        :label="button.label"/>
</template>

<script>
import Button from'./Button.vue'
import { reactive, computed } from 'vue'

export default {
    name: 'ButtonGroup',
    components: { Button },
    props: {
        buttons: { type: Array, required: true, default: () => [] },
    },
      setup(props) {
    props = reactive(props);
    return {
      isEmpty: computed(() => props.buttons.length === 0),
    };
  },
};
</script>