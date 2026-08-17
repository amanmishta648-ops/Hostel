<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Nomad Nest Hostel — Facebook Post</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,300;9..144,500;9..144,600;9..144,700&family=Inter:wght@400;500;600;700&family=JetBrains+Mono:wght@400;500;700&display=swap" rel="stylesheet">
<style>
  :root{
    --dusk-deep:   #1b2a4a;
    --dusk-mid:    #2c3f66;
    --flag-gold:   #e8a93b;
    --flag-red:    #c4432b;
    --pine:        #3f5d4e;
    --paper:       #f2ede3;
    --paper-dark:  #e6ded0;
    --ink:         #241f1a;
  }

  *{box-sizing:border-box; margin:0; padding:0;}

  html,body{
    width:1200px;
    height:630px;
    overflow:hidden;
    background:var(--dusk-deep);
    font-family:'Inter', sans-serif;
  }

  .canvas{
    position:relative;
    width:1200px;
    height:630px;
    background:
      radial-gradient(ellipse 900px 500px at 15% 110%, rgba(196,67,43,0.25), transparent 60%),
      linear-gradient(180deg, #14213d 0%, #223357 55%, #33456e 100%);
    overflow:hidden;
  }

  /* ---------- stars ---------- */
  .stars{
    position:absolute; inset:0;
    background-image:
      radial-gradient(1.5px 1.5px at 60px 40px, rgba(255,255,255,0.55), transparent),
      radial-gradient(1.5px 1.5px at 180px 90px, rgba(255,255,255,0.4), transparent),
      radial-gradient(2px 2px at 320px 30px, rgba(255,255,255,0.5), transparent),
      radial-gradient(1.5px 1.5px at 420px 70px, rgba(255,255,255,0.35), transparent),
      radial-gradient(2px 2px at 560px 50px, rgba(255,255,255,0.55), transparent),
      radial-gradient(1.5px 1.5px at 640px 20px, rgba(255,255,255,0.4), transparent),
      radial-gradient(1.5px 1.5px at 100px 130px, rgba(255,255,255,0.3), transparent),
      radial-gradient(2px 2px at 260px 140px, rgba(255,255,255,0.45), transparent);
    opacity:0.9;
  }

  /* ---------- prayer flag bunting ---------- */
  .bunting{
    position:absolute;
    top:0; left:0; right:0;
    height:70px;
    display:flex;
    align-items:flex-start;
    z-index:5;
  }
  .flag{
    width:38px; height:50px;
    margin-left:6px;
    clip-path: polygon(0 0, 100% 0, 50% 100%);
    box-shadow: 0 2px 4px rgba(0,0,0,0.2);
  }
  .flag:nth-child(5n+1){background:#4a7ba6;}
  .flag:nth-child(5n+2){background:var(--paper);}
  .flag:nth-child(5n+3){background:var(--flag-red);}
  .flag:nth-child(5n+4){background:var(--pine);}
  .flag:nth-child(5n+5){background:var(--flag-gold);}

  /* ---------- mountains ---------- */
  .mountains{
    position:absolute;
    bottom:0; left:0;
    width:760px;
    height:340px;
    z-index:2;
  }

  /* ---------- LEFT: identity panel ---------- */
  .left{
    position:absolute;
    top:0; left:0;
    width:760px; height:630px;
    padding:100px 70px 0 70px;
    z-index:6;
  }

  .eyebrow{
    font-family:'JetBrains Mono', monospace;
    font-size:15px;
    letter-spacing:4px;
    color:var(--flag-gold);
    font-weight:500;
    margin-bottom:22px;
  }

  .hostel-name{
    font-family:'Fraunces', serif;
    font-weight:600;
    font-size:96px;
    line-height:0.95;
    color:var(--paper);
    letter-spacing:-1px;
  }
  .hostel-name em{
    font-style:italic;
    font-weight:300;
    color:var(--flag-gold);
  }

  .tagline{
    margin-top:26px;
    font-size:21px;
    color:#c9d3e6;
    max-width:480px;
    line-height:1.5;
    font-weight:400;
  }

  .coords{
    margin-top:36px;
    font-family:'JetBrains Mono', monospace;
    font-size:14px;
    color:#8fa0c2;
    letter-spacing:1px;
  }

  /* ---------- perforated divider ---------- */
  .divider{
    position:absolute;
    top:0; bottom:0;
    left:772px;
    width:0;
    border-left:3px dashed rgba(242,237,227,0.35);
    z-index:7;
  }
  .notch{
    position:absolute;
    left:772px;
    width:28px; height:28px;
    background:var(--dusk-deep);
    border-radius:50%;
    transform:translateX(-14px);
    z-index:8;
  }
  .notch.top{top:-14px;}
  .notch.bottom{bottom:-14px;}

  /* ---------- RIGHT: boarding pass stub ---------- */
  .stub{
    position:absolute;
    top:0; right:0;
    width:428px; height:630px;
    background:var(--paper);
    padding:44px 38px;
    z-index:6;
    color:var(--ink);
  }

  .stub-label{
    font-family:'JetBrains Mono', monospace;
    font-size:12px;
    letter-spacing:3px;
    color:var(--pine);
    font-weight:700;
  }

  .stub-route{
    display:flex;
    align-items:center;
    justify-content:space-between;
    margin-top:16px;
    padding-bottom:20px;
    border-bottom:1.5px solid var(--paper-dark);
  }
  .route-point{ }
  .route-point .city{
    font-family:'Fraunces', serif;
    font-size:26px;
    font-weight:600;
  }
  .route-point .sub{
    font-family:'JetBrains Mono', monospace;
    font-size:11px;
    color:#8a8172;
    letter-spacing:1px;
    margin-top:2px;
  }
  .route-arrow{
    font-size:20px;
    color:var(--flag-red);
    margin:0 10px;
  }

  .price-block{
    margin-top:26px;
    padding-bottom:22px;
    border-bottom:1.5px solid var(--paper-dark);
  }
  .price-block .label{
    font-family:'JetBrains Mono', monospace;
    font-size:11px;
    letter-spacing:2px;
    color:#8a8172;
  }
  .price-row{
    display:flex;
    align-items:baseline;
    gap:8px;
    margin-top:6px;
  }
  .price-row .amount{
    font-family:'Fraunces', serif;
    font-weight:700;
    font-size:44px;
    color:var(--flag-red);
  }
  .price-row .unit{
    font-size:15px;
    color:#5c5648;
  }
  .price-alt{
    font-size:13px;
    color:#5c5648;
    margin-top:6px;
  }

  .amenities{
    margin-top:20px;
    display:grid;
    grid-template-columns:1fr 1fr;
    row-gap:10px;
    column-gap:8px;
  }
  .amenity{
    font-size:13.5px;
    display:flex;
    align-items:center;
    gap:7px;
    color:var(--ink);
  }
  .amenity::before{
    content:"";
    width:6px; height:6px;
    background:var(--pine);
    border-radius:50%;
    flex-shrink:0;
  }

  .stub-footer{
    position:absolute;
    bottom:40px;
    left:38px;
    right:38px;
  }
  .barcode{
    height:34px;
    background:repeating-linear-gradient(90deg,
      var(--ink) 0px, var(--ink) 2px,
      transparent 2px, transparent 5px,
      var(--ink) 5px, var(--ink) 6px,
      transparent 6px, transparent 10px,
      var(--ink) 10px, var(--ink) 13px,
      transparent 13px, transparent 15px);
    opacity:0.85;
  }
  .contact{
    margin-top:12px;
    font-family:'JetBrains Mono', monospace;
    font-size:12.5px;
    color:#5c5648;
    display:flex;
    justify-content:space-between;
    letter-spacing:0.5px;
  }
</style>
</head>
<body>
<div class="canvas">
  <div class="stars"></div>

  <svg class="mountains" viewBox="0 0 760 340" preserveAspectRatio="none">
    <polygon points="0,340 0,200 120,90 210,180 300,60 410,190 500,110 620,220 700,150 760,210 760,340" fill="#111a30" opacity="0.9"/>
    <polygon points="0,340 0,260 90,170 180,250 260,140 360,240 450,170 560,260 650,190 760,260 760,340" fill="#0a1424" opacity="0.95"/>
    <polygon points="180,250 210,180 240,220 260,140 280,210 300,190" fill="#e9e4d8" opacity="0.55"/>
    <polygon points="360,240 410,190 450,225 500,110 540,215 560,195" fill="#e9e4d8" opacity="0.5"/>
  </svg>

  <div class="bunting">
    <div class="flag" style="margin-left:20px"></div>
    <div class="flag"></div><div class="flag"></div><div class="flag"></div><div class="flag"></div>
    <div class="flag"></div><div class="flag"></div><div class="flag"></div><div class="flag"></div><div class="flag"></div>
    <div class="flag"></div><div class="flag"></div><div class="flag"></div><div class="flag"></div><div class="flag"></div>
    <div class="flag"></div><div class="flag"></div><div class="flag"></div>
  </div>

  <div class="left">
    <div class="eyebrow">POKHARA · NEPAL · BY PHEWA LAKE</div>
    <div class="hostel-name">Nomad<br><em>Nest</em></div>
    <div class="tagline">A basecamp for wanderers — dorm beds and lake-view hammocks, ten minutes' walk from the trekking trailhead.</div>
    <div class="coords">28.2096° N, 83.9856° E &nbsp;·&nbsp; OPEN YEAR-ROUND</div>
  </div>

  <div class="notch top"></div>
  <div class="divider"></div>
  <div class="notch bottom"></div>

  <div class="stub">
    <div class="stub-label">BOARDING PASS — TO ADVENTURE</div>
    <div class="stub-route">
      <div class="route-point">
        <div class="city">HOME</div>
        <div class="sub">EVERYDAY LIFE</div>
      </div>
      <div class="route-arrow">✈</div>
      <div class="route-point">
        <div class="city">PKR</div>
        <div class="sub">NOMAD NEST</div>
      </div>
    </div>

    <div class="price-block">
      <div class="label">FROM</div>
      <div class="price-row">
        <span class="amount">NPR 800</span>
        <span class="unit">/ night · dorm bed</span>
      </div>
      <div class="price-alt">Private rooms from NPR 2,400/night</div>
    </div>

    <div class="amenities">
      <div class="amenity">Free wifi</div>
      <div class="amenity">Breakfast incl.</div>
      <div class="amenity">Rooftop lounge</div>
      <div class="amenity">Lake-view terrace</div>
      <div class="amenity">Trekking desk</div>
      <div class="amenity">Hot showers</div>
      <div class="amenity">24hr check-in</div>
      <div class="amenity">Laundry</div>
    </div>

    <div class="stub-footer">
      <div class="barcode"></div>
      <div class="contact">
        <span>@nomadnesthostel</span>
        <span>nomadnest.com.np</span>
      </div>
    </div>
  </div>
</div>
</body>
</html>
