<template>
  <div id="app">
<b-navbar toggleable="lg" type="dark" variant="danger">
<b-container>
      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
        <b-navbar-brand :to="{name: 'Home'}">Hello Shop</b-navbar-brand>
        <b-collapse id="nav-collapse" is-nav>

        <b-navbar-nav>
            <b-nav-item :to="{name: 'Home'}" exact>Home</b-nav-item>
            <b-nav-item :to="{name: 'Clients'}">Clients</b-nav-item>
            <b-nav-item :to="{name: 'Proveidors'}">Proveïdors</b-nav-item>
            <b-nav-item :to="{name: 'Magatzem'}">Magatzem</b-nav-item>
            <b-nav-item-dropdown text="Botiga" right>
              <b-dropdown-item :to="{name: 'Alimentacio'}">Alimentació</b-dropdown-item>
              <b-dropdown-item :to="{name: 'Congelats'}">Congelats</b-dropdown-item>
            </b-nav-item-dropdown>
        </b-navbar-nav>

        </b-collapse>
</b-container>
</b-navbar>

  
      <b-container>
          <transition name="router-anim">
            <router-view/>
          </transition>
      </b-container>

  </div>
</template>

<style>
@import "https://cdn.jsdelivr.net/npm/animate.css@3.5.1";

.router-anim-enter-active {
  animation: coming 1s;
  animation-delay: .5s;
  opacity: 0;
}
.router-anim-leave-active {
  animation: going 1s;
}

@keyframes going {
  from {
    transform: translateX(0);
  }
  to {
    transform: translateX(-50px);
    opacity: 0;
  }
}
@keyframes coming {
  from {
    transform: translateX(-50px);
    opacity: 0;
  }
  to {
    transform: translateX(0);
    opacity: 1;
  }
}

</style>