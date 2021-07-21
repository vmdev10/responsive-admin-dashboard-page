<template>
  <div class="home">
    <Sidebar :sidebarOpen="sidebarOpen"/>
    <Navbar @toggleSidebar="sidebarOpen = $event"/>
  </div>
</template>

<script>
import Sidebar from "@/components/Sidebar.vue";
import Navbar from "@/components/Navbar.vue";

export default {
  name: "Home",
  components: {
    Sidebar,
    Navbar
  },
  data() {
    return {
      sidebarOpen: true
    }
  }
};
</script>
