<template>
  <Layout>
    <div  class="container">
      <div  class="contact-header">
        <h1  class="contact-title">Say hi!</h1>
        <p >
          Leave me a note with any questions you might have, I'll get back to you
          as soon as possible.
        </p>
      </div>
      <form  name="contact" class="contact-form">
        <div  class="sender-info">
          <div >
            <label  for="name" class="label">Your name</label
            ><input  type="text" name="name" />
          </div>
          <div >
            <label  for="email" class="label">Your email</label
            ><input  type="email" name="email" />
          </div>
        </div>
        <div  class="message">
          <label  for="message" class="label">Message</label
          ><textarea  name="message"></textarea>
        </div>
        <button  class="button">Submit form</button>
      </form>
    </div>

  </Layout>
</template>

<script>
export default {};
</script>

<style>
</style>