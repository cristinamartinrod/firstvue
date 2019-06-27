<template>
  <div id="app">
    <link
      rel="stylesheet"
      href="https://use.fontawesome.com/releases/v5.7.2/css/all.css"
      integrity="sha384-fnmOCqbTlWIlj8LyTjo7mOUStjsKC4pOpQbqyi7RrhN7udi9RwhKkMHpvLbHG9Sr"
      crossorigin="anonymous"
    >
    <section class="home">
      <div class="border"></div>
      <h1>{{ logo }}</h1>
      <projects />
    </section>
  </div>
</template>



<script>
import projects from "@/containers/projects";
export default {
  name: "App",
  components: {
    projects: projects,
  },
  data() {
    return {
      logo: "My projects"
    };
  },
};
</script>
<style lang="scss">
body,
html {
  width: 100%;
  height: 100%;
  margin: 0;
  padding: 0;
  font-family: "Roboto", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
#app {
  height: 100vh;
}
.home {
  h1,
  h2 {
    padding: 5px;
    width: 100%;
    margin: 20px auto;
    max-width: 230px;
    border: 5px solid #9DB6EC;
    color: #9DB6EC;
    font-weight: 800;
    font-size: 1.5em;
    text-align: center;
  }
  .search {
    background-color: #f4f4f5;
    border-radius: 20px;
    border: 0;
    width: 100vw;
    max-width: 300px;
    padding: 10px;
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 0 auto;
  }

  .border {
    height: 15px;
    width: 100%;
    background-color: #9DB6EC;
  }

  #app {
    font-family: "Roboto", Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
    width: 100%;
    height: 100%;
    margin: 0;
    padding: 0;
  }

  .addNewProject {
    border: 1px solid grey;
    border-radius: 5px;
    background-color: white;
    padding: 5px 15px 5px 15px;
    font-size: 1em;
    font-family: "Roboto", Helvetica, Arial, sans-serif;
    color: grey;
    display: flex;
    margin: 0 auto;
  }
}

.project {
  display: flex;
  max-height: 100%;
  margin: 30px 0;

  .image {
    background: url("https://www.azutura.com/media/catalog/product/cache/50/thumbnail/100x100/9df78eab33525d08d6e5fb8d27136e95/W/S/WS-42542_WP-01.jpg");
    width: 91px;
    height: 91px;
    background-size: cover;
    margin-right: 20px;
    background-repeat: no-repeat;
    background-position: center center;
  }

  .textContent {
    width: 100%;
    .title {
      margin: 0;
      display: flex;
      flex-direction: column;
      justify-content: flex-start;
      align-items: flex-start;
    }

    .header-box {
      display: flex;
      flex-direction: row;
      align-items: center;
      justify-content: space-between;
      margin: 5px 0;
      .btns {
        padding-right: 10px;
        span {
          width: 20px;
          width: 20px;
          margin: 0 5px;
        }
      }
    }
    .text {
      margin: 0;
    }
  }
}
</style>
