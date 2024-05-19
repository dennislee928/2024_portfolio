<template>
  <div :key="$route.fullPath">
    <Header />
    <div class="page-title">
      <h1>Contact me</h1>
    </div>
    <!-- Your Contacts content here -->
    <div class="input-container">
      <input
        class="email"
        type="text"
        v-model="email"
        placeholder="Your email"
      />
      <input class="name" type="text" v-model="name" placeholder="Your name" />
      <input
        class="content"
        type="text"
        v-model="cotent"
        placeholder="Your contact content"
      />
      <button @click="sendContactEmail">Send contact</button>
    </div>
    <Footer />
  </div>
</template>

<script>
import { ref } from "vue";
import emailjs from "emailjs-com"; // If installed via npm
//
export default {
  setup() {
    const email = ref("");
    const name = ref("");
    const content = ref("");

    const sendContactEmail = async () => {
      if (name.value && email.value && content.value) {
        const templateParams = {
          from_name: "https://2024portfolio-ciu.pages.dev/", // You can set a specific sender name or use an appropriate variable
          to_name: email.value, // Assuming you want to address the recipient directly
          message: `Contact content ${content.value} from ${name.value}. It expires in 10 minutes.`, // The OTP message
          to_email: email.value, // This might not be necessary if your EmailJS service handles the recipient directly from 'to_name'
        };

        try {
          await emailjs.send(
            "service_1y7pxij",
            "template_v5v99xe",
            templateParams,
            "rtofkHKZrBzmgJ_2T"
          );
          alert("sending success!");
        } catch (error) {
          errorMessage.value = "Failed to send OTP email.";
          console.error(error);
        }
      } else {
        alert("please enter all required input fileds!");
      }
    };
    return {
      email,
      name,
      content,
      sendContactEmail,
    };
  },
};
</script>
<style>
.page-title {
  align-items: center;
  align-content: center;
  text-align: center;
}
.input-container {
  border-style: solid;
  border-width: 1px;
  border-radius: 1.5cap;
  align-items: center;
  align-self: center;
  text-align: center;
  display: flex;
  flex-direction: column;
  width: 30%;
  justify-content: center;
  margin-left: auto;
  margin-right: auto;
  margin-bottom: 150px;
}
.name {
  width: fit-content;
  margin: 5px;
}
.email {
  width: fit-content;
  margin: 5px;
}
.content {
  width: fit-content;
  height: 150px;
  margin: 5px;
}
</style>
