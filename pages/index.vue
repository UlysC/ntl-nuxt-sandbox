<template>
  <section>
    <form
      method="POST"
      action="/thanks"
      name="privacy"
      data-netlify="true"
      netlify-honeypot="bot-field"
    >
      <label>sometext: <input type="text" name="letext" v-model="text"/></label>
      <label>email: <input type="email" name="email" v-model="email"/></label>
      <button type="submit">u n s u b s c r i b e</button>
    </form>
  </section>
</template>

<script>
export default {  

  data: () => ({
    text: ""
  }),
  methods: {
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
