<template>
  <div>
    <div class="layout" :class="layoutClass ? layoutClass : null">
      <header class="header" :class="headerClass ? headerClass : null">
        <div class="container">
          <div class="left">
            <g-link to="/" class="home-link active">
              <img
                src="https://gridsome-forestry.netlify.app/assets/img/logo.332701b7.svg"
                alt="Jason Huang"
                class="logo"
              />
            </g-link>
          </div>
          <nav class="nav right">
            <a href="/journal" class="nav__link">Journal</a
            ><a href="/contact" class="nav__link">Say Hi!</a>
          </nav>
        </div>
      </header>
      <slot />
      <footer class="footer">
        <div class="container"><span>Copyright © 2021</span></div>
      </footer>
    </div>

  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<script>
export default {
  props: ['layoutClass', 'headerClass']
}
</script>

<style>
/* body {
  --color-base: #fff;
  --color-base-1: #f3f3f3;
  --color-contrast: #000;
  --color-contrast-1: #2b2b2b;
  font-family: -apple-system, system-ui, BlinkMacSystemFont, Segoe UI, Roboto,
    Helvetica Neue, Arial, sans-serif;
  margin: 0;
  padding: 0;
  font-size: 16px;
  background: var(--color-base);
  color: var(--color-contrast);
  transition: background 0.5s ease;
} */

.nav > * {
    font-size: .9rem;
    font-weight: 600;
    text-decoration: none;
    margin-top: 4px;
    margin-right: 3rem;
    padding-bottom: 4px;
    border-bottom: 1px solid;
    border-color: transparent;
    transition: border .15s
}

.nav > :last-of-type {
    margin: 0
}

.nav > .active, .nav > :hover {
    border-color: inherit
}

.footer {
    font-size: .8rem;
    padding: 6rem 0
}

</style>
