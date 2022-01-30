<template>
<Navbar/>
  <div id="resume" >
    <h3 class="resume">My Resume</h3> <br>
    <p class="background">A Resume Of My Educational Background And A Bit Of Voluntering</p>
    <div style="display: flex; justify-content: center ; gap: 100px ; height: 669px ; padding: 95px">
      <div style="padding:57px">
        <h3 class="main-title">
      <span>Education</span>
    </h3>
    <ul class="resume-list" style="list-style-type:none ">
      <li>
        <div class="resume-info">
          <div class="left">
            <h3>Chuma Public Primary</h3>
          </div>
          <div class="right">
            <span>2008-2014</span>
          </div>
        </div>
        <div class="text">
            <p>A public school located in Town Two, Khayelitsha</p>
          </div>
      </li>
      <li>
        <div class="resume-info">
          <div class="left">
            <h3>Luhlaza High</h3>
          </div>
          <div class="right">
            <span>2015-2019</span>
          </div>
        </div>
        <div class="text">
            <p>A public school located in Khayelitsha</p>
          </div>
      </li>
      <li>
        <div class="resume-info">
          <div class="left">
            <h3>Lifechoices Coding Academy</h3>
          </div>
          <div class="right">
            <span>2021-present</span>
          </div>
        </div>
        <div class="text">
            <p>A coding academy located in Lansdowne</p>
          </div>
      </li>
    </ul>
      </div>
      <div>
         <h3 class="main-title">
      <span>Voluntering</span>
    </h3>
    <ul class="resume-list" style="list-style-type:none">
      <li>
        <div class="resume-info">
          <div class="left">
            <h3>Rise Women's club</h3>
          </div>
          <div class="right">
            <span>2016</span>
          </div>
        </div>
        <div class="text">
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Veritatis, natus.</p>
          </div>
      </li>
      <li>
        <div class="resume-info">
          <div class="left">
            <h3>Ikamva Youth</h3>
          </div>
          <div class="right">
            <span>2018</span>
          </div>
        </div>
        <div class="text">
            <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Aliquid, delectus.</p>
          </div>
      </li>
      <li>
        <div class="resume-info">
          <div class="left">
            <h3>Pascap Trust</h3>
          </div>
          <div class="right">
            <span>2015</span>
          </div>
        </div>
        <div class="text">
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Suscipit, sed.</p>
          </div>
      </li>
    
    </ul>
      </div>
    </div>
  </div>
</template>
<script>
import Navbar from '../components/Navbar.vue'

export default {
  name: 'Resume',
  components: {
  Navbar
  }
}
</script>

<style>
.resume{
    font-family: sans-serif;
    font-size: 60px;
    font-weight: 700;
    color: #ea4343;
    letter-spacing: -.2px;
    display: inline-block;
    margin-bottom: 6px;
}
.background{
  font-family: sans-serif;
    font-size: 20px;
    font-weight: 700;
    color: #fff;
    letter-spacing: -.2px;
    display: inline-block;
    margin-bottom: 6px;
}
.main-title{
    font-family: sans-serif;
    font-size: 30px;
    font-weight: 700;
    color: #ea4343;
    letter-spacing: -.2px;
    /* display: inline-block; */
    margin-bottom: 6px;
}
.resume-info{
  width: 100%;
  display: flex;
  justify-content: space-between;
  margin-bottom: 10px;
}
.resume .resume-list li{
  margin: 0 0 40px 0;
  width: 100%;
  list-style: none;
}
.left {
  font-family: sans-serif;
  font-size: 30px;
  font-weight: 700;
  color: #fff;
}
.right{
  font-family: sans-serif;
  font-size: 30px;
  font-weight: 700;
  color: #fff;
}
.text{
  font-family: sans-serif;
  font-size: 20px;
  font-weight: 700;
  color: #fff;
}
</style>