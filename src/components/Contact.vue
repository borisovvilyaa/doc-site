<template>
  <div
    class="contact-section wow animate__animated animate__fadeIn"
    id="contact"
  >
    <div class="container">
      <div class="row">
        <div class="col-md-4">
          <h3>Contact Dr. Gurmander Singh Kohli</h3>
        </div>
        <div class="col-md-8">
          <ul class="contact-list">
            <li>
              <i class="bi bi-telephone-fill"></i>
              Phone: 833-Regenerative Care
            </li>
            <li>
              <i class="bi bi-envelope-fill"></i>
              New Customers:
              <a href="mailto:ORDERS@RegenerativeCare.COM"
                >ORDERS@RegenerativeCare.COM</a
              >
            </li>
            <li>
              <i class="bi bi-envelope-fill"></i>
              Current Customers:
              <a href="mailto:SUPPORT@RegenerativeCare.COM"
                >SUPPORT@RegenerativeCare.COM</a
              >
            </li>
            <li>
              <i class="bi bi-envelope-fill"></i>
              Distributor Inquiries:
              <a href="mailto:DISTRIBUTOR@RegenerativeCare.COM"
                >DISTRIBUTOR@RegenerativeCare.COM</a
              >
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { WOW } from "wowjs";
import "animate.css";

export default {
  name: "ContactSection",
  mounted() {
    new WOW().init();
  },
};
</script>

<style scoped>
.contact-section {
  padding: 50px 0;
  background-color: #fff;
  color: #333;
}

h3 {
  font-size: 36px;
  font-weight: 300;
  margin-bottom: 20px;
  color: #333;
}

.contact-list {
  list-style: none;
  padding: 0;
}

.contact-list li {
  margin-bottom: 10px;
}

.contact-list i {
  margin-right: 10px;
  color: #007bff;
}

.contact-list a {
  color: #007bff;
  text-decoration: none;
  transition: color 0.3s;
}

.contact-list a:hover {
  color: #0056b3;
}

@media (max-width: 767px) {
  .row {
    flex-direction: column;
  }

  .col-md-4,
  .col-md-8 {
    width: 100%;
    margin-bottom: 20px;
  }

  h3 {
    font-size: 30px;
  }

  .contact-list {
    font-size: 14px;
  }
}
</style>
