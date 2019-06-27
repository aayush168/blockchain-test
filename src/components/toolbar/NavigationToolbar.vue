<template>
  <ul class="navToolbar">
    <li class="subheading font-weight-light" >Users</li>
    <li class="subheading font-weight-light">Add Addres Info</li>
    <li class="subheading font-weight-light">Address Lists </li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      selectedTab: 'users'
    }
  },
}
</script>

<style lang="stylus">
.navToolbar {
  list-style-type: none;
  display: flex;
  justify-content: center;
  padding: 10px;
  background-color: #f5f5f5;
  li {
    list-style: none;
    padding: 10px 20px;
    &:hover {
      cursor pointer;
    }
  }
}
</style>
