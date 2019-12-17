<template>
    <div id="projects">
        <div v-for="project in projects" :key="project.id" class="project">
            <picture class="media">
                <img v-bind:src="'' + project.image">
            </picture>
            <div class="content">
                <div class="inner">
                    <h1 class="title">{{ project.title }}</h1>
                    <p class="text">{{ project.desc }}</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
  export default {
    name: 'projects',
    props: {
        projects: Array,
    },
  }
</script>

<style scoped></style>