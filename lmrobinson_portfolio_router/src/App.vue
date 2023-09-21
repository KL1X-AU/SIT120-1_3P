<template>
  <router-view/>
</template>

<style>
/* Mobile Screen */
body {
  margin:0;
  height:100vh;
}

.grid-container {
  width: 100%;
  height: 100%;
  display: grid;
  grid-template-columns: 1fr 40vw 45vw;
  grid-template-rows: auto auto auto;
}

#header {
  grid-column-start: 1;
  grid-column-end: 4;
  grid-row-start:1;
  grid-row-end:1;
}

#contactbar {
  grid-column-start: 1;
  grid-column-end: 4;
  grid-row-start: 4;
  grid-row-end: 4;
  height: 100%;
  display: flex;
  justify-content: center;
  background-color: #313131;
}

#navbar {
  grid-column-start: 1;
  grid-column-end: 4;
  grid-row-start: 2;
  grid-row-end: 2;
  background-color: #313131;
}

#content {
  grid-column-start: 1;
  grid-column-end: 4;
  grid-row-start: 3;
  grid-row-end: 3;
}
/* Tablet 400px - 700px */
@media screen and (min-width: 400px) {
  body {
    margin:0;
    height:100vh;
  }

  .grid-container {
    width: 100%;
    height: 100%;
    display: grid;
    grid-template-columns: 1fr 40vw 45vw;
    grid-template-rows: auto auto auto;
  }

  #header {
    grid-column-start: 1;
    grid-column-end: 4;
    grid-row-start:1;
    grid-row-end:1;
  }

  #contactbar {
    grid-column-start: 1;
    grid-column-end: 4;
    grid-row-start: 3;
    grid-row-end: 4;
    height: 100%;
  }

  #navbar {
    grid-column-start: 1;
    grid-column-end: 2;
    grid-row-start: 2;
    grid-row-end: 2;
  }

  #content {
    grid-column-start: 2;
    grid-column-end: 4;
    grid-row-start: 2;
    grid-row-end: 2;
  }
}


/* Bigger Screens */
@media screen and (min-width: 700px) {
  body {
    margin:0;
    height:100vh;
  }

  .grid-container {
    width: 100%;
    height: 100%;
    display: grid;
    grid-template-columns: 1fr 40vw 45vw 5vw;
    grid-template-rows: auto auto auto;
  }

  #header {
    grid-column-start: 1;
    grid-column-end: 5;
    grid-row-start:1;
    grid-row-end:1;
  }

  #contactbar {
    grid-column-start: 4;
    grid-column-end: 5;
    grid-row-start: 2;
    grid-row-end: 3;
    height: 100%;
  }

  #navbar {
    grid-column-start: 1;
    grid-column-end: 2;
    grid-row-start: 2;
    grid-row-end: 2;
  }

  #content {
    grid-column-start: 2;
    grid-column-end: 4;
    grid-row-start: 2;
    grid-row-end: 2;
  }
}
</style>
