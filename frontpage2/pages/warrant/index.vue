<template>
  <NewHeader />
  <!-- First Divider -->
  <div class="divider"></div>
  <div class="title">
    <h1 class="first-title">Wanted</h1>

    <h3 class="second-title">Alive only</h3>
  </div>
  <!-- Second Divider -->
  <div class="divider"></div>

  <!-- Third Divider -->
  <div class="divider"></div>
  <div class="image">
    <img src="~/assets/dennislee.jpg" />
  </div>
  <div class="warrant-detail">
    <p>Level 5</p>
    <p>$5,000</p>
    <p>
      Possession of Too Many Puns: Charged for causing groans in public with an
      excessive use of puns.
    </p>
    <p>
      Grand Theft Cookie: Accused of stealthily stealing cookies from the cookie
      jar.
    </p>
    <P
      >Reckless Walking: For dangerously walking with laces untied, posing a
      tripping hazard.
    </P>
  </div>

  <!-- fourth Divider -->
  <div class="divider"></div>

  <!-- fivth Divider -->
  <div class="divider"></div>
  <div class="contact">
    <button class="send" @click="sendEmail">Contact:pcleegood@gmail.com</button>
  </div>
  <div class="warrant-detail">
    <p>All bounty payments and full responsibility are by B.Robert.OKX.</p>
  </div>
</template>

<script>
export default {
  methods: {
    sendEmail() {
      const email = "pcleegood@gmail.com";
      const subject = encodeURIComponent("Offer Proposal");
      const body = encodeURIComponent("I want to offer... about this man.");

      const mailtoLink = `mailto:${email}?subject=${subject}&body=${body}`;
      window.open(mailtoLink);
    },
  },
};
</script>
<style>
h1,
h3,
p,
button {
  font-family: "Old Newspaper Types", serif;
}

.divider {
  height: 2px;
  background-color: #ccc; /* Example color */
  margin: 20px 0;
}

.title,
.warrant-detail,
.contact {
  text-align: center;
  margin: 10px;
}

.image {
  display: flex;
  justify-content: center; /* Centers the child horizontally */
  align-items: center; /* Centers the child vertically */
  margin: 20px 0;
}

img {
  max-width: 50%; /* Ensures the image is responsive */
  height: auto; /* Maintains aspect ratio */
}
.send {
  text-decoration: underline;
}
</style>
