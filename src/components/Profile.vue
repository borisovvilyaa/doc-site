<template>
  <div class="profile-section container" id="about">
    <div class="row">
      <div
        class="col-md-6 wow animate__animated animate__fadeInUp"
        v-for="(section, index) in sections"
        :key="index"
      >
        <div class="block">
          <div class="icon-container"><i :class="section.icon"></i></div>
          <div class="text-container">
            <h2>{{ section.title }}</h2>
            <div v-if="section.content">
              <p v-html="section.content"></p>
            </div>
            <ul v-else>
              <li v-for="(item, idx) in section.list" :key="idx">{{ item }}</li>
            </ul>
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
  data() {
    return {
      sections: [
        {
          icon: "bi bi-person-circle",
          title: "Introduction",
          content: `
            <strong>Dr. Gurmander Singh Kohli</strong> is a dedicated,
            seasoned Plastic Surgeon with 38 years of experience and a
            continuing interest in cutting-edge technologies. He specializes
            in rhinoplasty and other plastic surgeries requiring precise and
            subtle skills.
          `,
        },
        {
          icon: "bi bi-briefcase",
          title: "Professional Experience",
          content: `
            Formerly the Medical Director of Loma Linda University’s Surgery
            Center in Riverside and an associate professor in the Department
            of Plastic Surgery, Dr. Kohli has a strong background in aesthetic
            and reconstructive surgery, medical education, and mentoring. His
            compassion and commitment to patients are demonstrated through a
            medical mission to Malawi and six trips to Lithuania to perform
            life-changing operations and train less advantaged surgeons.
          `,
        },
        {
          icon: "bi bi-award",
          title: "Certifications and Memberships",
          list: [
            "Certified by the American Board of Plastic Surgery",
            "Fellow of the American College of Surgeons",
            "Member of the American Society of Plastic and Reconstructive Surgeons, Inc.",
            "Member of the Massachusetts Society of Plastic Surgery",
            "Member of the Lipoplasty Society of North America",
            "Member of the General Medical Council, U.K.",
            "Member of the Massachusetts Medical Society",
            "Member of the International Medical Foundation",
          ],
        },
        {
          icon: "bi bi-book",
          title: "Education and Residencies",
          content: `
            Dr. Kohli received his M.D. degree from the University of Glasgow
            School of Medicine, Scotland, U.K., and completed residencies at
            The Glasgow Western Infirmary, The Glasgow Royal Infirmary, The
            London Charing Cross Hospital, and Malden Hospital in Malden,
            Massachusetts. Further training includes general surgery at The
            Boston University Hospital & Medical Center (now The Boston
            Medical Center) and plastic and reconstructive surgery at The
            Boston University Hospital & Medical Center (now The Boston
            Medical Center) in Boston, Massachusetts.
          `,
        },
        {
          icon: "bi bi-calendar4-week",
          title: "Previous Appointments and Practice",
          content: `
            Before relocating to California 10 years ago, Dr. Kohli lived in
            Boston for 35 years, spending 23 years in private practice. He
            served as Chief of Plastic Surgery at three Boston-area hospitals
            and was the Founder and Medical Director of “The Center for
            Plastic Surgery and Personal Development” at the Boston Regional
            Medical Center.
          `,
        },
        {
          icon: "bi bi-heart",
          title: "Specialties",
          content: `
            Plastic Surgery, Reconstructive Surgery, Cosmetic Surgery,
            Rhinoplasty (Primary and Secondary), Breast Reconstruction after
            Breast Cancer Surgery, Breast Reduction for Aesthetic and
            Functional Purposes, Breast Augmentation, Body Contouring,
            Liposuction.
          `,
        },
      ],
    };
  },
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
