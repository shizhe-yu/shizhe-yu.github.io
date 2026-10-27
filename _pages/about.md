---
layout: about
title: About
permalink: /
nav_order: 0

profile:
  align: left
  image: prof_pic.png
  image_circular: false # crops the image to make it circular
  more_info: >
    <p>Office 7222, 1180 Observatory Dr</p>
    <p>Madison, WI 53706</p>
    <div class="profile-icons">
      <a href="mailto:shizhe.yu@wisc.edu" title="Email"><i class="fa-solid fa-envelope"></i></a>
      <a href="https://econ.wisc.edu/staff/yu-shizhe/" title="Profile"><i class="fa-solid fa-building-columns"></i></a>
      <a href="/assets/img/wechat_qr.png" title="Wechat Blog" id="wechat-link"><i class="fa-brands fa-weixin"></i></a>
    </div>

selected_papers: false # includes a list of papers marked as "selected={true}"
social: false # icons are shown under the photo instead (see profile.more_info above)

announcements:
  enabled: false # includes a list of news items

latest_posts:
  enabled: false
---

<style>
  /* keep the photo at its original aspect ratio */
  .profile img { height: auto !important; aspect-ratio: auto; object-fit: contain; }
  /* address: same font as the page body, smaller and muted */
  .profile .more-info { font-family: inherit; font-size: 0.85rem; line-height: 1.35; margin-top: 0.4rem; color: var(--global-text-color-light); }
  .profile .more-info p { display: block; margin: 0; }
  /* contact icons under the photo */
  .profile .profile-icons { margin-top: 0.6rem; font-size: 1.25rem; }
  .profile .profile-icons a { color: var(--global-text-color-light); margin-right: 0.8rem; }
  .profile .profile-icons a:hover { color: var(--global-theme-color); }
  /* two-column layout: photo/address/icons on the left, text on the right */
  .post article { display: flex; align-items: flex-start; gap: 2rem; }
  .post article > .profile { flex: 0 0 30%; width: 30%; margin: 0; float: none; }
  .post article > .clearfix { flex: 1 1 auto; min-width: 0; }
  .post article > .clearfix > p:first-of-type { margin-top: 0; }
  /* Wechat Blog QR code pop-up */
  .qr-modal { display: none; position: fixed; inset: 0; z-index: 2000; background: rgba(0, 0, 0, 0.6);
    align-items: center; justify-content: center; padding: 1rem; }
  .qr-modal.open { display: flex; }
  .qr-modal-box { position: relative; background: var(--global-bg-color); border-radius: 10px;
    padding: 2.2rem 1.2rem 1.2rem; max-width: 360px; width: 100%; text-align: center; box-shadow: 0 8px 30px rgba(0, 0, 0, 0.3); }
  .qr-modal-box img { width: 100%; height: auto; border-radius: 6px; }
  .qr-modal-box p { margin: 0.6rem 0 0; font-size: 0.9rem; color: var(--global-text-color-light); }
  .qr-modal-close { position: absolute; top: 0.4rem; right: 0.6rem; border: none; background: none;
    font-size: 1.8rem; line-height: 1; color: var(--global-text-color); cursor: pointer; }
  .qr-modal-close:hover { color: var(--global-theme-color); }
  /* phones: stack photo above the text */
  @media (max-width: 576px) {
    .post article { flex-direction: column; }
    .post article > .profile { flex-basis: auto; width: 100%; }
  }
</style>

Welcome to my website!

I am Shizhe Yu (in Chinese, 俞施喆, pronounced SHR-juh YOO), a PhD candidate in Economics at University of Wisconsin–Madison, specializing in Industrial Organization. You can find my CV [here](/assets/pdf/cv.pdf){:target="_blank" rel="noopener"}.

Feel free to [contact me](mailto:shizhe.yu@wisc.edu) if you'd like to discuss anything.

<div class="qr-modal" id="wechat-modal" role="dialog" aria-modal="true" aria-label="Wechat Blog QR code">
  <div class="qr-modal-box">
    <button type="button" class="qr-modal-close" id="wechat-modal-close" aria-label="Close">&times;</button>
    <img src="/assets/img/wechat_qr.png" alt="Wechat Blog QR code">
    <p>Scan with WeChat</p>
  </div>
</div>

<script>
  document.addEventListener("DOMContentLoaded", function () {
    var link = document.getElementById("wechat-link");
    var modal = document.getElementById("wechat-modal");
    var closeBtn = document.getElementById("wechat-modal-close");
    if (!link || !modal) return;
    function openModal(e) { e.preventDefault(); modal.classList.add("open"); closeBtn.focus(); }
    function closeModal() { modal.classList.remove("open"); link.focus(); }
    link.addEventListener("click", openModal);
    closeBtn.addEventListener("click", closeModal);
    /* click on the dark background also closes it */
    modal.addEventListener("click", function (e) { if (e.target === modal) closeModal(); });
    /* so does the Esc key */
    document.addEventListener("keydown", function (e) { if (e.key === "Escape" && modal.classList.contains("open")) closeModal(); });
  });
</script>
