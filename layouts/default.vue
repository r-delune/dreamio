<template>
    <div>
        <nav
          class="top-navbar flex flex-row align-center p-2 fixed w-full"
          style="z-index: 9001;"
          >
          <!-- <div class="flex-grow">
            
                <a
                  href="https://threejs.org/"
                  target="_blank"
                  class="button--green"
                >
                Some cool shit here
              </a>
            
          </div> -->
          <!-- <div class="flex-grow">
            <router-link :to="{ name: 'About' }">
              About
            </router-link>
          </div>
          <div class="flex-grow">
            <router-link :to="{ name: 'Contact' }">
              Contact
            </router-link>
          </div> -->
        </nav>
      <nuxt />
    </div>
</template>
<style>
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}
</style>
