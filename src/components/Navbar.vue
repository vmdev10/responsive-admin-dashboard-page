<template>
  <div :class="{active: !sidebarOpen}" class="navbar-container">
    <nav>
      <div @click="toggleSidebar" class="toggle-menu">
        <i class="fas fa-bars"></i>
      </div>

      <div  class="sign-out">
        <a href="/login"><i class="fas fa-sign-out-alt"></i></a>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  name: "Navbar",
  data() {
    return {
      sidebarOpen: true
    }
  },
  methods: {
    toggleSidebar() {
      this.sidebarOpen = !this.sidebarOpen
      console.log(this.sidebarOpen)
      return this.$emit('toggleSidebar', this.sidebarOpen)
    },
  }
}
</script>

<style scoped>
.navbar-container {
  background-color: #04052e;
  width: calc(100% - 16rem);
  height: 2.5rem;
  border-top: 2px solid #140152;
  position: absolute;
  left: 16rem;
  top: 0;
}

nav,
.sign-out a {
  height: 100%;
  padding: 0 1rem;

  display: flex;
  justify-content: space-between;
  align-items: center;
  font-size: 0.9375rem;
  color: #fff;
}

.toggle-menu:hover,
.sign-out {
  cursor: pointer;
}

.active {
  width: 100%;
  left: 0;
}
</style>