---
layout: default
title: Home
date: 09-2025
---

hi! my name is <span id="random-name" style="cursor:pointer; text-decoration:underline;"></span>. i'm a foundation scholar in computer science and linguistics at trinity college, dublin; my interests include in computing, language, and <span id="random-entry" style="cursor:pointer; text-decoration:underline;">...</span>.

right now, i'm doing computational neuroscience research at the di liberto lab, organising schools debating events as librarian of the hist, and reading a lot of books.

you can find some projects i've worked on [here](projects.html) and some posts i've written [here](misc.html).

feel free to get in touch at [oscurran [at] gmail [dot] com](mailto:oscurran@gmail.com).

<script>
  const names = [
    "odhrán",
    "/ˈɔːɹ.ɪn/",
    "/ˈɔːɹ.aːn/",
    "/ˈoːɾˠ.aːnˠ/"
  ];

  let currentNameIndex = 0;
  const nameElement = document.getElementById('random-name');

  const setName = () => {
    if (nameElement) nameElement.textContent = names[currentNameIndex];
  };

  document.addEventListener('DOMContentLoaded', setName);

  if (nameElement) {
    nameElement.addEventListener('click', () => {
      currentNameIndex = (currentNameIndex + 1) % names.length;
      setName();
    });
  }

  const entries = [
    "cognition",
	"public policy",
	"philosophy",
	"rhetoric",
	"mathematics",
	"poetry",
	"public transit",
	"cities",
	"speculative fiction",
	"marginalia",
	"second-hand bookshops",
	"library stamps",
	"abandoned websites",
	"overheard conversations",
	"edge cases",
	"pointed questions",
  ];

  const randomEntry = () => entries[Math.floor(Math.random() * entries.length)];
  const element = document.getElementById('random-entry');

  const setEntry = () => {
    if (element) element.textContent = randomEntry();
  };

  document.addEventListener('DOMContentLoaded', setEntry);
  if (element) element.addEventListener('click', setEntry);
</script>