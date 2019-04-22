<template>
  <button type="button">{{ message | reverse }}</button>
</template>

<script lang="ts">
  import { Component, Prop, Vue } from 'vue-property-decorator';
  // export default {
  //   name: 'VButton',
  // };

  @Component({
    filters: {
      reverse(value: string): string {
        return value.split('').reverse().join('');
      },
    },
  })
  export default class VButton extends Vue {
    @Prop() private message: string = 'hello';
  }

  // export default Vue.extend({
  //   props: {
  //     message: {
  //       type: String,
  //       default: 'hello world',
  //     },
  //   },
  //   data(): object {
  //     return {
  //       test: 'test',
  //     };
  //   },
  // });
</script>

<style scoped>

</style>
