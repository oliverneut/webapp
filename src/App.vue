<template>
  <div id="app">
    <header>
          <a class="title" href=""> <div class="surname" >Oliver</div> <div class="name">Neut</div> </a>
          <nav>
              <ul class="nav_links">
                  <li><router-link to="/home">Home</router-link></li>
                  <li><router-link to="/projects">Projects</router-link></li>
                  <li><router-link to="/contact">Contact</router-link></li>
              </ul>
          </nav>
      </header>
      <router-view/>
    </div>
</template>

<style>

</style>
