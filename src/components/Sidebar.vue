<template>
  <div class="sidebar-container">
    <div class="sidebar-brand">
      <i class="fab fa-slack"></i>
      <h3>Business</h3>
    </div>

    <div class="dashboard">
      <div class="dashboard-header">
        <i class="fas fa-igloo"></i>
        <h3>
          Dashboard
        </h3>
       </div>
    </div>

    <div @click="openUserList" class="users">
      <div class="user-header">
        <div class="user-title">
          <i class="fas fa-users"></i>
          <h3>Usuários</h3>
        </div>

        <span><i class="fas fa-chevron-down"></i></span>
      </div>

      <ul v-if="userList" class="user-items">
        <li>Todos</li>
        <li>Admin</li>
        <li>Clientes</li>
      </ul>
    </div>

    <div @click="openBrandsList" class="brands">
      <div class="brands-header">
        <div class="brands-title">
          <i class="fas fa-list"></i>
          <h3>Marcas</h3>
        </div>

        <span><i class="fas fa-chevron-down"></i></span>
      </div>

      <ul v-if="brandsList" class="brands-items">
        <li>Todas as marcas</li>
        <li>Produtos</li>
        <li>Veículos</li>
      </ul>
    </div>

    <div @click="openProductsList" class="products">
      <div class="products-header">
        <div class="products-title">
          <i class="fas fa-shopping-bag"></i>
          <h3>Products</h3>
        </div>

        <span><i class="fas fa-chevron-down"></i></span>
      </div>

      <ul v-if="productsList" class="products-items">
        <li>Todos</li>
        <li>Ativos</li>
        <li>Inativos</li>
        <li>Aguardando revisão</li>
        <li>Finalizados</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      userList: false,
      brandsList: false,
      productsList: false
    }
  },

  methods: {
    openUserList() {
      this.userList = !this.userList
      return this.userList
    },

    openBrandsList() {
      this.brandsList = !this.brandsList
      return this.brandsList
    },

    openProductsList() {
      this.productsList = !this.productsList
      return this.productsList
    },    
  }
};
</script>

<style scoped>
.sidebar-container {
  background-color: #6f73d2;
  width: 16rem;
  height: 100vh;
}

.sidebar-brand {
  background-color: #7681b3;
  padding: 1.25rem 2rem;

  display: flex;
  gap: 0.75rem;
  align-items: center;

  color: #fff;
}

.dashboard {
  background-color: #83c9f4;
}

.dashboard-header {
  background-color: crimson;
  padding: 0.75rem 2rem;

  display: flex;
  align-items: center;
  gap: 0.625rem;

  color: #fff;
}

.dashboard-header:hover,
.dashboard-header:active {
  background-color: #fff;
  color: #6f73d2;
  cursor: pointer;
}

.dashboard-header h3 {
  font-size: 1rem;
  line-height: 1.5rem;
  font-weight: 500;
}

.users {
  background-color: #a3d5ff;
}

.user-header {
  background-color: chocolate;
  padding: 0.75rem 2rem;

  display: flex;
  justify-content: space-between;
  align-items: center;

  color: #fff;
}

.user-header:hover,
.user-header:active {
  background-color: #fff;
  color: #6f73d2;
  cursor: pointer;
}

.user-title {
  display: flex;
  align-items: center;
  gap: 0.625rem;
}

.user-title h3 {
  font-size: 1rem;
  line-height: 1.5rem;
  font-weight: 500;
}

.user-items li {
  background-color: chocolate;
  padding: 0.5rem 3.75rem;
  font-size: 1rem;
  line-height: 1.5rem;
  color: #fff;
}

.user-items li:hover,
.user-items li:active {
  background-color: #fff;
  color: #6f73d2;
  cursor: pointer;
}

.brands {
  background-color: #d9f0ff;
}

.brands-header {
  background-color: darkblue;
  padding: 0.75rem 2rem;

  display: flex;
  justify-content: space-between;
  align-items: center;

  color: #fff;
}

.brands-header:hover,
.brands-header:active {
  background-color: #fff;
  color: #6f73d2;
  cursor: pointer;
}

.brands-title {
  display: flex;
  align-items: center;
  gap: 0.625rem;
}

.brands-title h3 {
  font-size: 1rem;
  line-height: 1.5rem;
  font-weight: 500;
}

.brands-items li {
  background-color: darkblue;
  padding: 0.5rem 3.75rem;
  font-size: 1rem;
  line-height: 1.5rem;
  color: #fff;
}

.brands-items li:hover,
.brands-items li:active {
  background-color: #fff;
  color: #6f73d2;
  cursor: pointer;
}

.products {
  background-color: #7681b3;
}

.products-header {
  background-color: gold;
  padding: 0.75rem 2rem;

  display: flex;
  justify-content: space-between;
  align-items: center;

  color: #fff;
}

.products-header:hover,
.products-header:active {
  background-color: #fff;
  color: #6f73d2;
  cursor: pointer;
}

.products-title {
  display: flex;
  align-items: center;
  gap: 0.625rem;
}

.products-title h3 {
  font-size: 1rem;
  line-height: 1.5rem;
  font-weight: 500;
}

.products-items li {
  background-color: gold;
  padding: 0.5rem 3.75rem;
  font-size: 1rem;
  line-height: 1.5rem;
  color: #fff;
}

.products-items li:hover,
.products-items li:active {
  background-color: #fff;
  color: #6f73d2;
  cursor: pointer;
}

</style>
