<template>
  <div class="SidebarLinks">
    <div class="SidebarLinks-header">
      <i :class="sidebarLink.icon"></i>
      <h3>{{ sidebarLink.menu }}</h3>
    </div>
  </div>
</template>

<script>
export default {
  name: "SidebarLinks",
  props: {
    sidebarLink: {
      type: Object,
      require: true,
    },
  },
};
</script>

<style>
.SidebarLinks-header {
  padding: 0.75rem 2rem;

  display: flex;
  align-items: center;
  gap: 0.625rem;

  color: #fff;
}

.SidebarLinks-header:hover,
.SidebarLinks-header:active {
  background-color: #fff;
  color: #04052e;
  cursor: pointer;
}

.SidebarLinks-header h3 {
  font-size: 1rem;
  line-height: 1.5rem;
  font-weight: 500;
}
</style>
