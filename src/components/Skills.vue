<template>
  <div class="skills">
    <div class="holder">
      <ul>
        <li v-for="(data, index) in skills" :key='index'>{{ index }}. {{ data.skill }}</li>
      </ul>

      <p v-if="skills.length >= 2">You have more than one skill.</p>
      <p v-else>You have less than or equal to one skill.</p>

      <div v-bind:style="alertObject">test</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Skills',
  data() {
    return {
      skills: [
        { "skill": "Vue.js" },
        { "skill": "Frontend Developer" }
      ],
      alertObject: {
         backgroundColor: 'yellow',
         backgroundWidth: '100%',
         backgroundHeight: '30px'
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style src="./Skills.css" scoped>

</style>
