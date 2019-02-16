<template>
  <div class="example-form">
    <FormItem 
      v-for="(item,index) in formData" 
      :key="index" 
      :formDataItem="item"
    />
    <button class="form-item__submit" @click="handleSubmit">
      Submit
    </button>
    <div class="show-area">
      <p v-for="(item,index) in formData" :key="index">
        {{item.label}} {{item.value}}
      </p>
    </div>
  </div>
</template>

<script>
import FormItem from './FormItem'

const initialState = () => { 
  return JSON.parse(
    JSON.stringify({
      formData: [
        {
          value: '',
          label: '姓名:'
        },
        {
          value: '',
          label: '電話:'
        },
        {
          value: '',
          label: '住址:'
        }
      ]
    })
  )
};

export default {
  name: "FormWithItems",
  props: {
  },
  data() {
    return initialState()
  },
  methods: {
    handleSubmit(event) {
      event.preventDefault();
      alert(`您的表單已送出: 姓名:${this.formData[0].value} 電話:${this.formData[1].value} 住址:${this.formData[2].value}`);
      Object.assign(this.$data, initialState());
    }
  },
  components:{
    FormItem
  }
};
// JSON.parse(JSON.stringify(Object))
// this.$data = initialState() 會報錯  [Vue警告]：避免替换提體根$data。請改用鑲嵌數據属性
</script>

