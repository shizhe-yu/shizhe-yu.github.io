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
    <p>Office 7222</p>
    <p>1180 Observatory Dr</p>
    <p>Madison, WI 53706</p>
    <div class="profile-icons">
      <a href="mailto:shizhe.yu@wisc.edu" title="Email"><i class="fa-solid fa-envelope"></i></a>
      <a href="https://econ.wisc.edu/staff/yu-shizhe/" title="Profile"><i class="fa-solid fa-building-columns"></i></a>
      <a href="/assets/img/wechat_qr.png" title="Wechat Blog"><i class="fa-brands fa-weixin"></i></a>
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
  .profile .more-info { font-family: inherit; font-size: 0.85rem; line-height: 1.5; color: var(--global-text-color-light); }
  .profile .more-info p { display: block; }
  /* contact icons under the photo */
  .profile .profile-icons { margin-top: 0.6rem; font-size: 1.25rem; }
  .profile .profile-icons a { color: var(--global-text-color-light); margin-right: 0.8rem; }
  .profile .profile-icons a:hover { color: var(--global-theme-color); }
  /* two-column layout: photo/address/icons on the left, text on the right */
  .post article { display: flex; align-items: flex-start; gap: 2rem; }
  .post article > .profile { flex: 0 0 30%; width: 30%; margin: 0; float: none; }
  .post article > .clearfix { flex: 1 1 auto; min-width: 0; }
  .post article > .clearfix > p:first-child { margin-top: 0; }
  /* phones: stack photo above the text */
  @media (max-width: 576px) {
    .post article { flex-direction: column; }
    .post article > .profile { flex-basis: auto; width: 100%; }
  }
</style>

Welcome to my website!

I am Shizhe Yu (in Chinese, 俞施喆), a PhD candidate in Economics at University of Wisconsin–Madison, specializing in Industrial Organization ([CV](/assets/pdf/cv.pdf)).

Feel free to [contact me](mailto:shizhe.yu@wisc.edu) if you'd like to discuss anything.
