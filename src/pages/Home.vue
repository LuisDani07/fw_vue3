<template>
  <f7-page>
    <f7-navbar>
      <f7-nav-title>My App</f7-nav-title>
    </f7-navbar>

    <f7-block strong>
      <p>
        Input value is <b>{{ value }}</b>
      </p>
    </f7-block>
    <f7-list>
      <f7-list-input
        label="Item label"
        placeholder="Add value"
        type="text"
        v-model:value="value"
      />
    </f7-list>
  </f7-page>
</template>
<script>
export default {
  data() {
    return {
      value: "foo",
    };
  },
};
</script>