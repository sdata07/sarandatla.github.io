---
layout: about
title: about
permalink: /
subtitle:

profile:
  align: right
  image: Avatar.jpeg
  image_circular: false # crops the image to make it circular
  more_info: false 

selected_papers: false # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page

announcements:
  enabled: false # includes a list of news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: false
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts
---

<!-- Animated Hello World (Loki-style) -->
<div id="animated-hello" style="margin-bottom: 1em;"></div>

<script>
  document.addEventListener("DOMContentLoaded", function () {
    const fonts = [
      "Georgia", "Courier New", "Arial", "Times New Roman", "Comic Sans MS",
      "Impact", "Lucida Console", "Palatino Linotype", "Trebuchet MS", "Verdana"
    ];
    const finalFont = "Georgia";
    const text = "Hello World!";
    const container = document.getElementById("animated-hello");

    // Create spans for each letter (only once)
    container.innerHTML = "";
    text.split('').forEach(char => {
      const span = document.createElement("span");
      span.classList.add("letter");
      span.textContent = char;
      container.appendChild(span);
    });

    const spans = container.querySelectorAll(".letter");

    function animateLetters() {
      spans.forEach((span) => {
        let count = 0;
        const maxCycles = 15 + Math.floor(Math.random() * 10); // more cycles = slower
        const interval = setInterval(() => {
          const font = fonts[Math.floor(Math.random() * fonts.length)];
          span.style.fontFamily = font;
          count++;
          if (count >= maxCycles) {
            clearInterval(interval);
            span.style.fontFamily = finalFont;
          }
        }, 1000); // <-- slower switch speed (was 100ms)
      });
    }

    animateLetters();
    setInterval(animateLetters, 5000); // <-- slower repeat (was 3000ms)
  });
</script>

<style>
  #animated-hello {
    color: white;
    font-size: 2.5rem;
    font-weight: bold;
    text-align: center;
    font-family: Georgia, serif;
    letter-spacing: 0.05em;
  }
  #animated-hello .letter {
    display: inline-flex;
    justify-content: center;
    align-items: center;
    min-width: 1em;
    height: 3rem;
    transition: font-family 0.3s ease;
  }
  .profile .img {

  }
</style>

<div style = "font-size: 22px" >

<p>My name is Saran Datla and I am a sophomore studying CS + Physics at UIUC.</p>

<p>I ❤️ coding, physics, and everything in between.</p>

<p>I'm also a wannabe Quantum Engineer who also loves learning about AI. Find out more in my Projects Page!</p>

</div>
