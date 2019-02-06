<template>
  <div class="main-div">
    hello
  </div>
</template>

<script>    
export default {
  name: "MainDiv",
  data() {
    return {
      msg: "Welcome!",
    };
  },
  methods: {
    updateClick () {
        this.activeSidebar = !this.activeSidebar;
    }
  }
};
</script>

<style>

/* The sidebar menu */
.main-div {
  top: 50px;
  height: 100%;
  width: 100%; /* 0 width - change this with JavaScript */
  position: fixed; /* Stay in place */
  z-index: 0; /* Stay on top */
  bottom: 100px;
  left: 0px;
  transition: 0.5s; /* 0.5 second transition effect to slide in the sidebar */
  background-color: gray;
}

</style>
