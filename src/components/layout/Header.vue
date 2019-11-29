<template>
    <header class="header">
        <h1>To Do List</h1>
        <div id="nav">
            <router-link to="/">Home</router-link> |
            <router-link to="/about">About</router-link>
        </div>
    </header>
</template>

<script>
export default {
    name: "Header"
}
</script>

<style scoped>
    .header {
        background: #ABFFFF;
        color:#5176E8;
        text-align: center;
        padding: 10px;
    }
    .header a:link {
        color: #fff;
        padding-right: 5px;
        text-decoration: none;
    }
    .header a:visited {
        color: gray;
        padding-right: 5px;
        text-decoration: none;
    }
    .header a:hover {
        color: darkturquoise;
    }
    .header a:active {
        color: #fff;
    }
</style>