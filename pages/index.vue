<template>
  <section>
    <form
      action="POST"
      name="privacy"
      data-netlify="true"
      netlify-honeypot="bot-field"
      @submit="submit"
    >
      <label>sometext: <input type="text" name="letext" v-model="text"/></label>
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
    submit(){
      fetch('/',{
        method: 'post',
        body: {
          text: encodeURIComponent(this.text)
        }
      })
      .then(res => console.log(res))
      .catch(err=> console.log(err))
    }
  }

}
</script>

<style></style>
