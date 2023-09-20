<template>
  <footer class="footer">
    <div class="footer-content">
      <div class="contact-info">
        <div class="contact-item">
          <a href="mailto:tanvirrahmantaiyeb@gmail.com" class="contact-link">
            <img src="https://png.pngtree.com/png-vector/20190429/ourmid/pngtree-mail-icon-vector-illustration-in-line-style-for-any-purpose-png-image_996816.jpg" alt="Email Icon" class="contact-icon">
            tanvirrahmantaiyeb@gmail.com
          </a>
        </div>
        <div class="contact-item">
          <a href="tel:+61412781376" class="contact-link">
            <img src="https://images.rawpixel.com/image_png_800/cHJpdmF0ZS9sci9pbWFnZXMvd2Vic2l0ZS8yMDIyLTA1L3JtNTMzLW91dGxpbmUtMjJfMS5wbmc.png" alt="Phone Icon" class="contact-icon">
            +61 4 1278 1376
          </a>
        </div>
        <div class="contact-item">
          <a href="https://www.linkedin.com/in/tanvir-rahman-taiyeb/" target="_blank" class="contact-link">
            <img src="https://img.freepik.com/premium-vector/linkedin-icon_488108-5.jpg?w=2000" alt="LinkedIn Icon" class="contact-icon">
            linkedin.com/in/tanvir-rahman-taiyeb
          </a>
        </div>
      </div>
      <div class="social-icons">
        <!-- Add social media icons here -->
        <!-- Example: <a href="#" target="_blank"><i class="fab fa-twitter"></i></a> -->
      </div>
    </div>
  </footer>
</template>

<style scoped>
/* Add footer styles here */
.footer {
  background-color: #333;
  color: #fff;
  padding: 15px 0;
  text-align: center;
}

.footer-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
}

.contact-info {
  flex: 1;
  text-align: left;
}

.contact-item {
  margin: 5px 0;
}

.contact-link {
  color: #00a0d2;
  text-decoration: none;
  display: flex;
  align-items: center;
}

.contact-link:hover {
  text-decoration: underline;
}

.contact-icon {
  width: 16px;
  height: 16px;
  margin-right: 8px;
}

.social-icons {
  flex: 1;
  text-align: right;
}

/* Add custom styling for social media icons */
</style>
