---
title: "聯係我們"
date: 2025-01-01
draft: false
layout: "simple"
---

<div class="custom-contact-parent" style="margin-top: 50px;">
  <div class="custom-contact-child1">
  <div style="font-size: 20px; margin-top:30px; margin-bottom: 10px;" >發電子郵件給我們</div>
  <script src="https://cdn.jsdelivr.net/npm/@emailjs/browser@4/dist/email.min.js"></script>
   <form class="custom-formcontact-container" id="contact-form">
       <input class="custom-formcontact-input" type="text" id="name" placeholder="姓名" required><p>
       <input class="custom-formcontact-input" type="email" id="email" placeholder="郵箱" required><p>
       <textarea class="custom-formcontact-textarea" id="message" placeholder="留言" required></textarea><p>
       <button type="submit" class="custom-formcontact-button">發送</button>
   </form>
   <script>
       emailjs.init("vdP5Xufc7ya4tda5p"); //  Public Key
       document.getElementById('contact-form').addEventListener('submit', function(event) {
           event.preventDefault();
           const data = {
               name: document.getElementById("name").value,
               email: document.getElementById("email").value,
               message: document.getElementById("message").value,
           };
           console.log("發送數據:", data); // test
           emailjs.send("service_30kcso8", "template_0lan0r9", data) // 業務ID service 模板ID template
               .then(() => alert('發送成功！'),
                    (error) => alert('發送失敗：' + error.text));
       });
   </script>
  </div>

  <div class="custom-contact-child2"></div>
  
  <div class="custom-contact-child3">
   <div style="font-size: 20px; margin-top:30px; margin-bottom: 10px;" >關注我們的公衆號</div>
   <img style="margin-top: 8px; width: 275px;" src="/images/weixin.jpg">
   
  <div style="margin-top:0px; white-space: nowrap;">
  <a href="#" class="custom-icon-ohulab">{{< icon "weixin" >}}</a>
  <a href="https://www.toutiao.com/c/user/token/MS4wLjABAAAAg0e3TfgJwAzj2dS6wu8Mg3dWTIzAjTGU26mQGm4AKjQ/" target="_blank" class="custom-icon-ohulab">{{< 
  icon "toutiao" >}}</a>
  <a href="https://www.xiaohongshu.com/user/profile/5d423fc90000000016034bc6?xsec_token=YBvkMf6BM6shT8zJAPAaDS4TdQNUmu4WskjU5MrT_0mss%3D&xsec_source=app_share&
  xhsshare=WeixinSession&appuid=5d423fc90000000016034bc6&apptime=1741686168&share_id=5759c5c385644ebf8cf03fea99c2e53e&share_channel=wechat/" target="_blank" 
  class="custom-icon-ohulab">{{< icon "redbook" >}}</a>
  <a href="https://zhihu.com/people/nscm/" target="_blank" class="custom-icon-ohulab">{{< icon "zhihu" >}}</a>
  <a href="https://m.weibo.cn/u/6178605197/" target="_blank" class="custom-icon-ohulab">{{< icon "xinlangweibo" >}}</a>
  <a href="mailto:ohulab.org@ohulab.org" target="_blank" class="custom-icon-ohulab">{{< icon "email" >}}</a>
  </div>
  
  </div>
</div>
