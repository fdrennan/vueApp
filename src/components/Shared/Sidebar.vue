<template>
  <div id="mySidebar" 
        v-bind:style="{left: sidebarLeft, backgroundColor: backgroundColor}"
       class="sidebar">
    <ul id="sidebar-ul"
       >

      <li class="sidebar-li">
        <button type="submit" 
                id="sidebar-submit"
                v-on:click="updateClick"
                v-bind:style="{ backgroundColor: clickColor}">
                    <font-awesome-icon icon="bars" /></button>
        </li>

      <li class="sidebar-li">
        <a href="#">{{msg}}</a>
        </li>

      <li class="sidebar-li">
            <input class="sidebar-date" type="date" name="bday" max="1979-12-31">
            <input class="sidebar-date" type="date" name="bday" min="2000-01-02">
        </li>
  
      <li  id="sidebar-datasets" >
         <select v-model="selected">
                  <option disabled value="">Please select one</option>
                  <option>Iris</option>
                  <option>mtcars</option>
        </select>
        <span>Selected: {{ selected }}</span>
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
      backgroundColor:  "rgb(28, 28, 28, .5)",
      sidebarLeft: 50 + "px",
      activeSidebar: true,
      clickColor: "rgb(28, 28, 28, .5)",
      selected: ""
    };
  },
  methods: {
    updateClick () {
        this.activeSidebar = !this.activeSidebar;
        if(this.activeSidebar) {
            this.backgroundColor = "rgb(28, 28, 28, .5)";
            this.sidebarLeft = 50 + "px";
        } else {
            this.backgroundColor = "rgb(28, 28, 28, 0)";
            this.sidebarLeft = -274 + "px"
        }
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
  color: white;
}

/* When you mouse over the navigation links, change their color */
.sidebar a:hover {
  color: #f1f1f1;
  border-style: solid;
  border-width: 0px 0px 1px 0px;
}

#sidebar-ul {
    list-style: none;
    padding: 0;
}

.sidebar-li {
    list-style: none;
    padding: 3px;
    text-align: center;
}

#sidebar-submit {
    width: 100%;
    text-align: right;
    color: white;
}

.sidebar-date {
    font-size: 10px;
    width: 100px;
    display: inline-block;
}

#sidebar-datasets {
    text-align: center;
}

</style>
