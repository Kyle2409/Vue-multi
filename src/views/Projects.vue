<template>
<Navbar/>
<div style="background-color:#ea4343">
<div style="padding:41px">
<label class="labels">Sort Name:</label>
 <select v-model="name" @change="sortName(name)">
     <option value="select">-Select-</option>
     <option value="asc">Ascending</option>
     <option value="desc">Descending</option>
 </select>

 <label class="labels">Sort Language:</label>
 <select v-model="slang" @change="sortLang(slang)">
     <option value="select">-Select-</option>
     <option value="asc">Ascending</option>
     <option value="desc">Descending</option>
 </select>

 <label class="labels">Filter by Language</label>
 <select v-model="flang" @change="filterLang(flang)">
     <option value="all">All</option>
     <option value="html">HTML</option>
     <option value="javascript">JavaScript</option>
     <option value="vue">Vue</option>
 </select>
</div>
<div  class="project-container" v-if="projects">
<div v-for="project of projects" :key="project.id" class="projects">     
<router-link :to="{name: 'ProjectDetails',params:{id:project.id}}">
<div class="card" style="width: 18rem;">
    <img :src="project.img_url" class="card-img-top" alt="...">
<div class="card-body">
    <h2>{{project.title}}</h2>
</div>
<ul class="list-group list-group-flush">
    <li class="list-group-item">An item</li>
    <li class="list-group-item">A second item</li>
    <li class="list-group-item">A third item</li>
</ul>
<div class="card-body">
    <a href="#" class="card-link">Card link</a>
    <a href="#" class="card-link">Another link</a>
</div>
</div>
</router-link>
    </div>
</div>
<div v-else>
    <p>loading projects...</p>
</div>
</div>
</template>

<script>
import Navbar from '../components/Navbar.vue'

export default {
    props:['id'],
    data(){
        return{
            projects:[]
        }
    },
mounted(){
    fetch('http://localhost:3000/projects')
    .then(res => res.json())
    .then(data => this.projects=data)
    .catch(err => console.log(err.message))
},
  name: 'Projects',
  components: {
   Navbar
  }
}
</script>

<style>
.project-container {
    background-color: #ea4343;
    padding: 5px;
    display: grid;
    flex-direction: column;
    grid-gap: 1rem;
    justify-content: space-evenly;
    flex-wrap: wrap;
    grid-template-columns: repeat(3 ,1fr);
}
.labels{
    font-family: sans-serif;
    font-size: 20px;
    font-weight: 700;
    color: black;
}
</style>