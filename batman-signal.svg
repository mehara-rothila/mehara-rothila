<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 400" width="800" height="400">
  <defs>
    <!-- The Bat Symbol Path -->
    <path id="bat-shape" d="M 50,25 C 50,25 60,35 60,50 C 60,65 55,75 55,75 C 55,75 75,70 85,80 C 85,80 82,60 85,55 C 88,50 92,48 95,50 C 98,52 100,60 100,60 C 100,60 102,52 105,50 C 108,48 112,50 115,55 C 118,60 115,80 115,80 C 125,70 145,75 145,75 C 145,75 140,65 140,50 C 140,35 150,25 150,25 C 150,25 125,40 100,20 C 75,40 50,25 50,25 Z" fill="#000" transform="translate(-100, -50) scale(2)"/>
    
    <!-- Mask for the spotlight beam -->
    <mask id="beam-mask">
      <rect x="0" y="0" width="800" height="400" fill="black" />
      <path d="M 400,350 L 300,50 L 500,50 Z" fill="white">
         <animateTransform attributeName="transform" type="rotate" from="-5 400 350" to="5 400 350" dur="6s" repeatCount="indefinite" values="-5 400 350; 5 400 350; -5 400 350" keyTimes="0; 0.5; 1" />
      </path>
    </mask>

    <!-- Raindrop Symbol -->
    <line id="rain" x1="0" y1="0" x2="0" y2="15" stroke="rgba(255,255,255,0.3)" stroke-width="2" />
  </defs>

  <!-- Sky Background -->
  <rect width="100%" height="100%" fill="#0a0a12" />

  <!-- Moon/Cloud Glow behind signal -->
  <circle cx="400" cy="150" r="100" fill="#2a2a35" filter="url(#blur)">
     <animate attributeName="opacity" values="0.4;0.6;0.4" dur="8s" repeatCount="indefinite" />
  </circle>

  <!-- The Signal Beam -->
  <g opacity="0.8">
      <!-- The Beam Cone -->
      <path d="M 400,450 L 250,-50 L 550,-50 Z" fill="url(#beamGradient)" opacity="0.3">
        <animateTransform attributeName="transform" type="rotate" from="-5 400 450" to="5 400 450" dur="6s" repeatCount="indefinite" values="-5 400 450; 5 400 450; -5 400 450" keyTimes="0; 0.5; 1" />
      </path>
      
      <!-- The Projected Oval Light on Clouds -->
      <ellipse cx="400" cy="120" rx="120" ry="70" fill="#ffeb3b" opacity="0.8">
        <animateTransform attributeName="transform" type="translate" values="-30 0; 30 0; -30 0" dur="6s" repeatCount="indefinite" />
         <!-- Flicker Effect -->
        <animate attributeName="opacity" values="0.7;0.8;0.6;0.8;0.7" dur="0.2s" repeatCount="indefinite" />
      </ellipse>
      
      <!-- The Bat Symbol inside the light -->
      <g transform="translate(300, 70)">
        <path d="M 50,25 C 50,25 60,35 60,50 C 60,65 55,75 55,75 C 55,75 75,70 85,80 C 85,80 82,60 85,55 C 88,50 92,48 95,50 C 98,52 100,60 100,60 C 100,60 102,52 105,50 C 108,48 112,50 115,55 C 118,60 115,80 115,80 C 125,70 145,75 145,75 C 145,75 140,65 140,50 C 140,35 150,25 150,25 C 150,25 125,40 100,20 C 75,40 50,25 50,25 Z" fill="#0a0a12">
            <animateTransform attributeName="transform" type="translate" values="-30 0; 30 0; -30 0" dur="6s" repeatCount="indefinite" />
        </path>
      </g>
  </g>

  <!-- City Skyline Silhouette (Static bottom) -->
  <path d="M0,400 L0,320 L50,320 L50,280 L100,280 L100,340 L150,340 L150,250 L220,250 L220,350 L280,350 L280,300 L350,300 L350,400 Z" fill="#050508" />
  <path d="M800,400 L800,310 L740,310 L740,260 L680,260 L680,330 L620,330 L620,290 L550,290 L550,360 L450,360 L450,400 Z" fill="#050508" />
  
  <!-- Rain Animation Layer -->
  <g stroke="rgba(174, 194, 224, 0.4)" stroke-width="1.5" stroke-linecap="round">
      <style>
          .rain { animation: rainfall 1s linear infinite; }
          .rain-slow { animation: rainfall 2s linear infinite; }
          .rain-fast { animation: rainfall 0.7s linear infinite; }
          
          @keyframes rainfall {
              0% { transform: translateY(-50px); opacity: 0; }
              20% { opacity: 1; }
              100% { transform: translateY(450px); opacity: 0; }
          }
      </style>
      
      <!-- Generating rain drops manually since we can't use JS -->
      <line x1="100" y1="-20" x2="100" y2="0" class="rain" style="animation-delay: 0.2s" />
      <line x1="250" y1="-20" x2="250" y2="0" class="rain-fast" style="animation-delay: 0.5s" />
      <line x1="400" y1="-20" x2="400" y2="0" class="rain" style="animation-delay: 0.1s" />
      <line x1="550" y1="-20" x2="550" y2="0" class="rain-slow" style="animation-delay: 0.8s" />
      <line x1="700" y1="-20" x2="700" y2="0" class="rain-fast" style="animation-delay: 0.3s" />
      
      <line x1="50" y1="-50" x2="50" y2="-30" class="rain-fast" style="animation-delay: 0.7s" />
      <line x1="180" y1="-50" x2="180" y2="-30" class="rain" style="animation-delay: 0.4s" />
      <line x1="320" y1="-50" x2="320" y2="-30" class="rain-slow" style="animation-delay: 0.9s" />
      <line x1="480" y1="-50" x2="480" y2="-30" class="rain" style="animation-delay: 0.2s" />
      <line x1="620" y1="-50" x2="620" y2="-30" class="rain-fast" style="animation-delay: 0.6s" />
      
      <!-- More angled rain for depth -->
      <g opacity="0.5">
          <line x1="120" y1="-20" x2="120" y2="0" class="rain-fast" style="animation-delay: 0.1s" />
          <line x1="380" y1="-20" x2="380" y2="0" class="rain-slow" style="animation-delay: 0.45s" />
          <line x1="580" y1="-20" x2="580" y2="0" class="rain" style="animation-delay: 0.85s" />
      </g>
  </g>

  <!-- Gradient Defs -->
  <defs>
    <linearGradient id="beamGradient" x1="0%" y1="100%" x2="0%" y2="0%">
      <stop offset="0%" stop-color="#ffeb3b" stop-opacity="0.1" />
      <stop offset="100%" stop-color="#ffeb3b" stop-opacity="0" />
    </linearGradient>
    <filter id="blur">
      <feGaussianBlur in="SourceGraphic" stdDeviation="20" />
    </filter>
  </defs>
</svg>
