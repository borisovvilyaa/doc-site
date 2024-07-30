<template>
  <div class="profile-section container">
    <div class="row">
      <div class="col-md-12">
        <div class="block introduction">
          <h2>Introduction</h2>
          <p>
            <strong>Dr. Gurmander Singh Kohli</strong> is a dedicated, seasoned
            Plastic Surgeon with 38 years of experience and a continuing
            interest in cutting-edge technologies. He specializes in rhinoplasty
            and other plastic surgeries requiring precise and subtle skills.
          </p>
        </div>
        <div class="block professional-experience">
          <h2>Professional Experience</h2>
          <p>
            Formerly the Medical Director of Loma Linda University’s Surgery
            Center in Riverside and an associate professor in the Department of
            Plastic Surgery, Dr. Kohli has a strong background in aesthetic and
            reconstructive surgery, medical education, and mentoring. His
            compassion and commitment to patients are demonstrated through a
            medical mission to Malawi and six trips to Lithuania to perform
            life-changing operations and train less advantaged surgeons.
          </p>
        </div>
        <div class="block certifications-memberships">
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
        <div class="block education-residencies">
          <h2>Education and Residencies</h2>
          <p>
            Dr. Kohli received his M.D. degree from the University of Glasgow
            School of Medicine, Scotland, U.K., and completed residencies at The
            Glasgow Western Infirmary, The Glasgow Royal Infirmary, The London
            Charing Cross Hospital, and Malden Hospital in Malden,
            Massachusetts. Further training includes general surgery at The
            Boston University Hospital & Medical Center (now The Boston Medical
            Center) and plastic and reconstructive surgery at The Boston
            University Hospital & Medical Center (now The Boston Medical Center)
            in Boston, Massachusetts.
          </p>
        </div>
        <div class="block previous-appointments">
          <h2>Previous Appointments and Practice</h2>
          <p>
            Before relocating to California 10 years ago, Dr. Kohli lived in
            Boston for 35 years, spending 23 years in private practice. He
            served as Chief of Plastic Surgery at three Boston-area hospitals
            and was the Founder and Medical Director of “The Center for Plastic
            Surgery and Personal Development” at the Boston Regional Medical
            Center.
          </p>
        </div>
        <div class="block specialties">
          <h2>Specialties</h2>
          <p>
            Plastic Surgery, Reconstructive Surgery, Cosmetic Surgery,
            Rhinoplasty (Primary and Secondary), Breast Reconstruction after
            Breast Cancer Surgery, Breast Reduction for Aesthetic and Functional
            Purposes, Breast Augmentation, Body Contouring, Liposuction.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProfileSection",
};
</script>

<style scoped>
.profile-section {
  padding: 60px 0;
  color: #333;
}

.block {
  margin-bottom: 40px;
  padding: 20px;
  border-radius: 8px;
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
  strong {
    font-weight: bold;
  }
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

/* Responsive styles */
@media (max-width: 767px) {
  .block h2 {
    font-size: 24px;
  }

  .block p {
    font-size: 16px;
  }

  .block ul li {
    font-size: 14px;
  }
}
</style>
