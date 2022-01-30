<template>
<div id="nav">
  <nav class="navbar navbar-expand-lg navbar-light bg-dark sticky">
  <div class="container-fluid">
    <a class="navbar-brand" href="#"> <h1><span>K</span>YLE <span>M</span>C <span>B</span>RYNE</h1></a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item">
        <router-link to="/">Home</router-link> 
        </li><br>
         <li class="nav-item">
          <router-link :to="{name:'About'}">About</router-link> 
        </li><br>
        <li class="nav-item">
            <router-link :to="{name: 'Resume'}">Resume</router-link> 
        </li><br>
        <li class="nav-item">
          <router-link :to="{name:'Projects'}">projects</router-link> 
        </li><br>
        <li class="nav-item">
          <router-link :to="{name:'Testimonials'}">Testimonials</router-link> 
        </li><br>
        <li class="nav-item">
          <router-link :to="{ name: 'Contact'}">contact</router-link> 
        </li>
      </ul>
    </div>
  </div>
</nav>
</div>
</template>

<script>
export default {

}
</script>

<style>

#nav{
  z-index: -2;
}
#nav a {
font-weight: bold;
color: white;
text-decoration: none;
padding: 10px;
border-radius: 4px;
}

#navbar a.router-link-exact-active {
color: white;
background: crimson;
}
div#navbarNav{
  justify-content: end;
}
 span {
	color: crimson;
}
</style>