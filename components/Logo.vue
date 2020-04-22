<template>
   <img class="NuxtLogo spinner" src="~/assets/sleep.png">
  <!-- <svg class="NuxtLogo" width="245" height="180" viewBox="0 0 452 342" xmlns="http://www.w3.org/2000/svg">
    <g fill="none" fill-rule="evenodd">
      <path
        d="M139 330l-1-2c-2-4-2-8-1-13H29L189 31l67 121 22-16-67-121c-1-2-9-14-22-14-6 0-15 2-22 15L5 303c-1 3-8 16-2 27 4 6 10 12 24 12h136c-14 0-21-6-24-12z"
        fill="#00C58E"
      />
      <path
        d="M447 304L317 70c-2-2-9-15-22-15-6 0-15 3-22 15l-17 28v54l39-67 129 230h-49a23 23 0 0 1-2 14l-1 1c-6 11-21 12-23 12h76c3 0 17-1 24-12 3-5 5-14-2-26z"
        fill="#108775"
      />
      <path
        d="M376 330v-1l1-2c1-4 2-8 1-12l-4-12-102-178-15-27h-1l-15 27-102 178-4 12a24 24 0 0 0 2 15c4 6 10 12 24 12h190c3 0 18-1 25-12zM256 152l93 163H163l93-163z"
        fill="#2F495E"
        fill-rule="nonzero"
      />
    </g>
  </svg> -->
</template>
<style>
.NuxtLogo {
  animation: 1s appear;
  margin: auto;
}

.rotate {
  animation: rotation 4s infinite linear;
}

@keyframes appear {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}

.spinner {
    display: block;
    /* margin: 50px;
    height: 28px;
    width: 28px;     */
    -webkit-animation: rotate 0.8s infinite linear !important;
    -moz-animation: rotate .8s infinite linear !important;
    animation: rotate 39.8s infinite linear !important;
    /* border: 8px solid grey;
    border-right-color: transparent;
    border-radius: 50%; */
    position:relative;
}
@-webkit-keyframes rotate {
    0%    { transform: rotate(0deg); }
    100%  { transform: rotate(360deg); }
}
@-moz-keyframes rotate {
    0%    { transform: rotate(0deg); }
    100%  { transform: rotate(360deg); }
}
@keyframes rotate {
    0%    { transform: rotate(0deg); }
    100%  { transform: rotate(360deg); }
}


</style>
