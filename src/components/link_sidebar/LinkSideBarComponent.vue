|<template>
<div>
    <a class="link-sidebar"  :href="link">
    <img :src="icon" width="32" height="32" aria-hidden="true" loading="lazy">
    <p><strong>{{title }}</strong></p>
    </a>
    

</div>
</template>
<script>
export default {
    name: "LinkSidebarComponent",
    props: {
    title: {
      type: String,
      required: true
    },
    link: {
      type: String,
      required: true
    },
    icon: {
      type: String,
      required: true
    }
  }
}
</script>

<style>
.link-sidebar {
    height: 50px;
    margin-left: 10px;
    margin-top: 10px;
   margin-bottom: 10px;
    text-align: center;
    color: black;
    text-decoration: none;
    display: flex;
    justify-items: center;
    align-items: center;

}
nav {
    width: 100%;
}

.link-sidebar p {
    margin-left: 10px;
}
.link-sidebar:hover {
    margin-top: 10px;
   margin-bottom: 10px;
background-color: #eee;
transition: 0.3s;
}
</style>
