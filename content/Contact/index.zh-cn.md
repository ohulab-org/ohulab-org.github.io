---
title: "联系我们"
date: 2025-01-01
draft: false
layout: "simple"
---

<div class="custom-contact-parent" style="margin-top: 50px;">
  <div class="custom-contact-child1">
  <div style="font-size: 20px; margin-top:30px; margin-bottom: 10px;" >发电子邮件给我们</div>
  <script src="https://cdn.jsdelivr.net/npm/@emailjs/browser@4/dist/email.min.js"></script>
   <form class="custom-formcontact-container" id="contact-form">
       <input class="custom-formcontact-input" type="text" id="name" placeholder="姓名" required><p>
       <input class="custom-formcontact-input" type="email" id="email" placeholder="邮箱" required><p>
       <textarea class="custom-formcontact-textarea" id="message" placeholder="留言" required></textarea><p>
       <button type="submit" class="custom-formcontact-button">发送</button>
   </form>
   <script>
       emailjs.init("vdP5Xufc7ya4tda5p"); // 替换为你的 Public Key
       document.getElementById('contact-form').addEventListener('submit', function(event) {
           event.preventDefault();
           const data = {
               name: document.getElementById("name").value,
               email: document.getElementById("email").value,
               message: document.getElementById("message").value,
           };
           console.log("发送数据:", data); // 调试用
           emailjs.send("service_30kcso8", "template_0lan0r9", data) // 业务ID service 和模板ID template
               .then(() => alert('发送成功！'),
                    (error) => alert('发送失败：' + error.text));
       });
   </script>
  </div>



  <div class="custom-contact-child2"></div>
  
  <div class="custom-contact-child3">
   <div style="font-size: 20px; margin-top:30px; margin-bottom: 10px;" >Official WeChat account</div>
   <img style="margin-top: 8px; width: 275px;" src="/images/weixin.jpg">
   
  <div style="margin-top:0px; white-space: nowrap;">
  <a href="#" class="custom-icon-ohulab">{{< icon "weixin" >}}</a>
  <a href="#" target="_blank" class="custom-icon-ohulab">{{< icon "toutiao" >}}</a>
  <a href="#" target="_blank" 
  class="custom-icon-ohulab">{{< icon "redbook" >}}</a>
  <a href="#" target="_blank" class="custom-icon-ohulab">{{< icon "zhihu" >}}</a>
  <a href="#" target="_blank" class="custom-icon-ohulab">{{< icon "xinlangweibo" >}}</a>
  <a href="mailto:ohulab.org@ohulab.org" target="_blank" class="custom-icon-ohulab">{{< icon "email" >}}</a>
  </div>
  
  </div>
</div>
