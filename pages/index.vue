<template>
  <section>
    <div style="width: 100px; height:80px;background-color:lightgrey;" @click="di">
      click here
    </div>
    <form v-if="displayform"
      method="POST"
      action="/thanks"
      name="privacy"
      data-netlify="true"
      netlify-honeypot="bot-field"
    >
      <input type="hidden" name="form-name" value="privacy" />
      <label>sometext: <input type="text" name="letext" v-model="text"/></label>
      <label>email: <input type="email" name="email" v-model="email"/></label>
      <button type="submit">u n s u b s c r i b e !</button>
    </form>
  </section>
</template>

<script>
export default {  
  data: () => ({
    displayform: false,
    text: "",
    email: ""
  }),
  methods: {
    di() {
      this.displayform = !this.displayform
    }
    // submit(){
    //   fetch('/',{
    //     method: 'post',
    //     body: {
    //       email: encodeURIComponent(this.email),
    //       text: encodeURIComponent(this.text),
    //     }
    //   })
    //   .then(res => console.log(res))
    //   .catch(err=> console.log(err))
    // }
  }

}
</script>

<style></style>
