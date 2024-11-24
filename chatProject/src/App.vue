<script>
export default {
  data(){
    return {
      name : "abdelkader",
      status : "developer",
      skill : ["cpp", "python", "javascript", "php"],
      link  : "https://github.com/Kader1680"
    }
  },

  methods:{
      changeJobs(){
        if (this.status == "developer") {
              this.status = "vue js developer"
          } else if (this.status == "security"){
              this.status = "red team"
          }else{
              this.status = "sorry not know "
          }
    }
  }
}
</script>
<template>

<h3>welcome {{status}}</h3>
<p v-if=" status === 'developer' " > is (devloper)</p>
<p v-else-if=" status === 'cybersecurity' " > is (cybersecurity)</p>
<p v-else >isn't empoloyer</p>
<ul v-for="item in skill" :key="item">
   <li>{{ item }}</li>
</ul>
<a v-bind:href="link">see my projects</a>
<button v-on:click="changeJobs" >change job</button>
</template>
