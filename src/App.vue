<template>
  <!-- <div class="container m-auto" style="background: rgb(84 84 84); color: white;" >
    <div class="row">
      <div class="col-12 col-md-4"> 
         <div class="d-flex  align-items-center "> 
     <router-link  to="/"><p class="color-white mb-0 "> Home</p></router-link> |
     <router-link to="/about"><p class="color-white mb-0"> Feed</p></router-link>
  </div>
      </div>
      <div class="col-12 col-md-3"> 
         <div class="d-flex"><input name="search" id="search" placeholder="nhập thông tin tìm kiếm"> 
      <button>  <i class="fa fa-search"> </i></button>
    </div>
        </div>
        <div class="col-12 col-md-5"> 
         <div class="d-flex"><input name="search" id="search" > 
      <button>  <i class="fa fa-search"> </i></button>
    </div>
        </div>
    </div>
   
   
  </div> -->
  <header class="">
      <nav class="navbar navbar-expand-lg">
        <div class="container">
          <a class="navbar-brand" href="index.html"><h2>V<em>sound</em></h2></a>
          <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarResponsive" aria-controls="navbarResponsive" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbarResponsive">
            <ul class="navbar-nav ml-auto">

              
              <li class="nav-item active">
                <a class="nav-link" href="/">Home
                  <span class="sr-only">(current)</span>
                </a>
              </li> 
              <li class="nav-item">
                <a class="nav-link" href="/about">favoris</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="/about">Category</a>
              </li>
              <li class="nav-item mt-2 ">
                <input placeholder="Search" id="searchSound" name="searchSound">
                <button> <i class="fa fa-search"> </i></button>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#">For Producer </a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#">Upload</a>
              </li>
              <li class="nav-item d-flex">
                <img style="width: 30px; height:30px;  border-radius: 50px;" class="mt-2"  src="https://scontent.fhan17-1.fna.fbcdn.net/v/t39.30808-6/345256734_278921197796034_4130124785679367968_n.jpg?_nc_cat=106&ccb=1-7&_nc_sid=09cbfe&_nc_ohc=tLVTwABH6iYAX8n5fkT&_nc_ht=scontent.fhan17-1.fna&oh=00_AfDsRJMPMk03qolFEhfyXrlcLcdeRhMOo9MEXK2F6Euo1w&oe=64634837">
                <a class="nav-link color-white"> Profile</a>
              </li>
            </ul>
          </div>
        </div>
      </nav>
    </header>
 
  <router-view/>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
