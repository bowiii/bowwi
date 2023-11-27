<template>
  <section>
    <img v-bind:src="picture" width="260" height="300">
    <h1>ชื่อผู้สมัครงาน : {{fullname()}}</h1>
    <h1>อายุ : {{age}} ปี</h1>
    <p>ที่อยู่ : <span v-html="address"></span></p>
    <h2><img v-bind:src="picture1" width="30" height="25"> : <a :href="social" target="_blank">Warissara Phongphimai</a></h2>
  </section>
</template>

<script>
export default {
  name: 'App',
  data(){
    return{
      firstname:"วริศรา",
      lastname:"พงษ์พิมาย",
      age:17,
      address:"<i>จังหวัดฉะเชิงเทรา</i>",
      picture:"https://www.pedigree.co.th/cdn-cgi/image/format=auto,q=90/sites/g/files/fnmzdf3521/files/2022-02/hero-5-dog.png",
      social:"https://www.facebook.com/warissara.phongphimai.9",
      picture1:"https://cdn.pixabay.com/photo/2021/06/15/12/51/facebook-6338509_1280.png"
    }
  },
  methods:{
    fullname(){
      return this.firstname + " "+ this.lastname
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