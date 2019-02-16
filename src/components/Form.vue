<template>
  <div class="example-form">
    <div class="form-item">
      <label>姓名</label>
      <input type="text" class="form-item__input" v-model="userName"/>
    </div>
    <div class="form-item">
      <label>電話</label>
      <input type="text" class="form-item__input" v-model="phone"/>
    </div>
    <div class="form-item">
      <label>地址</label>
      <input type="text" class="form-item__input" v-model="address"/>
    </div>
    <button class="form-item__submit" @click="handleSubmit">Submit</button>
    <div class="show-area">
      <p>姓名: {{userName}}</p>
      <p>電話: {{phone}}</p>
      <p>地址: {{address}}</p>
    </div>
  </div>
</template>

<script>
const initialState = () => { 
  return JSON.parse(
    JSON.stringify({
      userName: '',
      phone: '',
      address: ''
    })
  )
};

export default {
  name: "Form",
  props: {
  },
  data() {
    return initialState()
  },
  methods: {
    handleSubmit(event) {
      event.preventDefault();
      alert(`您的表單已送出: 姓名:${this.userName} 電話:${this.phone} 住址:${this.address}`);
      Object.assign(this.$data, initialState());
    }
  }
};
// JSON.parse(JSON.stringify(Object))
// this.$data = initialState() 會報錯  [Vue警告]：避免替换提體根$data。請改用鑲嵌數據属性
</script>

