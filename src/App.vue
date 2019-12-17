<template>
  <div id="app">
      <projects :projects="projects" />
  </div>
</template>

<script>
import projects from './components/projects.vue'

export default {
  name: 'app',
  components: {
      projects,
  },
  data() {
      return {
          projects: [
              {
                  id: 1,
                  image: 'http://www.picsum.photos/800/401?random',
                  title: 'Star Wars: The Last Jedi',
                  desc: 'Star Wars: The Last Jedi is een Amerikaanse sciencefictionfilm uit 2017 en het achtste deel uit de Star Wars-filmfranchise. De film is geregisseerd en geschreven door Rian Johnson en speelt zich af na de gebeurtenissen in The Force Awakens. De film ging op 9 december 2017 in wereldpremière in Los Angeles.',  
              },
              {
                  id: 2,
                  image: 'http://www.picsum.photos/800/400?random',
                  title: 'Star Wars: The Force Awakens',
                  desc: 'Star Wars: The Force Awakens is het zevende deel uit de succesvolle filmfranchise Star Wars bedacht door George Lucas. De film werd geregisseerd door J.J. Abrams en geproduceerd door Lucasfilm, Walt Disney Pictures en Bad Robot Productions.',  
              },
          ],
      }
  },
}
</script>

<style lang="scss">
@import "/assets/scss/_variables.scss";

body {
  font-size: $body-font-size;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  color: #2c3e50;
}

#projects {
  .project {
    
    @media (min-width: 750px) {
      display: flex;
    }

    &:not(:last-of-type) { margin-bottom: $gutter-base; }

    &:nth-child(even) {
      flex-direction: row-reverse;
    }

    .media {
      @media (min-width: 750px) {
        flex: 0 1 auto;
      }

      img {
        display: block;
        width: 100%;
        border-radius: $border-radius-base;
      }
    }

    .content {
      @media (min-width: 750px) {
        flex: 0 0 50%;
      }

      .inner {
        padding: ($gutter-base / 2);
      }
    }
  }
}
</style>

