<template>
  <div id="mySidebar" class="sidebar">
    <ul id="sidebar-ul">

      <li class="sidebar-li">
        <button type="submit" 
                id="sidebar-submit"
                v-on:click="updateClick"
                v-bind:style="{ fontSize: fontSize + 'px' }">
                    Click Me</button>
        </li>

      <li class="sidebar-li">
        <a href="#">{{msg}}</a>
        </li>

      <li class="sidebar-li">
        <a href="#">Services</a>
        </li>

    </ul>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      msg: "Welcome!",
      fontSize: 10
    };
  },
  methods: {
    updateClick () {
        this.fontSize = this.fontSize + 1;
        console.log(this.fontSize)
    }
  }
};
</script>

<style>
#sidebar-submit {
  right: 0;
}
/* The sidebar menu */
.sidebar {
  top: 60px;
  height: 600px;
  width: 300px; /* 0 width - change this with JavaScript */
  position: fixed; /* Stay in place */
  z-index: 1; /* Stay on top */
  bottom: 100px;
  left: 10%;
  background-color: rgb(86, 188, 235, 0.3); /* Black*/
  transition: 0.5s; /* 0.5 second transition effect to slide in the sidebar */
}

/* The sidebar links */
.sidebar a {
  padding: 10px;
  text-decoration: none;
  font-size: 25px;
  color: #818181;
  display: block;
  transition: 0.3s;
}

/* When you mouse over the navigation links, change their color */
.sidebar a:hover {
  color: #f1f1f1;
}

#sidebar-ul {
    list-style: none;
    padding: 0;
}

.sidebar-li {
    list-style: none;
    padding: 0;
    background-color: black;
}

#sidebar-submit {
    width: 100%;
}
</style>
