<template>
  <div class="projects">
    <div class="project-image-holder">
      <div class="project-image" />
    </div>
    <div class="project-content">
      <h1 class="title">Projects</h1>
      <h2 class="project-title">{{ 'Azerion' }}</h2>
      <div class="project-title-line"></div>
      <p class="project-description">Lorem Ipsum</p>
      <a href="#" class="btn">View Website</a>
    </div>
  </div>
</template>

<style lang="scss">
$dark: #313131;
$darker: #2c2c2c;
$theme: #ff9900;
$light: #e1e1e1;

$desktop-padding: 82px;
$tablet-padding: 82px;
$mobile-padding: 82px;

.projects {
  min-height: 650px;
  height: 50vh;
  display: flex;
}
.project-image-holder {
  transform: translate(-$desktop-padding, 0);
  flex: 1;
  position: relative;
  .project-image {
    background: $theme;
    position: absolute;
    right: 0;
    top: 25px;
    width: calc(50vw + 300px);
    height: calc(50vw + 300px);
    border-radius: 50%;
    background-size: auto 50%;
    background-position: 100% 0;
    background-repeat: no-repeat;
    background-image: url('https://via.placeholder.com/300x200?text=Placeholder 3:2');
  }
}
.project-content {
  flex: 0 0 50%;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  .project-description {
    padding: 1em 0;
  }
  .project-title-line {
    height: 8px;
    border-radius: 4px;
    width: 300px;
    background: $theme;
  }
  .title {
    color: $theme;
  }
}
</style>
