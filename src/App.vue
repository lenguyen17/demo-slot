<template>
  <div id="app">
    <SlotCommonComponent>
      <!-- Use v-slot to specify data for the "header" slot -->
      <template v-slot:header>
        <div>{{ someObject.name }}</div>
      </template>

      <!-- Use v-slot to specify data for the default slot -->
      <template v-slot>
        <div>
          <div v-html="customHtml"></div>
          <div>
            <b>{{ someObject.value }}</b>
          </div>
        </div>
      </template>

      <!-- Use v-slot to specify data for the "footer" slot -->
      <template v-slot:footer>
        <div>{{ someObject.footer }}</div>
      </template>
    </SlotCommonComponent>
  </div>
</template>

<script>
import SlotCommonComponent from './components/SlotCommonComponent.vue';

export default {
  name: 'App',
  components: {
    SlotCommonComponent
  },
  data() {
    return {
      customHtml: "<p>MERRY CHRISTMAS<p>",
      someObject: {
        name: "Quote",
        value: "To the person reading this, Good Luck! Don't stress, everything will be fine. No matter what difficulty you are facing right now, you can overcome it! You are strong and brave",
        footer: "This text was created at 1AM"
      },
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
