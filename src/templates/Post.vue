<template>
  <Layout :layout-class="'sticky'" :header-class="sticky">
    <div class="project-wrapper">
      <div class="container">
        <div class="project-header">
          <h1 class="project-title">Banana</h1>
          <div class="project-info">
            <div class="categories-container">
              <div class="categories">
                <span class="label">Categories</span
                ><span class="category">photography</span
                ><span class="category">pink</span>
              </div>
            </div>
            <div class="year-container">
              <span class="label">Year</span>
              <div>2019</div>
            </div>
          </div>
        </div>
        <div class="content">
          <p>
            The&nbsp;<strong>banana</strong>&nbsp;fruits grow from
            a&nbsp;<strong>banana</strong>&nbsp;blossom in hanging clusters,
            also called a bunch or&nbsp;<strong>banana</strong> stem. The fruits
            grow in rows called tiers or hands. There can be as many as twenty
            fruits to a hand, and as many as twenty tiers in a bunch. A bunch
            usually weighs between 30 and 50 kilograms (65 to 110 pounds).
          </p>
          <p>
            <img
              class="g-image g-image--lazy g-image--loaded"
              src="/assets/static/mike-dorner-173502-unsplash.42db587.16e7958f24c375d7bd7b08073b4ce000.jpg"
              width="2560"
              data-srcset="/assets/static/mike-dorner-173502-unsplash.82a2fbd.16e7958f24c375d7bd7b08073b4ce000.jpg 480w, /assets/static/mike-dorner-173502-unsplash.cbab2cf.16e7958f24c375d7bd7b08073b4ce000.jpg 1024w, /assets/static/mike-dorner-173502-unsplash.2665e34.16e7958f24c375d7bd7b08073b4ce000.jpg 1920w, /assets/static/mike-dorner-173502-unsplash.42db587.16e7958f24c375d7bd7b08073b4ce000.jpg 2560w"
              data-sizes="(max-width: 2560px) 100vw, 2560px"
              data-src="/assets/static/mike-dorner-173502-unsplash.42db587.16e7958f24c375d7bd7b08073b4ce000.jpg"
              srcset="
                /assets/static/mike-dorner-173502-unsplash.82a2fbd.16e7958f24c375d7bd7b08073b4ce000.jpg  480w,
                /assets/static/mike-dorner-173502-unsplash.cbab2cf.16e7958f24c375d7bd7b08073b4ce000.jpg 1024w,
                /assets/static/mike-dorner-173502-unsplash.2665e34.16e7958f24c375d7bd7b08073b4ce000.jpg 1920w,
                /assets/static/mike-dorner-173502-unsplash.42db587.16e7958f24c375d7bd7b08073b4ce000.jpg 2560w
              "
              sizes="(max-width: 2560px) 100vw, 2560px"
            /><noscript
              ><img
                class="g-image g-image--lazy g-image--loaded"
                src="/assets/static/mike-dorner-173502-unsplash.42db587.16e7958f24c375d7bd7b08073b4ce000.jpg"
                width="2560"
            /></noscript>
          </p>
        </div>
      </div>
    </div>
  </Layout>
</template>

<script>                    
export default {};
</script>

<style scoped>
.layout {
    padding: 0 !important;
}
.project-title {
  font-size: 4rem;
  margin: 0 0 4rem;
  padding: 0;
  text-align: left;
}
</style>