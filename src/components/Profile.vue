<template>
  <div class="profile-section container">
    <div class="row">
      <div class="col-md-6 wow animate__animated animate__fadeInUp">
        <div class="block">
          <div class="icon-container"><i class="bi bi-person-circle"></i></div>
          <div class="text-container">
            <h2>Introduction</h2>
            <p>
              <strong>Dr. Gurmander Singh Kohli</strong> is a dedicated,
              seasoned Plastic Surgeon with 38 years of experience and a
              continuing interest in cutting-edge technologies. He specializes
              in rhinoplasty and other plastic surgeries requiring precise and
              subtle skills.
            </p>
          </div>
        </div>
      </div>
      <div class="col-md-6 wow animate__animated animate__fadeInUp">
        <div class="block">
          <div class="icon-container"><i class="bi bi-briefcase"></i></div>
          <div class="text-container">
            <h2>Professional Experience</h2>
            <p>
              Formerly the Medical Director of Loma Linda University’s Surgery
              Center in Riverside and an associate professor in the Department
              of Plastic Surgery, Dr. Kohli has a strong background in aesthetic
              and reconstructive surgery, medical education, and mentoring. His
              compassion and commitment to patients are demonstrated through a
              medical mission to Malawi and six trips to Lithuania to perform
              life-changing operations and train less advantaged surgeons.
            </p>
          </div>
        </div>
      </div>
      <div class="col-md-6 wow animate__animated animate__fadeInUp">
        <div class="block">
          <div class="icon-container"><i class="bi bi-award"></i></div>
          <div class="text-container">
            <h2>Certifications and Memberships</h2>
            <ul>
              <li>Certified by the American Board of Plastic Surgery</li>
              <li>Fellow of the American College of Surgeons</li>
              <li>
                Member of the American Society of Plastic and Reconstructive
                Surgeons, Inc.
              </li>
              <li>Member of the Massachusetts Society of Plastic Surgery</li>
              <li>Member of the Lipoplasty Society of North America</li>
              <li>Member of the General Medical Council, U.K.</li>
              <li>Member of the Massachusetts Medical Society</li>
              <li>Member of the International Medical Foundation</li>
            </ul>
          </div>
        </div>
      </div>
      <div class="col-md-6 wow animate__animated animate__fadeInUp">
        <div class="block">
          <div class="icon-container"><i class="bi bi-book"></i></div>
          <div class="text-container">
            <h2>Education and Residencies</h2>
            <p>
              Dr. Kohli received his M.D. degree from the University of Glasgow
              School of Medicine, Scotland, U.K., and completed residencies at
              The Glasgow Western Infirmary, The Glasgow Royal Infirmary, The
              London Charing Cross Hospital, and Malden Hospital in Malden,
              Massachusetts. Further training includes general surgery at The
              Boston University Hospital & Medical Center (now The Boston
              Medical Center) and plastic and reconstructive surgery at The
              Boston University Hospital & Medical Center (now The Boston
              Medical Center) in Boston, Massachusetts.
            </p>
          </div>
        </div>
      </div>
      <div class="col-md-6 wow animate__animated animate__fadeInUp">
        <div class="block">
          <div class="icon-container"><i class="bi bi-calendar4-week"></i></div>
          <div class="text-container">
            <h2>Previous Appointments and Practice</h2>
            <p>
              Before relocating to California 10 years ago, Dr. Kohli lived in
              Boston for 35 years, spending 23 years in private practice. He
              served as Chief of Plastic Surgery at three Boston-area hospitals
              and was the Founder and Medical Director of “The Center for
              Plastic Surgery and Personal Development” at the Boston Regional
              Medical Center.
            </p>
          </div>
        </div>
      </div>
      <div class="col-md-6 wow animate__animated animate__fadeInUp">
        <div class="block">
          <div class="icon-container"><i class="bi bi-heart"></i></div>
          <div class="text-container">
            <h2>Specialties</h2>
            <p>
              Plastic Surgery, Reconstructive Surgery, Cosmetic Surgery,
              Rhinoplasty (Primary and Secondary), Breast Reconstruction after
              Breast Cancer Surgery, Breast Reduction for Aesthetic and
              Functional Purposes, Breast Augmentation, Body Contouring,
              Liposuction.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { WOW } from "wowjs";
import "animate.css";

export default {
  name: "ProfileSection",
  mounted() {
    new WOW().init();
  },
};
</script>

<style scoped>
.profile-section {
  padding: 60px 0;
  color: #333;
}

.row {
  display: flex;
  flex-wrap: wrap;
}
.col-md-6 {
  margin-top: 20px;
}
.block {
  display: flex;
  align-items: center;
  margin-bottom: 40px;
  padding: 20px;
  border-radius: 20px;
  box-shadow: rgba(33, 35, 38, 0.1) 0px 10px 10px -10px;
  background-color: #f9f9f9;
  height: 100%;
}

.icon-container {
  flex: 0 0 50px; /* Ограничение размера иконки */
  margin-right: 20px;
}

.icon-container i {
  font-size: 3rem; /* Увеличение размера иконки */
  color: #00aaff; /* Цвет иконки */
}

.text-container {
  flex-grow: 1;
}

.block h2 {
  font-size: 2rem;
  font-weight: 700;
  color: #2c3e50;
  margin-bottom: 15px;
  border-bottom: 2px solid #054052;
  padding-bottom: 5px;
}

.block p {
  font-size: 18px;
  line-height: 1.8;
  font-weight: 100;
  color: #4a4a4a;
}

.block ul {
  list-style: square;
  padding-left: 20px;
}

.block ul li {
  margin-bottom: 12px;
  font-size: 16px;
  color: #333;
}

@media (max-width: 767px) {
  .block {
    flex-direction: column;
    align-items: flex-start;
  }

  .block h2 {
    font-size: 24px;
  }

  .block p {
    font-size: 16px;
  }

  .block ul li {
    font-size: 14px;
  }

  .icon-container {
    margin-bottom: 10px;
  }
}
</style>
