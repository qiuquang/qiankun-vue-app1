<template>
  <div class="about">
    <h1>This is an about page {{ a }}</h1>
    <div @click="gotoApp">gotopage </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      a: 1
    }
  },
  inject: ['mainAppHistory'],
  methods: {
    gotoApp() {
      console.log(this.mainAppHistory);
      this.mainAppHistory.push('/app-react')
    }
  }
}
</script>