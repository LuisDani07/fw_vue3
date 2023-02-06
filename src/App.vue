<template>
  <f7-app v-bind="f7params">
    <f7-panel left reveal theme-dark>
      <f7-view>
        <f7-page>
          <f7-block>
            <p>Panel Left</p>
          </f7-block>
        </f7-page>
      </f7-view>
    </f7-panel>

    <f7-panel right cover themeDark>
      <f7-view>
        <f7-page>
          <f7-block>
            <p>Panel Right</p>
          </f7-block>
        </f7-page>
      </f7-view>
    </f7-panel>

    <f7-view main url="/" />
  </f7-app>
</template>

<script>
import PageHome from "./pages/Home.vue";
import PageAbout from "./pages/About.vue";
import PageNotFound from "./pages/404.vue";

const f7params = {
  id: "io.framework7.testapp", // App bundle ID
  name: "Framework7", // App name
  theme: "auto", // Automatic theme detection
  // App routes
  routes: [
    {
      path: "/",
      component: PageHome,
    },
    {
      path: "/about/",
      component: PageAbout,
    },
    {
      path: "(.*)",
      component: PageNotFound,
    },
  ],
};
export default {
  data() {
    return {
      f7params,
    };
  },
};
</script>
