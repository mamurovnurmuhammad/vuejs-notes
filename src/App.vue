<template>
  <div class="my-auto text">
     You can add note
  </div>
  <form>
    <div class="flexcontainer">
    <div class="left tools">
      <div class="containertext">Tools</div>
    </div>
    <div class="container">
      <div class="containertext">Enter your note or reference</div>
      <input type="text" placeholder="Enter your title" class="form-control inputtext" v-model="title">
      <textarea type="text" placeholder="Enter your note" class="form-control inputtext" v-model="note"></textarea>
      <button class="btn1">Submit</button>
      <dir class="checkbox">
        <input type="checkbox">
        <h5>pin</h5> 
      </dir>
    </div>
    <div class="right tools">
      <div class="containertext">Your notes</div>
      <p class="">{{title}}</p>
    </div>
    </div>
  </form>
</template>

<script>


export default {
  name: 'App',
  data() {
    return {
      title: '',
      note: '',
      data() {
        return {
          array:[
            { id: 1, title: '', notes: ''}
          ]
        }
      },
    }
  },
  components: {
  }
}
</script>

<style>
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.flexcontainer{
  display: flex;
}

.text{
  backdrop-filter: blur(15px);
  display: flex;
  justify-content: center;
  font-family: 'Bebas Neue', cursive;
  height: 50px;
  align-items: center;
  font-size: 35px;
}
body{
  background: url('https://life.getflywheel.com/wp-content/uploads/2016/08/Whats-at-Your-Desk-Wednesday-Josh-C-0298.jpg');
  background-repeat: no-repeat;
  background-size: cover;
}
.container{
  width: 50%;
  margin-top: 50px;
  backdrop-filter: blur(35px);
  height: 320px;
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.containertext{
  font-family: 'Bebas Neue', cursive;
  display: flex;
  justify-content: center;
  align-items: center;
  /* border: 1px solid red; */
  height: 50px;
  font-size: 25px;
}
.tools{
  backdrop-filter: blur(35px);
  height: 500px;
  width: 250px;
  display: inline-block;
  border-radius: 0px 10px 10px 0px;
  margin-top: 50px;
}
.right{
  border-radius: 10px 0px 0px 10px;
}
.form-control{
  font-family: 'Mukta', sans-serif;
}
.inputtext{
  margin-top: 20px;
}
.btn1{
border-radius: 10px;
padding: 9px 15px;
margin-top: 30px;
background: #27272667;
border: none;
color: #fff;
font-size: 20px;
font-family: 'Mukta', sans-serif;
}
.btn1:hover{
background: #17171767;
box-shadow: 0px 0px 5px black;
}
.checkbox{
  display:flex;
  align-items: center;
  width: 50px;
  height: 25px;
  /* border: 1px solid red; */
  justify-content: space-around;
  margin-top: 10px;
}
.checkbox input {
  height: 15px;
  width: 15px;
}
.checkbox h5{
  color: white;
}
</style>
