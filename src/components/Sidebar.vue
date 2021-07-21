<template>
  <div v-if="sidebarOpen" class="sidebar-container">
    <div class="sidebar-brand">
      <i class="fab fa-slack"></i>
      <h3>Business</h3>
    </div>

    <SidebarLinks v-for="sidebarLink in sidebarLinks" :key="sidebarLink" :sidebarLink="sidebarLink"/>

    <DropdownMenu
      v-for="dropdownItem in dropdownItems"
      :key="dropdownItem"
      :dropdownItem="dropdownItem"
    />
  </div>
</template>

<script>
import DropdownMenu from "./DropdownMenu.vue";
import SidebarLinks from "./SidebarLinks.vue";

export default {
  name: "Sidebar",
  components: { DropdownMenu, SidebarLinks },
  props: {
    sidebarOpen: {
      type: Boolean,
      require: true
    }
  },
  data() {
    return {
      sidebarLinks: [
        {
          menu: "Dashboard",
          icon: "fas fa-igloo",
        },
        {
          menu: "Tables",
          icon: "fas fa-table",
        },
        {
          menu: "Forms",
          icon: "fas fa-pen-alt",
        },
        {
          menu: "Profile",
          icon: "fas fa-user-circle",
        },
      ],
      dropdownItems: [
        {
          menu: "Usuários",
          icon: "fas fa-users",
          submenu: [
            {
              title: "Todos",
              route: "#",
            },
            {
              title: "Admin",
              route: "#",
            },
            {
              title: "Clientes",
              route: "#",
            },
          ],
        },
        {
          menu: "Marcas",
          icon: "fas fa-list",
          submenu: [
            {
              title: "Todas as marcas",
              route: "#",
            },
            {
              title: "Produtos",
              route: "#",
            },
            {
              title: "Veículos",
              route: "#",
            },
          ],
        },
        {
          menu: "Produtos",
          icon: "fas fa-shopping-bag",
          submenu: [
            {
              title: "Todos",
              route: "#",
            },
            {
              title: "Ativos",
              route: "#",
            },
            {
              title: "Inativos",
              route: "#",
            },
            {
              title: "Aguardando revisão",
              route: "#",
            },
            {
              title: "FInalizados",
              route: "#",
            },
          ],
        },
      ],
    };
  },
};
</script>

<style scoped>
.sidebar-container {
  background-color: #04052e;
  width: 16rem;
  min-height: 100vh;
}

.sidebar-brand {
  height: 3rem;
  padding: 0 2rem;
  border-top: 2px solid #140152;

  display: flex;
  gap: 0.75rem;
  align-items: center;

  color: #fff;
}
</style>
