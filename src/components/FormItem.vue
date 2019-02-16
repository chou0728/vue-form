<template>
  <div class="form-item">
    <label>{{formDataItem.label}}</label>
    <input type="text" class="form-item__input" v-model="formDataItem.value"/>
  </div>
</template>

<script>
export default {
  name: "FormItem",
  props: {
    formDataItem: {
      type: Object
    }
  },
  data() {
    return {}
  },
  methods: {}
};
</script>

