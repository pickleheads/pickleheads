<template>
  <footer class="footer">
    <div class="footer-top">
      <p class="footer-title">The answer is 42</p>
    </div>
    <div class="footer-bottom">
      <div>
        <p>2019 Pickleheads</p>
      </div>
      <div class="footer-icon-container">
        <a class="footer-link" href="https://github.com/pickleheads">
          <i class="fab fa-github footer-icon"></i>
        </a>
        <a class="footer-link" href="mailto:hello@pickleheads.club">
          <i class="fas fa-envelope footer-icon"></i>
        </a>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
};
</script>

<style scoped>
.footer {
  padding: 60px 40px 40px;
  background-color: var(--black);
  color: white;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.footer-top {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.footer-title {
  font-size: 1.4rem;
  font-family: 'Playfair Display', serif;
}

.footer-bottom {
  margin: 30px 0 0;
  width: 100%;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
}

.footer-link {
  transition: color 150ms linear;
  color: #95989a;
}

.footer-link:hover {
  color: white;
}

.footer-icon-container > .footer-link {
  margin-right: 20px;
}

.footer-icon-container > .footer-link:last-of-type {
  margin-right: 0;
}

.footer-icon {
  font-size: 1.6rem;
}
</style>
