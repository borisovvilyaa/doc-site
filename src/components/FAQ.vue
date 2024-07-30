<template>
  <div class="accordion-container" id="FAQ">
    <div class="accordion">
      <div v-for="(faq, index) in faqs" :key="index" class="accordion-item">
        <div class="accordion-header" @click="toggleAccordion(index)">
          {{ faq.question }}
          <span
            class="accordion-icon"
            :class="{ 'rotate-icon': faq.open }"
          ></span>
        </div>
        <div class="accordion-body" :class="{ show: faq.open }">
          {{ faq.answer }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "FAQSection",
  data() {
    return {
      faqs: [
        {
          question: "What are the benefits of Amniotic Membrane Grafts?",
          answer:
            "Amniotic Membrane Grafts offer several benefits including enhanced wound healing, reduced inflammation, and a natural scaffold for new tissue growth. These grafts are particularly effective for chronic and complex wounds.",
          open: true,
        },
        {
          question: "How is Amniotic Wound Care administered?",
          answer:
            "Amniotic Wound Care is administered by applying amniotic membrane grafts directly to the wound. The procedure is performed by certified wound care professionals who ensure the proper application and follow-up care.",
          open: false,
        },
        {
          question: "What conditions can benefit from regenerative therapy?",
          answer:
            "Regenerative therapy can benefit a range of conditions including diabetic foot ulcers, venous leg ulcers, pressure ulcers, surgical wounds, burns, and other chronic or non-healing wounds.",
          open: false,
        },
        {
          question: "Who can be treated with regenerative care?",
          answer:
            "Patients with chronic or non-healing wounds that have not improved with standard treatments are eligible for regenerative care. Eligibility is assessed based on the wound's condition and the patient’s overall health.",
          open: false,
        },
      ],
    };
  },
  methods: {
    toggleAccordion(index) {
      this.faqs.forEach((faq, i) => {
        if (i === index) {
          faq.open = !faq.open;
        } else {
          faq.open = false;
        }
      });
    },
  },
};
</script>
<style scoped>
.accordion-container {
  width: 100%;
  margin: 0 auto;
  padding-bottom: 50px;
  padding-top: 50px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.accordion {
  width: 100%;
}

.accordion-item {
  background-color: #ffffff; /* White background */
  margin-bottom: 10px;
  border: none;
  border-radius: 5px;
}

.accordion-header {
  font-weight: 100;
  border-bottom: 1px solid #e0e0e0; /* Light gray border */
  color: #333333; /* Dark text for better readability */
  padding: 10px;
  cursor: pointer;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  font-size: 2rem;
}

.accordion-header:hover {
}

.accordion-body {
  padding: 10px;
  font-weight: 100;
  color: #333333; /* Dark text for better readability */
  display: none;
}

.accordion-body.show {
  display: block;
}

.accordion-icon {
  float: right;
  margin-left: 10px;
  width: 0;
  height: 0;
  border-left: 6px solid transparent;
  border-right: 6px solid transparent;
  border-top: 6px solid #333333; /* Dark icon for better visibility */
  transition: transform 0.3s ease;
}

.rotate-icon {
  transform: rotate(180deg);
}

/* Media queries for mobile adaptation */
@media (max-width: 600px) {
  .accordion-header {
    font-size: 1.5rem;
    white-space: normal;
  }

  .accordion-body {
    font-size: 1rem;
  }
}
</style>
