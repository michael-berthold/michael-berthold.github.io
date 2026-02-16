---
layout: default
title: About Me
permalink: /about/
---

<style>
/* Language toggle button styling */
.language-toggle {
  display: flex;
  gap: 10px;
  margin-bottom: 30px;
  padding: 10px 0;
}

.language-toggle button {
  padding: 2px 4px;
  border: 2px solid #2b2b2b;
  background-color: white;
  color: #2b2b2b;
  font-family: 'Inter', sans-serif;
  font-size: 12px;
  font-weight: 600;
  cursor: pointer;
  border-radius: 2px;
  transition: all 0.3s ease;
}

.language-toggle button:hover {
  background-color: #7a7a7a;
  transform: translateY(-2px);
}

.language-toggle button.active {
  background: linear-gradient(90deg, #2b2b2b, #3b3b3b);
  color: white;
  border-color: #2b2b2b;
  box-shadow: 0 4px 8px rgba(126, 126, 126, 0.3);
}

.language-section {
  display: none;
}

.language-section.active {
  display: block;
  animation: fadeIn 0.3s ease-in;
}

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(10px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>

<div class="language-toggle">
  <button id="btn-english" class="active">en</button>
  <button id="btn-german">de</button>
</div>

<div id="content-english" class="language-section active" markdown="1">

# About Me

Hello! I'm Michael Berthold. This is my personal website where I share my work, thoughts, and publications.

### Profile Picture

![Michael Berthold Profile]({{ site.baseurl }}/assets/images/Berthold2025sw.jpg){: style="max-width: 300px; border-radius: 8px; margin: 20px 0;"}

### Background

[Your background and professional information will go here]

### Interests

[Your interests and expertise will go here]

</div>

<div id="content-german" class="language-section" markdown="1">

# Über mich

Hallo! Ich bin Michael Berthold. Dies ist meine persönliche Website, auf der ich meine Arbeit, Gedanken und Veröffentlichungen teile.

### Profile Picture

![Michael Berthold Profile]({{ site.baseurl }}/assets/images/Berthold2025sw.jpg){: style="max-width: 300px; border-radius: 8px; margin: 20px 0;"}

### Hintergrund

[Ihre Hintergrundinformationen und professionellen Details werden hier eingefügt]

### Interessen

[Ihre Interessen und Fachkenntnisse werden hier eingefügt]

</div>

<script>
// Language toggle functionality
function switchLanguage(lang) {
  // Validate language parameter to prevent XSS
  if (lang !== 'en' && lang !== 'de') {
    return;
  }
  
  // Update active states for buttons
  const btnEnglish = document.getElementById('btn-english');
  const btnGerman = document.getElementById('btn-german');
  const contentEnglish = document.getElementById('content-english');
  const contentGerman = document.getElementById('content-german');
  
  if (lang === 'en') {
    btnEnglish.classList.add('active');
    btnGerman.classList.remove('active');
    contentEnglish.classList.add('active');
    contentGerman.classList.remove('active');
  } else if (lang === 'de') {
    btnEnglish.classList.remove('active');
    btnGerman.classList.add('active');
    contentEnglish.classList.remove('active');
    contentGerman.classList.add('active');
  }
  
  // Save preference to localStorage
  localStorage.setItem('preferredLanguage', lang);
}

// Initialize event listeners and load saved preference on page load
document.addEventListener('DOMContentLoaded', function() {
  // Attach event listeners to buttons
  const btnEnglish = document.getElementById('btn-english');
  const btnGerman = document.getElementById('btn-german');
  
  btnEnglish.addEventListener('click', function() {
    switchLanguage('en');
  });
  
  btnGerman.addEventListener('click', function() {
    switchLanguage('de');
  });
  
  // Load saved language preference with validation
  const savedLang = localStorage.getItem('preferredLanguage');
  if (savedLang === 'en' || savedLang === 'de') {
    switchLanguage(savedLang);
  }
});
</script>
