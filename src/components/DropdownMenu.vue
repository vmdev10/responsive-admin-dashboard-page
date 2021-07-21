<template>
  <div @click="openDropdownMenu" class="dropdownMenu">
    <div class="dropdownMenu-header">
      <div class="dropdownMenu-title">
        <i :class="dropdownItem.icon"></i>
        <h3>{{ dropdownItem.menu }}</h3>
      </div>

      <span :class="{active: dropdownMenu}" class="arrow-icon"><i class="fas fa-chevron-down"></i></span>
    </div>

    <ul v-if="dropdownMenu" class="dropdownMenu-items">
      <!-- Falta add o link -->
      <li v-for="submenu in dropdownItem.submenu" :key="submenu">{{ submenu.title }}</li>
    </ul>
  </div>
</template>

<script>

export default {
  name: "DropdownMenu",
  props: {
    dropdownItem: {
      type: Object,
      require: true
    }
  },
  data() {
    return {
      dropdownMenu: false,
    };
  },

  methods: {
    openDropdownMenu() {
      this.dropdownMenu = !this.dropdownMenu;
      return this.dropdownMenu;
    },
  },
};
</script>

<style>
.dropdownMenu-header {
  padding: 0.75rem 2rem;

  display: flex;
  justify-content: space-between;
  align-items: center;

  color: #fff;
}

.dropdownMenu-header:hover,
.dropdownMenu-header:active {
  background-color: #fff;
  color: #04052E;
  cursor: pointer;
}

.dropdownMenu-title {
  display: flex;
  align-items: center;
  gap: 0.625rem;
}

.dropdownMenu-title h3 {
  font-size: 1rem;
  line-height: 1.5rem;
  font-weight: 500;
}

.arrow-icon {
  font-size: 0.875rem;
  line-height: 1.25rem;
}

.active svg {
  transform: rotateX(180deg);
}

.dropdownMenu-items li {
  background-color: #140152;
  padding: 0.5rem 3.75rem;
  font-size: 0.9375rem;
  line-height: 1.5rem;
  color: #fff;
}

.user-items li:hover,
.user-items li:active {
  background-color: #fff;
  color: #6f73d2;
  cursor: pointer;
}
</style>
