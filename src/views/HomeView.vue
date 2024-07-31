<template>
  <div class="home container wow animate__animated animate__fadeIn">
    <div
      class="home-content d-flex align-items-center flex-column flex-md-row"
      id="home"
    >
      <div class="col image-container">
        <img src="@/assets/Home/kohli.png" alt="Dr. Gurmander Singh Kohli" />
      </div>
      <div class="col text-container">
        <h1 class="title">Dr. Gurmander Singh Kohli</h1>
        <p class="description fw-light">
          A seasoned plastic surgeon with 38 years of experience, specializes in
          rhinoplasty and precise plastic surgeries. Formerly Medical Director
          at Loma Linda University’s Surgery Center and associate professor in
          Plastic Surgery, he is certified by the American Board of Plastic
          Surgery and is a fellow of the American College of Surgeons.
        </p>
        <a href="#contact" class="btn contact-btn">Contact Dr. Kohli</a>
      </div>
    </div>
    <Profile />
    <FAQ />
    <Contact />
  </div>
</template>

<script>
import Contact from "@/components/Contact.vue";
import Profile from "@/components/Profile.vue";
import FAQ from "@/components/FAQ.vue";
import { WOW } from "wowjs";
import "animate.css";

export default {
  name: "HomeView",
  components: {
    Contact,
    Profile,
    FAQ,
  },
  mounted() {
    new WOW().init();
  },
};
</script>

<style scoped>
.home {
  padding-top: 100px;
  font-size: 1.2rem;
  /* Ensure full-width fade-in effect */
}

.home-content {
  border-radius: 8px;
  overflow: hidden;
  padding: 40px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.image-container img {
  max-width: 100%;
  border-radius: 8px;
}

.text-container {
  padding: 20px;
  text-align: center;
}

.title {
  font-size: 2.5rem;
  font-weight: 700;
  color: #333;
  margin-bottom: 20px;
}

.description {
  font-size: 1.1rem;
  color: #555;
  margin-bottom: 20px;
}

.contact-btn {
  background-color: #054052;
  color: #fff;
  padding: 10px 20px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.3s;
}

.contact-btn:hover {
  color: #fff;
  background-color: #085870;
}

/* Media Queries */
@media (min-width: 768px) {
  .home-content {
    flex-direction: row;
  }

  .text-container {
    text-align: left;
    padding-left: 20px;
  }
}

@media (max-width: 576px) {
  .title {
    font-size: 2rem;
  }

  .description {
    font-size: 1rem;
  }

  .contact-btn {
    padding: 8px 16px;
  }
}
</style>
