---
layout: page
title: Contact
permalink: /contact/
description: Tell us what you need and we'll follow up directly.
---

<div class="page-heading">
  <h1>Start a conversation</h1>
  <p class="page-heading__sub">Tell us what you need and we'll follow up directly.</p>
</div>

<section class="section--tight">
  <form action="https://api.web3forms.com/submit" method="POST">
    <input type="hidden" name="access_key" value="002ec953-d28c-4382-a8ee-29ad289d5723">
    <input type="hidden" name="subject" value="New inquiry from Light Analytics website">
    <input type="checkbox" name="botcheck" style="display: none;" tabindex="-1" autocomplete="off">

    <div class="form-field">
      <label for="name">Name</label>
      <input type="text" id="name" name="name" required>
    </div>

    <div class="form-field">
      <label for="organization">Organization</label>
      <input type="text" id="organization" name="organization" required>
    </div>

    <div class="form-field">
      <label for="email">Email</label>
      <input type="email" id="email" name="email" required>
    </div>

    <div class="form-field">
      <label for="need">What do you need?</label>
      <select id="need" name="need" required>
        <option value="" disabled selected>Select one</option>
        <option value="Investigative Report">Investigative Report</option>
        <option value="SACCO/MFB Due Diligence">SACCO/MFB Due Diligence</option>
        <option value="Sector Intelligence Retainer">Sector Intelligence Retainer</option>
        <option value="Custom Engagement">Custom Engagement</option>
        <option value="Dataset Request">Dataset Request</option>
        <option value="Not sure yet">Not sure yet</option>
      </select>
    </div>

    <div class="form-field">
      <label for="message">Message</label>
      <textarea id="message" name="message" required></textarea>
    </div>

    <button type="submit" class="btn">Send</button>
  </form>

  <div class="contact-alt">
    <p><strong>Prefer email or LinkedIn?</strong></p>
    <p><a href="mailto:lucywanguik01@gmail.com">lucywanguik01@gmail.com</a></p>
    <p><a href="https://www.linkedin.com/in/lucywangui-data" target="_blank" rel="noopener">linkedin.com/in/lucywangui-data</a></p>
  </div>
</section>
