<template>
  <Page>
    <ActionBar>
      <Label text="Home" />
    </ActionBar>

    <FlexboxLayout flexDirection="column" justifyContent="center">
      <Label
        class="p-5 m-l-15 m-r-15 m-b-15 text-center"
        :text="message"
        @tap="logMessage"
      />
      <Label class="p-5 m-l-15 m-r-15 m-b-15 text-center" :text="count" />
      <Button text="Botãozinho" class="button" @tap="increment"></Button>
    </FlexboxLayout>
  </Page>
</template>

<script lang="ts">
import Vue from 'nativescript-vue';

export default Vue.extend({
  data: () => ({
    count: 1,
  }),
  computed: {
    message() {
      return 'Olá Cainho lindo';
    },
  },

  methods: {
    logMessage() {
      console.log('You have tapped the message!');
    },
    increment() {
      this.count++;
    },
  },
});
</script>

<style scoped>
.info {
  font-size: 20;
  horizontal-align: center;
  vertical-align: center;
}
</style>
