<template>
  <section>
    <img v-bind:src="picture" width="150" height="200"/>
    <h1>ชื่อผู้สมัครงาน : {{getfullName()}}</h1>
    <h1>อายุ : {{age}} ปี</h1>
    <p>ที่อยู่ : <span v-html="address"></span></p>
  </section>
</template>
<script>
export default {
  name: 'App',
  data(){
    return{
      firstName:"วริศรา",
      lastName:"พงษ์พิมาย",
      age:17,
      address: "<i>จังหวัดฉะเชิงเทรา</i>",
      picture:"https://thumbor.forbes.com/thumbor/fit-in/900x510/https://www.forbes.com/advisor/wp-content/uploads/2023/07/top-20-small-dog-breeds.jpeg.jpg",
      size:160,
      social:"https://www.facebook.com/warissara.phongphimai.9"
    }
  },
  method:{
    getfullName(){
      return this.firstname + " " + this.lastName 
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

