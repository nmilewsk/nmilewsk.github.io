---
title: Private Tutoring
layout: default
has_toc: false
nav_order: 4
faqs:
  - q: "What are your rates?"
    a: "I'm extremely flexible, especially depending on needs of the student, but I will generally start at $40/hr."
  - q: "Which subjects do you tutor?"
    a: "I specialize in tutoring mathematics of any level up through the undergraduate level. For primary/secondary education, this includes, but is not limited to, pre-algebra, algebra I, geometry, algebra II, pre-calculus, statistics, and AP calculus. As for college math courses, I have taken the following courses and can tutor in any of them: calculus 1-3, differential equations, discrete, linear algebra, abstract algebra, intro to number theory, euclidean geometry, topology, real analysis, measure theory, combinatorics, and set theory. In addition to the listed math courses, I can tutor in physics and chemistry."
  - q: "What ages can you work with?"
    a: "I have worked with all ages, from pre-school aged children up to college students."
  - q: "How long are your sessions?"
    a: "Generally they can be as long/short as is needed. On average though, they are typically an hour long."
  - q: "What form of payments do you accept?"
    a: "PayPal, Venmo, CashApp, Zelle, and Cash."
  - q: "Where are your sessions conducted?"
    a: "Wherever works best! If local, I can commute to a preferred spot in person. However I can also do remote tutoring over zoom!"
  - q: "How can I schedule a session?"
    a: "Reach out to me using the form above and I'll get back to you ASAP!"
---
<style>
  .main { max-width: 100% !important; } 
</style>

<div class="side-by-side">
  <div class="text-content">
    <div class ="content-card">
      <p> I have vast experience working both in education and in the world of mathematics, having tutored a number of students in fields ranging from grade school math up to differential equations and beyond. I aim to improve not just grades but the understanding of the content and its underlying logic. I always adapt my lessons based on the needs of my students. If you have any inquiries/questions, please fill out the form below to reach out to me! </p>
    </div>
    <br>
    <form
      action="https://formspree.io/f/xreodnnl"
      method="POST"
      class="fs-form"
      target="_top"
    >
      <div class="fs-field">
        <label class="fs-label" for="name">Name:</label>
        <input class="fs-input" id="name" name="name" required />
      </div>
      <div class="fs-field">
        <label class="fs-label" for="email">Email:</label>
        <input class="fs-input" id="email" name="email" required />
      </div>
      <div class="fs-field">
        <label class="fs-label" for="message">Message:</label>
        <textarea
          class="fs-textarea"
          id="message"
          name="message"
          required
        ></textarea>
      </div>
      <div class="fs-button-group">
        <button class="fs-button" type="submit">Submit</button>
      </div>
    </form>
  </div>
  <img src="{{ site.baseurl }}/assets/images/posterPresentation.jpeg" alt="poster_presentation">
</div>

## FAQ

{% for item in page.faqs %}
<details class="faq-container">
  <summary class="faq-button">
    {{ item.q }}
  </summary>
  <div class="faq-answer">
    <p>{{ item.a }}</p>
  </div>
</details>
{% endfor %}

<script>
  // Select all FAQ containers
  const details = document.querySelectorAll('details.faq-container');

  details.forEach((targetDetail) => {
    targetDetail.addEventListener('toggle', (event) => {
      // Only scroll if the container was just opened
      if (targetDetail.open) {
        // Scroll to the top of the clicked question
        targetDetail.scrollIntoView({
          behavior: 'smooth', // Smooth animation
          block: 'start'      // Align the top of the element to the top of the screen
        });
      }
    });
  });
</script>