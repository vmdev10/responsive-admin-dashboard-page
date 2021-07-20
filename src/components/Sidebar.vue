<template>
  <div class="sidebar-container">
    <div class="sidebar-brand">
      <i class="fab fa-slack"></i>
      <h3>Business</h3>
    </div>

    <SidebarLinks title="Dashboard"><i class="fas fa-igloo"></i></SidebarLinks> 
    <SidebarLinks title="Tables"><i class="fas fa-table"></i></SidebarLinks>
    <SidebarLinks title="Forms"><i class="fas fa-pen-alt"></i></SidebarLinks>
    <SidebarLinks title="Profile"><i class="fas fa-user-circle"></i></SidebarLinks>

    <DropdownMenu title='Usuários' :dropdownItems="['Todos', 'Admin', 'Clientes']"><i class="fas fa-users"></i></DropdownMenu>
    <DropdownMenu title="Marcas" :dropdownItems="['Todas as marcas', 'Produtos', 'Veículos']"><i class="fas fa-list"></i></DropdownMenu>
    <DropdownMenu title="Produtos" :dropdownItems="['Todos', 'Ativos', 'Inativos', 'Aguardando revisão', 'Finalizados']"><i class="fas fa-shopping-bag"></i></DropdownMenu>
  </div>
</template>

<script>
import DropdownMenu from './DropdownMenu.vue'
import SidebarLinks from './SidebarLinks.vue'

export default {
  name: 'Sidebar',
  components: {DropdownMenu, SidebarLinks},
};
</script>

<style scoped>
.sidebar-container {
  background-color: #04052E;
  width: 16rem;
  min-height: 100vh;
}

.sidebar-brand {
  background-color: #140152;
  padding: 1.25rem 2rem;

  display: flex;
  gap: 0.75rem;
  align-items: center;

  color: #fff;
}
</style>
