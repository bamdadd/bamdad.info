---
layout: page
title: Contact
permalink: /contact/
---

<div class="content-section">
  <div class="wrapper">
    <div class="section-title">
      <h2>Get in Touch</h2>
      <p class="section-subtitle">Ready to transform your technology capabilities? Let's discuss your requirements and explore how we can help.</p>
    </div>
    
    <div class="contact-content">
      <div class="contact-info">
        <div class="contact-method">
          <div class="contact-icon email-icon"></div>
          <h3>Email</h3>
          <p><a href="#" onclick="sendEmail(); return false;" class="email-link">Click to reveal email</a></p>
          <p class="contact-note">For project inquiries and general consultation requests</p>
        </div>
        
        <div class="contact-method">
          <div class="contact-icon location-icon"></div>
          <h3>Office Locations</h3>
          <div class="office-locations">
            <div class="office">
              <h4>United Kingdom</h4>
              <address>
                Ground Floor, Unit B<br>
                Lostock Office Park<br>
                Lynstock Way, Lostock<br>
                Bolton, England BL6 4SG
              </address>
            </div>
            
            <div class="office">
              <h4>City of London</h4>
              <address>
                Financial District<br>
                London, England
              </address>
            </div>
            
            <div class="office">
              <h4>Abu Dhabi</h4>
              <address>
                Abu Dhabi Global Market<br>
                Abu Dhabi, UAE
              </address>
            </div>
            
            <div class="office">
              <h4>Toronto</h4>
              <address>
                Financial District<br>
                Toronto, ON, Canada
              </address>
            </div>
          </div>
        </div>
        
        <div class="contact-method">
          <div class="contact-icon calendar-icon"></div>
          <h3>Consultation</h3>
          <p>We offer complimentary initial consultations to understand your technology challenges and requirements.</p>
          <a href="#" onclick="scheduleConsultation(); return false;" class="btn btn-primary">Schedule a Consultation</a>
        </div>
      </div>
      
      <div class="availability-section">
        <div class="contact-method">
          <div class="contact-icon availability-icon"></div>
          <h3>Availability</h3>
          <p>Currently accepting new consulting projects for Q3 2025 and beyond. We work with select clients to ensure the highest quality of service and attention to detail.</p>
          <div class="response-time">
            <strong>Response Time:</strong> Within 24 hours for all inquiries
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

<style>
.contact-content {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
  margin-top: 3rem;
}

.contact-info {
  display: flex;
  flex-direction: column;
  gap: 2rem;
}

.availability-section {
  display: flex;
  flex-direction: column;
  gap: 2rem;
}

.contact-method {
  padding: 2rem;
  background: white;
  border-radius: 12px;
  border: 1px solid var(--border-light);
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
}

.contact-icon {
  width: 48px;
  height: 48px;
  background: linear-gradient(135deg, var(--primary-blue), var(--secondary-blue));
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 1rem;
  position: relative;
  
  &::before {
    content: '';
    position: absolute;
    width: 24px;
    height: 24px;
    background: white;
  }
}

.email-icon::before {
  mask: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect width="20" height="16" x="2" y="4" rx="2"/><path d="m22 7-10 5L2 7"/></svg>');
  -webkit-mask: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect width="20" height="16" x="2" y="4" rx="2"/><path d="m22 7-10 5L2 7"/></svg>');
  mask-size: cover;
  -webkit-mask-size: cover;
}

.location-icon::before {
  mask: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M20 10c0 6-8 12-8 12s-8-6-8-12a8 8 0 0 1 16 0Z"/><circle cx="12" cy="10" r="3"/></svg>');
  -webkit-mask: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M20 10c0 6-8 12-8 12s-8-6-8-12a8 8 0 0 1 16 0Z"/><circle cx="12" cy="10" r="3"/></svg>');
  mask-size: cover;
  -webkit-mask-size: cover;
}

.calendar-icon::before {
  mask: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M8 2v4"/><path d="M16 2v4"/><rect width="18" height="18" x="3" y="4" rx="2"/><path d="M3 10h18"/></svg>');
  -webkit-mask: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M8 2v4"/><path d="M16 2v4"/><rect width="18" height="18" x="3" y="4" rx="2"/><path d="M3 10h18"/></svg>');
  mask-size: cover;
  -webkit-mask-size: cover;
}

.availability-icon::before {
  mask: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"/><path d="M12 6v6l4 2"/></svg>');
  -webkit-mask: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"/><path d="M12 6v6l4 2"/></svg>');
  mask-size: cover;
  -webkit-mask-size: cover;
}

.contact-method h3 {
  margin-bottom: 0.5rem;
  font-size: 1.25rem;
}

.contact-method address {
  font-style: normal;
  line-height: 1.6;
  color: var(--text-medium);
}

.contact-note {
  font-size: 0.9rem;
  color: var(--text-light);
  margin-top: 0.5rem;
}

.response-time {
  margin-top: 1rem;
  padding: 1rem;
  background: var(--bg-light);
  border-radius: 6px;
  border-left: 4px solid var(--accent-blue);
}

.office-locations {
  display: grid;
  gap: 1.5rem;
  margin-top: 1rem;
}

.office h4 {
  margin-bottom: 0.5rem;
  color: var(--primary-blue);
  font-size: 1rem;
  font-weight: 600;
}

.office address {
  margin-left: 0;
  padding-left: 1rem;
  border-left: 2px solid var(--border-light);
}

@media (max-width: 768px) {
  .contact-content {
    grid-template-columns: 1fr;
    gap: 2rem;
  }
}
</style>

<script>
function sendEmail() {
  // ROT13 encoded email to prevent spam bot harvesting
  const encoded = 'onzqnq@onzqnq.vasb';
  const email = encoded.replace(/[a-zA-Z]/g, function(c) {
    return String.fromCharCode((c <= 'Z' ? 90 : 122) >= (c = c.charCodeAt(0) + 13) ? c : c - 26);
  });
  
  // Update the link text and make it a proper mailto
  const emailLink = document.querySelector('.email-link');
  emailLink.href = 'mailto:' + email;
  emailLink.textContent = email;
  emailLink.onclick = null; // Remove the onclick handler
  
  // Optionally trigger the email client
  window.location.href = 'mailto:' + email;
}

function scheduleConsultation() {
  // ROT13 encoded email
  const encoded = 'onzqnq@onzqnq.vasb';
  const email = encoded.replace(/[a-zA-Z]/g, function(c) {
    return String.fromCharCode((c <= 'Z' ? 90 : 122) >= (c = c.charCodeAt(0) + 13) ? c : c - 26);
  });
  
  const subject = encodeURIComponent('Consultation Request');
  window.location.href = 'mailto:' + email + '?subject=' + subject;
}
</script>