---
title: Private Tutoring
layout: default
has_toc: false
nav_order: 4
faqs:
  - q: "What is Jekyll?"
    a: "A static site generator."
  - q: "Can I use it with GitHub?"
    a: "Yes, via GitHub Pages."
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

{% for item in page.faqs %}
<details class="faq-item">
  <summary class="faq-question">
    {{ item.question }}
  </summary>
  <div class="faq-answer">
    <p>{{ item.answer }}</p>
  </div>
</details>
{% endfor %}