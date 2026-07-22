<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
  <title>Abhishek Shukla • AI Engineer GitHub Profile</title>
  <!-- Font Awesome 6 for icons -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <!-- Google Fonts for modern look -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,400;14..32,500;14..32,600;14..32,700&family=Fira+Code:wght@400;500;600&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    body {
      background: linear-gradient(135deg, #0b041c 0%, #1a0a2e 40%, #0f1b3a 100%);
      font-family: 'Inter', sans-serif;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding: 2rem 1.5rem;
      min-height: 100vh;
      color: #e8e0f0;
    }
    /* Main card – replicates GitHub README style with max width */
    .profile-container {
      max-width: 960px;
      width: 100%;
      background: rgba(18, 10, 31, 0.7);
      backdrop-filter: blur(16px);
      -webkit-backdrop-filter: blur(16px);
      border: 1px solid rgba(106, 17, 203, 0.25);
      box-shadow: 0 30px 50px rgba(0,0,0,0.7), 0 0 0 1px rgba(106, 17, 203, 0.3);
      border-radius: 2.5rem;
      overflow: hidden;
      transition: all 0.3s ease;
    }

    /* Video Banner Section */
    .banner-video-wrapper {
      position: relative;
      width: 100%;
      height: 240px;
      overflow: hidden;
      border-bottom: 2px solid #6a11cb;
    }
    .banner-video {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: block;
      filter: brightness(0.9) contrast(1.1);
    }
    .banner-overlay {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: linear-gradient(to bottom, rgba(106,17,203,0.25), rgba(37,117,252,0.3));
      mix-blend-mode: overlay;
      pointer-events: none;
    }
    .banner-text-overlay {
      position: absolute;
      bottom: 20px;
      left: 30px;
      color: white;
      text-shadow: 0 4px 15px black;
      z-index: 2;
      display: flex;
      flex-direction: column;
    }
    .banner-name {
      font-size: 2.8rem;
      font-weight: 700;
      letter-spacing: 1px;
      background: linear-gradient(to right, #ffffff, #d9b3ff);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }
    .banner-desc {
      font-size: 1rem;
      font-weight: 500;
      color: #f0e6ff;
      background: rgba(0,0,0,0.5);
      padding: 0.2rem 1rem;
      border-radius: 20px;
      backdrop-filter: blur(4px);
      width: fit-content;
      margin-top: 5px;
    }

    /* inner content padding */
    .content {
      padding: 2rem 2rem 1.8rem;
    }

    /* badges row */
    .badges-row {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      justify-content: center;
      gap: 0.7rem;
      margin: 0.5rem 0 1.5rem;
    }
    .badge {
      background: rgba(106, 17, 203, 0.2);
      backdrop-filter: blur(8px);
      border: 1px solid rgba(255,255,255,0.2);
      padding: 0.4rem 1.2rem;
      border-radius: 30px;
      font-weight: 600;
      font-size: 0.9rem;
      color: #fff;
      display: flex;
      align-items: center;
      gap: 5px;
      transition: 0.2s;
      box-shadow: 0 4px 12px rgba(0,0,0,0.3);
    }
    .badge i {
      color: #ffd966;
    }
    .social-links {
      display: flex;
      justify-content: center;
      gap: 1.8rem;
      margin: 1rem 0 1.2rem;
    }
    .social-links a {
      color: #d4c0f0;
      font-size: 1.6rem;
      transition: 0.3s;
      background: rgba(255,255,255,0.05);
      padding: 0.5rem;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      width: 48px;
      height: 48px;
      backdrop-filter: blur(5px);
      border: 1px solid rgba(255,255,255,0.2);
    }
    .social-links a:hover {
      color: white;
      background: #6a11cb;
      transform: translateY(-3px);
      box-shadow: 0 10px 20px rgba(106,17,203,0.5);
    }

    .typing-animation {
      font-family: 'Fira Code', monospace;
      font-weight: 600;
      font-size: 1.3rem;
      color: #c28aff;
      text-align: center;
      margin: 1rem 0 1.8rem;
      border-right: 2px solid #a970ff;
      white-space: nowrap;
      overflow: hidden;
      width: fit-content;
      margin-left: auto;
      margin-right: auto;
      animation: blinkCursor 0.8s infinite;
    }
    @keyframes blinkCursor {
      0%, 100% { border-color: #a970ff; }
      50% { border-color: transparent; }
    }

    .section-divider {
      height: 3px;
      background: linear-gradient(90deg, #6a11cb, #2575fc, #6a11cb);
      margin: 1.8rem 0 1.8rem;
      border-radius: 5px;
    }

    .about-code {
      background: rgba(10, 5, 20, 0.7);
      backdrop-filter: blur(10px);
      border-radius: 20px;
      padding: 1.2rem 1.5rem;
      font-family: 'Fira Code', monospace;
      font-size: 0.9rem;
      border-left: 4px solid #a970ff;
      margin: 1.2rem 0;
      color: #d7c4f0;
      line-height: 1.6;
    }

    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 1.5rem;
      margin: 1.8rem 0;
    }
    .project-card {
      background: rgba(25, 15, 45, 0.6);
      backdrop-filter: blur(14px);
      border: 1px solid rgba(106,17,203,0.35);
      border-radius: 24px;
      padding: 1.5rem 1.2rem;
      transition: all 0.25s;
    }
    .project-card:hover {
      transform: translateY(-5px);
      border-color: #a970ff;
      box-shadow: 0 20px 30px -10px #6a11cb55;
    }
    .tech-tag {
      display: inline-block;
      background: #2a1a4a;
      padding: 0.2rem 0.7rem;
      border-radius: 15px;
      font-size: 0.7rem;
      font-weight: 600;
      margin-right: 5px;
      margin-bottom: 5px;
      color: #e0c8ff;
    }
    .stats-row {
      display: flex;
      flex-wrap: wrap;
      gap: 1rem;
      justify-content: center;
      margin: 1.8rem 0;
    }
    .stat-card {
      background: rgba(20, 10, 35, 0.7);
      backdrop-filter: blur(10px);
      border-radius: 20px;
      padding: 1rem 2rem;
      text-align: center;
      border: 1px solid #6a11cb55;
      min-width: 130px;
    }
    .footer-wave {
      height: 80px;
      background: linear-gradient(90deg, #6a11cb, #2575fc);
      mask-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 1200 120' preserveAspectRatio='none'%3E%3Cpath d='M321.39,56.44c58-10.79,114.16-30.13,172-41.86,82.39-16.72,168.19-17.73,250.45-.39C823.78,31,906.67,72,985.66,92.83c70.05,18.48,146.53,26.09,214.34,3V0H0V27.35A600.21,600.21,0,0,0,321.39,56.44Z'%3E%3C/path%3E%3C/svg%3E");
      -webkit-mask-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 1200 120' preserveAspectRatio='none'%3E%3Cpath d='M321.39,56.44c58-10.79,114.16-30.13,172-41.86,82.39-16.72,168.19-17.73,250.45-.39C823.78,31,906.67,72,985.66,92.83c70.05,18.48,146.53,26.09,214.34,3V0H0V27.35A600.21,600.21,0,0,0,321.39,56.44Z'%3E%3C/path%3E%3C/svg%3E");
      mask-size: cover;
      -webkit-mask-size: cover;
      margin-top: 0.5rem;
    }

    .glow-text {
      color: #e4ccff;
    }
    @media (max-width: 600px) {
      .banner-video-wrapper {
        height: 180px;
      }
      .banner-name {
        font-size: 2rem;
      }
    }
  </style>
</head>
<body>
  <div class="profile-container">
    <!-- Video Banner with animation overlay -->
    <div class="banner-video-wrapper">
      <!-- Embedded video: abstract AI neural network animation (looping, muted, autoplay) -->
      <video class="banner-video" autoplay muted loop playsinline>
        <!-- Using a royalty-free abstract tech video from coverr or similar. Placeholder source: -->
        <source src="https://cdn.coverr.co/videos/coverr-abstract-neural-network-1080p.mp4" type="video/mp4">
        <!-- Fallback image if video not supported -->
        <img src="https://placehold.co/960x240/1a0a2e/ffffff?text=AI+Neural+Animation" alt="banner fallback" style="width:100%; height:100%; object-fit:cover;">
      </video>
      <div class="banner-overlay"></div>
      <div class="banner-text-overlay">
        <span class="banner-name">Abhishek Shukla</span>
        <span class="banner-desc"><i class="fas fa-robot"></i> AI Engineer • Python Dev • LLM & RAG</span>
      </div>
    </div>

    <div class="content">
      <!-- Badges row -->
      <div class="badges-row">
        <div class="badge"><i class="fas fa-graduation-cap"></i> MCA Student</div>
        <div class="badge"><i class="fas fa-brain"></i> RAG | LangChain</div>
        <div class="badge"><i class="fas fa-code"></i> 200+ LeetCode</div>
        <div class="badge"><i class="fas fa-eye"></i> 12.3k views</div>
      </div>

      <!-- Social icons -->
      <div class="social-links">
        <a href="#" aria-label="LinkedIn"><i class="fab fa-linkedin-in"></i></a>
        <a href="#" aria-label="Gmail"><i class="fas fa-envelope"></i></a>
        <a href="#" aria-label="LeetCode"><i class="fas fa-laptop-code"></i></a>
        <a href="#" aria-label="GitHub"><i class="fab fa-github"></i></a>
      </div>

      <!-- Dynamic typing effect -->
      <div class="typing-animation" id="typingText"></div>

      <div class="section-divider"></div>

      <!-- About me code block -->
      <div style="font-weight: 600; font-size: 1.3rem; margin-bottom: 0.3rem;"><i class="fas fa-user-astronaut" style="color:#a970ff;"></i> 🧠 About Me</div>
      <div class="about-code">
        <span style="color:#c792ea;">class</span> <span style="color:#ffcb6b;">AbhishekShukla</span>:<br>
        &nbsp;&nbsp;<span style="color:#89ddff;">def</span> <span style="color:#82aaff;">__init__</span>(<span style="color:#ffcb6b;">self</span>):<br>
        &nbsp;&nbsp;&nbsp;&nbsp;self.role = <span style="color:#c3e88d;">"AI Engineer | Python Developer"</span><br>
        &nbsp;&nbsp;&nbsp;&nbsp;self.education = <span style="color:#c3e88d;">"MCA @ Accurate Institute"</span><br>
        &nbsp;&nbsp;&nbsp;&nbsp;self.focus = [<span style="color:#c3e88d;">"RAG Pipelines"</span>, <span style="color:#c3e88d;">"LLM Apps"</span>, <span style="color:#c3e88d;">"Multi-modal"</span>]<br>
        &nbsp;&nbsp;&nbsp;&nbsp;self.leetcode = <span style="color:#f78c6c;">"200+ solved"</span><br>
        &nbsp;&nbsp;&nbsp;&nbsp;self.location = <span style="color:#c3e88d;">"Noida, India"</span><br><br>
        <span style="color:#89ddff;">def</span> <span style="color:#82aaff;">currently_building</span>(<span style="color:#ffcb6b;">self</span>):<br>
        &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ff5370;">return</span> <span style="color:#c3e88d;">"AI Meeting Assistant — Multi-modal RAG 🎙️"</span>
      </div>

      <!-- Projects Section -->
      <div style="display: flex; align-items: center; gap: 0.5rem; margin: 1.5rem 0 0.8rem;">
        <i class="fas fa-rocket" style="color:#a970ff; font-size: 1.4rem;"></i>
        <span style="font-weight: 700; font-size: 1.4rem;">🚀 Featured Projects</span>
      </div>
      <div class="projects-grid">
        <div class="project-card">
          <h4 style="color: #f5e1ff;"><i class="fas fa-microphone-alt"></i> AI Meeting Assistant</h4>
          <p style="font-size:0.85rem; margin:0.5rem 0; opacity:0.9;">Multi-Modal RAG app: audio/video & docs → transcripts, summaries, bilingual.</p>
          <div>
            <span class="tech-tag">Python</span>
            <span class="tech-tag">LangChain</span>
            <span class="tech-tag">FAISS</span>
            <span class="tech-tag">Streamlit</span>
          </div>
          <a href="#" style="color:#bb9eff; font-size:0.8rem; margin-top:8px; display:inline-block;">🔗 Live Demo</a>
        </div>
        <div class="project-card">
          <h4 style="color: #f5e1ff;"><i class="fas fa-file-pdf"></i> AbhiChat – PDF Bot</h4>
          <p style="font-size:0.85rem; margin:0.5rem 0;">RAG chatbot: upload PDF, ask questions. FastAPI + vector retrieval.</p>
          <div>
            <span class="tech-tag">Python</span>
            <span class="tech-tag">LangChain</span>
            <span class="tech-tag">FastAPI</span>
            <span class="tech-tag">Vector DB</span>
          </div>
        </div>
      </div>

      <!-- Tech stack icons row -->
      <div style="margin: 1.5rem 0 0.5rem; font-weight: 600;"><i class="fas fa-tools"></i> Technologies & Tools</div>
      <div style="display: flex; flex-wrap: wrap; gap: 0.8rem; justify-content: center; background: rgba(0,0,0,0.3); border-radius: 30px; padding: 0.8rem;">
        <i class="fab fa-python fa-2x" style="color:#306998;"></i>
        <i class="fas fa-brain fa-2x" style="color:#a970ff;"></i>
        <img src="https://img.icons8.com/color/48/langchain.png" width="28" alt="langchain" style="filter: drop-shadow(0 0 4px #6a11cb);">
        <i class="fas fa-database fa-2x" style="color:#4db8ff;"></i>
        <i class="fab fa-js fa-2x" style="color:#f7df1e;"></i>
        <i class="fab fa-angular fa-2x" style="color:#dd0031;"></i>
        <i class="fab fa-git-alt fa-2x" style="color:#f05032;"></i>
        <i class="fab fa-linux fa-2x" style="color:#fcc624;"></i>
      </div>

      <!-- GitHub Stats style cards (graphical representation) -->
      <div class="stats-row">
        <div class="stat-card"><i class="fas fa-star"></i> 42 Stars</div>
        <div class="stat-card"><i class="fas fa-code-branch"></i> 18 Repos</div>
        <div class="stat-card"><i class="fas fa-fire"></i> 85 Contributions</div>
      </div>

      <!-- Contribution snake animation (inline SVG animation) -->
      <div style="text-align: center; margin: 1rem 0;">
        <svg width="100%" height="80" viewBox="0 0 600 80" preserveAspectRatio="none" style="max-width:100%;">
          <defs>
            <linearGradient id="snakeGrad" x1="0%" y1="0%" x2="100%" y2="0%">
              <stop offset="0%" stop-color="#6a11cb" />
              <stop offset="100%" stop-color="#2575fc" />
            </linearGradient>
          </defs>
          <path d="M0,40 C30,20 70,60 110,40 C150,20 190,60 230,40 C270,20 310,60 350,40 C390,20 430,60 470,40 C510,20 550,60 600,30" 
                fill="none" stroke="url(#snakeGrad)" stroke-width="4" stroke-linecap="round" stroke-dasharray="200" stroke-dashoffset="0">
            <animate attributeName="stroke-dashoffset" from="400" to="0" dur="3s" repeatCount="indefinite" />
          </path>
          <circle r="6" fill="#a970ff">
            <animateMotion dur="3s" repeatCount="indefinite" path="M0,40 C30,20 70,60 110,40 C150,20 190,60 230,40 C270,20 310,60 350,40 C390,20 430,60 470,40 C510,20 550,60 600,30" />
          </circle>
        </svg>
        <p style="font-size:0.8rem; color:#b9a0e0;">🐍 contribution snake animation</p>
      </div>
    </div>
    <!-- Footer wave -->
    <div class="footer-wave"></div>
    <div style="text-align:center; padding:0.5rem; font-size:0.8rem; background:rgba(0,0,0,0.5);">✨ crafted with graphics & animation</div>
  </div>

  <script>
    // Typing animation effect for the dynamic text
    (function() {
      const textArray = [
        "Building RAG Pipelines & AI Chatbots",
        "LangChain | LangGraph | FastAPI | FAISS",
        "Turning Ideas into Deployed AI Products",
        "Multi-modal systems enthusiast"
      ];
      let arrIndex = 0;
      let charIndex = 0;
      let currentText = textArray[arrIndex];
      const typingElement = document.getElementById('typingText');
      
      function type() {
        if (charIndex < currentText.length) {
          typingElement.textContent += currentText.charAt(charIndex);
          charIndex++;
          setTimeout(type, 60);
        } else {
          setTimeout(erase, 2000);
        }
      }
      function erase() {
        if (charIndex > 0) {
          typingElement.textContent = currentText.substring(0, charIndex-1);
          charIndex--;
          setTimeout(erase, 30);
        } else {
          arrIndex = (arrIndex + 1) % textArray.length;
          currentText = textArray[arrIndex];
          setTimeout(type, 400);
        }
      }
      // initial start
      setTimeout(type, 300);
    })();
  </script>
</body>
</html>
