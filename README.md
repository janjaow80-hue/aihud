    <!-- Open Graph / Facebook Meta Tags -->
    <meta property="og:title" content="KMHUD.STUDIO | The Lunar & Earth Nexus 3.8">
    <meta property="og:description" content="ในห้วงอวกาศอันเวิ้งว้าง... ก้าวเล็กๆ ของมนุษย์คนหนึ่ง ดังกึกก้องไปชั่วนิรันดร์ จากเศษผงธุลีดวงจันทร์ สู่เปลวเพลิงที่กำลังเต้นระบำ ณ ใจกลางโลก">
    <meta property="og:image" content="https://images.unsplash.com/photo-1541185933-ef5d8ed016c2?q=80&w=1000&auto=format&fit=crop">
    <meta property="og:url" content="https://tiny-violet-63f9.janjaow80.workers.dev/">
    <meta property="og:type" content="website">

    <title>KMHUD.STUDIO | The Lunar &amp; Earth Nexus 3.8</title>
    
    <!-- Google Fonts & Icons -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin="">
    <link href="https://fonts.googleapis.com/css2?family=Chakra+Petch:wght@400;600&amp;family=Orbitron:wght@500;700&amp;family=Prompt:wght@300;400;600&amp;display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">

    <style>

        :root {
            --gold: #d4af37;
            --gold-glow: rgba(212, 175, 55, 0.5);
            --bg-dark: #050505;
            --border-color: rgba(212, 175, 55, 0.3);
        }
        
        * { margin: 0; padding: 0; box-sizing: border-box; }
        
        body {
            background-color: var(--bg-dark);
            color: #ffffff;
            font-family: 'Prompt', sans-serif;
            overflow-x: hidden;
            scroll-behavior: smooth;
        }

        /* TOP BAR */
        header {
            position: fixed;
            top: 0; width: 100%;
            padding: 20px 50px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            z-index: 1000;
            background: rgba(5, 5, 5, 0.85);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid var(--border-color);
        }

        .brand-container { display: flex; align-items: center; gap: 15px; }
        .brand {
            font-family: 'Orbitron', sans-serif;
            font-size: 24px;
            font-weight: 700;
            letter-spacing: 5px;
            color: #fff;
        }
        .nexus-badge {
            font-family: 'Chakra Petch', sans-serif;
            font-size: 11px;
            color: var(--gold);
            border: 1px solid var(--border-color);
            padding: 3px 8px;
            border-radius: 4px;
            background: rgba(212, 175, 55, 0.05);
        }

        nav { display: flex; align-items: center; gap: 20px; flex-wrap: wrap; }
        nav a {
            color: #e0e0e0;
            text-decoration: none;
            font-size: 14px;
            transition: 0.3s;
            font-family: 'Chakra Petch', sans-serif;
            display: flex;
            align-items: center;
            gap: 6px;
        }
        nav a:hover { color: var(--gold); }

        .comm-btn {
            background: rgba(255,255,255,0.05);
            border: 1px solid rgba(255,255,255,0.2);
            padding: 8px 20px;
            border-radius: 30px;
            color: #aaa;
            font-family: 'Chakra Petch', sans-serif;
            font-size: 13px;
            cursor: pointer;
            transition: all 0.3s;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        .comm-btn.active {
            border-color: #22c55e;
            color: #22c55e;
            box-shadow: 0 0 15px rgba(34, 197, 94, 0.3);
        }
        .comm-dot { width: 8px; height: 8px; background: #aaa; border-radius: 50%; }
        .comm-btn.active .comm-dot { background: #22c55e; box-shadow: 0 0 8px #22c55e; }

        section {
            padding: 140px 20px 80px 20px;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            border-bottom: 1px solid var(--border-color);
            position: relative;
        }

        /* HERO SECTION */
        .hero {
            position: relative;
            overflow: hidden;
            text-align: center;
        }
        .bg-image {
            position: absolute;
            inset: -5%;
            background-image: url('https://images.unsplash.com/photo-1614730321146-b6fa6a46bcb4?q=80&w=2000&auto=format&fit=crop');
            background-size: cover;
            background-position: center;
            z-index: 1;
        }
        .bg-overlay {
            position: absolute;
            inset: 0;
            background: radial-gradient(circle at center, rgba(5,5,5,0.3) 0%, rgba(5,5,5,0.85) 100%);
            z-index: 2;
        }
        .space-stars {
            position: absolute;
            inset: 0;
            z-index: 2;
            pointer-events: none;
            background-image: radial-gradient(white 1px, transparent 0), radial-gradient(rgba(212,175,55,0.8) 1.5px, transparent 0);
            background-size: 80px 80px, 120px 120px;
            opacity: 0.6;
        }
        .hero-content { position: relative; z-index: 3; max-width: 900px; }
        .archive-tag {
            font-family: 'Chakra Petch', sans-serif;
            font-size: 11px;
            color: var(--gold);
            letter-spacing: 3px;
            margin-bottom: 15px;
            border: 1px solid var(--border-color);
            display: inline-block;
            padding: 5px 15px;
            border-radius: 20px;
            background: rgba(10,15,25,0.6);
        }
        .quote {
            font-style: italic; color: #ccc; font-weight: 300; letter-spacing: 1px;
            margin-bottom: 25px; font-size: 16px; line-height: 1.6;
        }
        .title-sub {
            font-family: 'Orbitron', sans-serif; letter-spacing: 4px;
            color: var(--gold); font-size: 15px; margin-bottom: 15px;
        }
        .main-title {
            font-size: 48px; font-weight: 700; line-height: 1.2;
            margin-bottom: 35px; font-family: 'Orbitron', sans-serif;
        }
        .acts-container {
            display: flex; gap: 20px; justify-content: center; margin-bottom: 40px; flex-wrap: wrap;
        }
        .act-item {
            font-family: 'Chakra Petch', sans-serif; font-size: 14px;
            color: #ddd; background: rgba(10,15,25,0.7); padding: 8px 16px;
            border-radius: 4px; border: 1px solid rgba(255,255,255,0.1);
        }
        .act-item span { color: var(--gold); font-weight: 600; }
        .hero-buttons { display: flex; gap: 15px; justify-content: center; flex-wrap: wrap; }
        .btn-custom {
            padding: 12px 25px; border-radius: 4px; font-family: 'Chakra Petch', sans-serif;
            font-size: 13px; letter-spacing: 1px; text-decoration: none; transition: 0.3s;
            cursor: pointer; display: flex; align-items: center; gap: 8px;
        }
        .btn-gold { background: var(--gold); color: #050505; font-weight: 600; border: none; }
        .btn-gold:hover { background: #fff; box-shadow: 0 0 20px var(--gold-glow); }
        .btn-outline { background: rgba(10,15,25,0.8); color: #fff; border: 1px solid var(--border-color); }
        .btn-outline:hover { border-color: var(--gold); box-shadow: 0 0 15px var(--gold-glow); }

        /* CHRONICLES 6 BLOCKS */
        #chronicles { background: #050505; padding: 100px 20px; }
        .chronicles-header { text-align: center; margin-bottom: 50px; }
        .chronicles-title { font-family: 'Orbitron', sans-serif; font-size: 32px; color: #fff; margin-bottom: 10px; }
        .chronicles-desc { font-family: 'Chakra Petch', sans-serif; font-size: 13px; color: #888; max-width: 600px; margin: 0 auto; line-height: 1.6; }
        .cards-grid {
            display: grid; grid-template-columns: repeat(auto-fit, minmax(340px, 1fr));
            gap: 30px; width: 100%; max-width: 1200px;
        }
        .story-card {
            background: rgba(10, 15, 25, 0.9); border: 1px solid var(--border-color);
            border-radius: 8px; overflow: hidden; transition: 0.4s; display: flex; flex-direction: column;
        }
        .story-card:hover { border-color: var(--gold); box-shadow: 0 15px 40px rgba(212, 175, 55, 0.25); transform: translateY(-6px); }
        .card-img-container { width: 100%; height: 200px; overflow: hidden; border-bottom: 1px solid var(--border-color); }
        .card-img-container img { width: 100%; height: 100%; object-fit: cover; transition: 0.6s; }
        .story-card:hover .card-img-container img { transform: scale(1.08); }
        .story-content { padding: 25px; display: flex; flex-direction: column; flex-grow: 1; }
        .story-tag { font-family: 'Chakra Petch', sans-serif; font-size: 11px; color: var(--gold); margin-bottom: 8px; }
        .story-title { font-family: 'Orbitron', sans-serif; font-size: 17px; color: #fff; margin-bottom: 12px; }
        .story-text { font-size: 13px; color: #cfd8dc; line-height: 1.6; margin-bottom: 20px; flex-grow: 1; }
        .read-more-btn {
            display: inline-flex; align-items: center; gap: 8px; font-family: 'Chakra Petch', sans-serif;
            font-size: 13px; color: var(--gold); background: none; border: none; cursor: pointer; text-align: left;
        }
        .read-more-btn:hover { color: #fff; text-shadow: 0 0 8px var(--gold); }

        /* YOUTUBE DYNAMIC SECTION */
        #youtube-section { background: #070913; padding: 100px 20px; border-bottom: 1px solid var(--border-color); }
        .yt-container { max-width: 800px; width: 100%; margin: 0 auto; }
        .yt-card {
            background: rgba(10, 15, 25, 0.95); border: 1px solid var(--border-color);
            border-radius: 10px; overflow: hidden; box-shadow: 0 15px 40px rgba(0,0,0,0.8);
        }
        .yt-thumbnail-wrapper { position: relative; width: 100%; padding-top: 56.25%; background: #000; }
        .yt-thumbnail-wrapper img { position: absolute; top: 0; left: 0; width: 100%; height: 100%; object-fit: cover; }
        .yt-info { padding: 25px; }
        .yt-channel { font-family: 'Chakra Petch', sans-serif; font-size: 12px; color: var(--gold); margin-bottom: 8px; }
        .yt-title { font-family: 'Orbitron', sans-serif; font-size: 18px; color: #fff; margin-bottom: 12px; }
        .yt-desc { font-size: 13px; color: #aaa; line-height: 1.6; margin-bottom: 20px; }
        .yt-btn {
            display: inline-flex; align-items: center; gap: 8px; background: #ff0000; color: #fff;
            padding: 10px 20px; border-radius: 4px; text-decoration: none; font-family: 'Chakra Petch', sans-serif;
            font-size: 13px; font-weight: 600; transition: 0.3s;
        }
        .yt-btn:hover { background: #cc0000; box-shadow: 0 0 15px rgba(255,0,0,0.4); }

        /* EARTH NEXUS 3D SECTION */
        #earth-nexus { background: #050505; }
        .nexus-wrapper { display: flex; align-items: center; justify-content: center; gap: 30px; width: 100%; max-width: 1200px; margin: 20px 0; flex-wrap: wrap; }
        .panel { background: rgba(10, 15, 25, 0.8); border: 1px solid var(--border-color); padding: 20px; width: 240px; border-radius: 6px; }
        .panel-item { margin-bottom: 18px; }
        .panel-label { font-size: 10px; color: #888; display: block; margin-bottom: 4px; font-family: 'Chakra Petch', sans-serif; }
        .panel-value { font-size: 17px; color: var(--gold); font-weight: bold; font-family: 'Orbitron', sans-serif; }
        #canvas-container {
            width: 420px; height: 420px; position: relative;
            background: radial-gradient(circle, #0a1128 0%, #03050a 100%);
            border-radius: 50%; border: 1px solid var(--border-color); overflow: hidden; flex-shrink: 0;
        }
        .warp-btn {
            margin-top: 20px; padding: 15px 40px; background: transparent; border: 1px solid #ff4d4d;
            color: #ff4d4d; font-family: 'Chakra Petch', sans-serif; font-size: 15px; letter-spacing: 2px;
            cursor: pointer; transition: 0.3s; border-radius: 4px; text-decoration: none; display: inline-block;
        }
        .warp-btn:hover { background: #ff4d4d; color: #000; box-shadow: 0 0 25px #ff4d4d; }

        /* RESERVATION SECTION */
        #reservation { background: radial-gradient(circle at center, #0a111a 0%, #050505 90%); }
        .reservation-box {
            background: rgba(10, 15, 25, 0.9); border: 1px solid var(--border-color);
            padding: 40px; width: 100%; max-width: 600px; border-radius: 8px; text-align: center;
        }
        .form-group { text-align: left; margin-bottom: 20px; }
        .reservation-box label { display: block; font-size: 12px; font-family: 'Chakra Petch', sans-serif; color: var(--gold); margin-bottom: 8px; }
        .reservation-box input, .reservation-box select {
            width: 100%; padding: 12px 15px; background: rgba(255,255,255,0.05);
            border: 1px solid rgba(212,175,55,0.3); color: #fff; font-family: 'Prompt', sans-serif; border-radius: 4px; font-size: 14px;
        }
        .submit-btn {
            background: var(--gold); color: #000; border: none; width: 100%; padding: 14px;
            font-family: 'Chakra Petch', sans-serif; font-size: 15px; font-weight: 600; cursor: pointer; border-radius: 4px; margin-top: 10px;
        }
        .submit-btn:hover { background: #fff; box-shadow: 0 0 20px var(--gold-glow); }
        .success-ticket {
            display: none; text-align: left; background: rgba(0, 255, 100, 0.05);
            border: 1px solid #22c55e; padding: 20px; border-radius: 6px; margin-top: 15px;
        }

        /* MODAL */
        .modal-overlay {
            position: fixed; inset: 0; background: rgba(0, 0, 0, 0.85); backdrop-filter: blur(12px);
            z-index: 9999; display: flex; align-items: center; justify-content: center; opacity: 0; pointer-events: none; transition: 0.3s; padding: 20px;
        }
        .modal-overlay.active { opacity: 1; pointer-events: auto; }
        .modal-box {
            background: rgba(12, 18, 30, 0.95); border: 1px solid var(--gold); border-radius: 12px;
            max-width: 700px; width: 100%; max-height: 85vh; overflow-y: auto;
        }
        .modal-header-img { width: 100%; height: 280px; object-fit: cover; border-bottom: 1px solid var(--border-color); }
        .modal-body { padding: 30px; }
        .modal-close-btn { background: var(--gold); color: #000; border: none; padding: 10px 25px; font-family: 'Chakra Petch', sans-serif; font-weight: 600; cursor: pointer; border-radius: 4px; }
    </style>
</head>
<body>

    <audio id="bg-audio" loop>
        <source src="https://cdn.pixabay.com/download/audio/2022/02/10/audio_fc86950293.mp3" type="audio/mpeg">
    </audio>

    <!-- Top Bar -->
    <header>
        <div class="brand-container">
            <div class="brand">KMHUD.STUDIO</div>
            <div class="nexus-badge">NEXUS 3.8</div>
        </div>
        <nav>
            <a href="#chronicles"><i class="fa-solid fa-book-open"></i> มหากาพย์</a>
            <a href="#youtube-section"><i class="fa-brands fa-youtube"></i> ข้อมูลยูทูป</a>
            <a href="#earth-nexus"><i class="fa-solid fa-globe"></i> สาระบบโลก</a>
            <a href="#reservation"><i class="fa-solid fa-ticket"></i> สำรองที่นั่ง VIP</a>
        </nav>
        <button class="comm-btn active" id="comm-toggle">
            <span class="comm-dot"></span>
            <span id="comm-text">COMM: ONLINE</span>
        </button>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="hero-container">
        <div class="bg-image"></div>
        <div class="space-stars"></div>
        <div class="bg-overlay"></div>
        <div class="hero-content">
            <div class="archive-tag">EXCLUSIVE ARCHIVE // MEMBER PRIVILEGE</div>
            <p class="quote">"ในห้วงอวกาศอันเวิ้งว้าง... ก้าวเล็กๆ ของมนุษย์คนหนึ่ง ดังกึกก้องไปชั่วนิรันดร์<br>จากเศษผงธุลีดวงจันทร์ สู่เปลวเพลิงที่กำลังเต้นระบำ ณ ใจกลางโลก"</p>
            <div class="title-sub">THE LUNAR &amp; CORE CHRONICLE</div>
            <h1 class="main-title">มหากาพย์ก้าวแรก<br>สู่ธรณิมิตแกนพิภพ</h1>
            
            <div class="acts-container">
                <div class="act-item"><span>ACT I :</span> THE IGNITION</div>
                <div class="act-item"><span>ACT II :</span> THE FAR SIDE</div>
                <div class="act-item"><span>ACT III :</span> GEODYNAMO</div>
            </div>

            <div class="hero-buttons">
                <a href="#chronicles" class="btn-custom btn-gold"><i class="fa-solid fa-book-open"></i> อ่านบันทึกมหากาพย์</a>
                <a href="#youtube-section" class="btn-custom btn-outline" style="border-color: #ff0000; color: #ff5555;"><i class="fa-brands fa-youtube"></i> ข้อมูล YouTube</a>
                <a href="#earth-nexus" class="btn-custom btn-outline"><i class="fa-solid fa-compass"></i> สาระบบสังเกตการณ์ 3.8</a>
                <a href="#reservation" class="btn-custom btn-outline"><i class="fa-solid fa-user-shield"></i> สำรองที่นั่ง VIP</a>
            </div>
        </div>
    </section>
    <!-- Chronicles Section (6 Blocks) -->
    <section id="chronicles">
        <div class="chronicles-header">
            <div style="font-family: 'Chakra Petch', sans-serif; font-size: 11px; color: var(--gold); letter-spacing: 3px; margin-bottom: 10px;">ROADMAP TO DEEP SPACE // EXCLUSIVE ARCHIVE</div>
            <h2 class="chronicles-title">MISSION PROGRESSION: จากอดีตสู่อนาคต</h2>
            <p class="chronicles-desc">เส้นทางแห่งการสำรวจจากรากฐานยุคบุกเบิก สู่การตั้งถิ่นฐานในห้วงอวกาศลึกและดาวเคราะห์เพื่อนบ้าน</p>
        </div>
<div class="youtube-shorts-container" style="position: relative; width: 100%; max-width: 315px; aspect-ratio: 9 / 16; margin: 20px auto;">
  <iframe 
    src="https://www.youtube.com/embed/H5eNm1fM8B0" 
    title="KMHUD.STUDIO Shorts" 
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border-radius: 12px; border: none;" 
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
    allowfullscreen>
  </iframe>
</div>
</style>
       <div class="cards-grid">
            <div class="story-card">
                <div class="card-img-container"><img src="https://images.unsplash.com/photo-1541185933-ef5d8ed016c2?q=80&amp;w=1000&amp;auto=format&amp;fit=crop" alt="Apollo"></div>
                <div class="story-content">
                    <div class="story-tag">CHRONICLE 01 // 1969 APOLLO TOUCHDOWN</div>
                    <div class="story-title">แสงวาบแรกกับการจุดระเบิด (The Ignition)</div>
                    <p class="story-text">เสียงคำรามของเครื่องยนต์ Saturn V ขับเคลื่อนมวลมนุษย์ ฉีกผ่านแรงโน้มถ่วง มุ่งหน้าสู่มหาสมุทรแห่งความเงียบงัน</p>
                    <button class="read-more-btn" onclick="triggerWarpAlert()">อ่านเพิ่มเติม →</button>
                </div>
            </div>
            <div class="story-card">
                <div class="card-img-container"><img src="https://images.unsplash.com/photo-1506703719100-a0f3a48c0f86?q=80&amp;w=1000&amp;auto=format&amp;fit=crop" alt="Radio"></div>
                <div class="story-content">
                    <div class="story-tag">CHRONICLE 02 // RADIO SILENCE</div>
                    <div class="story-title">ความลับบนเงามืดที่ไร้เสียงสะท้อน</div>
                    <p class="story-text">เมื่อยานอวกาศเคลื่อนผ่านเข้าสู่ด้านไกลของดวงจันทร์ สัญญาณวิทยุจากโลกถูกตัดขาด มนุษย์เผชิญหน้ากับความเงียบอันลึกซึ้ง</p>
                    <button class="read-more-btn" onclick="triggerWarpAlert()">อ่านเพิ่มเติม →</button>
                </div>
            </div>
            <div class="story-card">
                <div class="card-img-container"><img src="https://images.unsplash.com/photo-1446776811953-b23d57bd21aa?q=80&amp;w=1000&amp;auto=format&amp;fit=crop" alt="Core"></div>
                <div class="story-content">
                    <div class="story-tag">CHRONICLE 03 // 6,371 KM DEPTH</div>
                    <div class="story-title">ไดนาโมพลังงานใต้แกนโลก</div>
                    <p class="story-text">ลึกลงไปใต้เปลือกหินคือโลหะเหลวร้อนราว 4,000-5,000°C การหมุนวนของมันสร้างสนามแม่เหล็กที่ปกป้องโลก</p>
                    <button class="read-more-btn" onclick="triggerWarpAlert()">อ่านเพิ่มเติม →</button>
                </div>
            </div>
            <div class="story-card">
                <div class="card-img-container"><img src="https://images.unsplash.com/photo-1618005182384-a83a8bd57fbe?q=80&amp;w=1000&amp;auto=format&amp;fit=crop" alt="Grid"></div>
                <div class="story-content">
                    <div class="story-tag">CHRONICLE 04 // THE LUNAR GRID</div>
                    <div class="story-title">โครงข่ายพลังงานดาวบริวาร</div>
                    <p class="story-text">การสร้างสถานีส่งกำลังไฟฟ้าและขุดเจาะน้ำแข็งที่ขั้วดวงจันทร์ เพื่อเป็นฐานเสบียงหลักและจุดเติมเชื้อเพลิง</p>
                    <button class="read-more-btn" onclick="triggerWarpAlert()">อ่านเพิ่มเติม →</button>
                </div>
            </div>
            <div class="story-card">
                <div class="card-img-container"><img src="https://images.unsplash.com/photo-1502134249126-9f3755a50d78?q=80&amp;w=1000&amp;auto=format&amp;fit=crop" alt="Mars"></div>
                <div class="story-content">
                    <div class="story-tag">CHRONICLE 05 // MARS HORIZON</div>
                    <div class="story-title">นิคมมนุษยชาติแห่งดาวอังคาร</div>
                    <p class="story-text">การตั้งถิ่นฐานถาวรแห่งแรกบนดาวอังคาร พัฒนาระบบปิดในการผลิตออกซิเจนและอาหาร</p>
                    <button class="read-more-btn" onclick="triggerWarpAlert()">อ่านเพิ่มเติม →</button>
                </div>
            </div>
            <div class="story-card">
                <div class="card-img-container"><img src="https://images.unsplash.com/photo-1507499739999-097706ad8914?q=80&amp;w=1000&amp;auto=format&amp;fit=crop" alt="Deep Space"></div>
                <div class="story-content">
                    <div class="story-tag">CHRONICLE 06 // DEEP SPACE</div>
                    <div class="story-title">ขอบเขตห้วงอวกาศลึก</div>
                    <p class="story-text">ก้าวข้ามระบบสุริยะด้วยเทคโนโลยีขับเคลื่อนความเร็วสูง เปิดประตูสู่การสำรวจดาวเคราะห์นอกระบบ</p>
                    <button class="read-more-btn" onclick="triggerWarpAlert()">อ่านเพิ่มเติม →</button>
                </div>
            </div>
        </div>
    </section>

    <!-- YouTube Dynamic API Section -->
    <section id="youtube-section">
        <div style="text-align: center; margin-bottom: 40px;">
            <div style="font-family: 'Chakra Petch', sans-serif; font-size: 11px; color: var(--gold); letter-spacing: 3px; margin-bottom: 10px;">LIVE API FEED // YOUTUBE DATA</div>
            <h2 style="font-family: 'Orbitron', sans-serif; font-size: 28px; color: #fff;">วิดีโอแนะนำจากระบบสตรีมมิ่ง</h2>
        </div>

        <div class="yt-container">
            <div class="yt-card">
                <div class="yt-thumbnail-wrapper">
                    <img id="yt-img" src="https://i.ytimg.com/vi/dQw4w9WgXcQ/maxresdefault.jpg" alt="Thumbnail">
                </div>
                <div class="yt-info">
                    <div class="yt-channel" id="yt-channel">CHANNEL: RICK ASTLEY</div>
                    <h3 class="yt-title" id="yt-title">Rick Astley - Never Gonna Give You Up (Official Video)</h3>
                    <p class="yt-desc" id="yt-desc">The official video for “Never Gonna Give You Up” was a global smash on its release in July 1987...</p>
                    <a id="yt-link" href="https://youtube.com/shorts/tcSWOS1yq7s?si=aY6tSRbA05HkBdx1" target="_blank" class="yt-btn">
                        <i class="fa-brands fa-youtube"></i> รับชมวิดีโอบบน YouTube
                    </a>
                </div>
            </div>
        </div>
    </section>
<!-- Earth Nexus Section -->
<section id="earth-nexus" style="text-align: center; padding: 40px 20px;">
    <h2 style="color: var(--gold); letter-spacing: 2px; margin-bottom: 5px; font-family: 'Orbitron', sans-serif;">สาระบบโลกและสนามพลังแม่เหล็ก</h2>
    <p style="color: #888; font-size: 13px; margin-bottom: 30px; font-family: 'Chakra Petch', sans-serif;">ระบบจำลองดาวเทียมและพิกัดวงโคจรโลกเสมือนจริงแบบเรียลไทม์</p>
    
    <div class="nexus-wrapper" style="display: flex; justify-content: center; align-items: center; gap: 30px; flex-wrap: wrap;">
        <!-- Panel ซ้าย -->
        <div class="panel" style="background: rgba(10, 15, 30, 0.8); border: 1px solid rgba(56, 189, 248, 0.3); padding: 20px; border-radius: 8px; text-align: left; width: 240px;">
            <div class="panel-item" style="margin-bottom: 15px;"><span class="panel-label" style="display: block; font-size: 10px; color: #888;">ORBITAL VELOCITY</span><span class="panel-value" style="font-size: 18px; color: #fff; font-family: 'Orbitron', sans-serif;">29.78 <span style="font-size:11px; color:#38bdf8;">KM/S</span></span></div>
            <div class="panel-item" style="margin-bottom: 15px;"><span class="panel-label" style="display: block; font-size: 10px; color: #888;">LUNAR SEPARATION</span><span class="panel-value" style="font-size: 18px; color: #fff; font-family: 'Orbitron', sans-serif;">384,400 <span style="font-size:11px; color:#38bdf8;">KM</span></span></div>
            <div class="panel-item"><span class="panel-label" style="display: block; font-size: 10px; color: #888;">GEOMAGNETIC FLUX</span><span class="panel-value" style="font-size: 18px; color: #fff; font-family: 'Orbitron', sans-serif;">0.65 <span style="font-size:11px; color:#38bdf8;">GAUSS</span></span></div>
        </div>

        <!-- Canvas แสดงผล 3 มิติ -->
        <div style="display: flex; flex-direction: column; align-items: center;">
            <div id="canvas-container" style="width: 418px; height: 418px; position: relative; border-radius: 50%; overflow: hidden; background: radial-gradient(circle, #050b14 0%, #000000 100%); box-shadow: 0 0 30px rgba(56, 189, 248, 0.2);"></div>
            <p style="font-size: 11px; color: var(--gold); margin-top: 12px; font-family: 'Chakra Petch', sans-serif;">⟳ คลิกลากเพื่อหมุนสำรวจโลก 3 มิติ</p>
        </div>

        <!-- Panel ขวา -->
        <div class="panel" style="background: rgba(10, 15, 30, 0.8); border: 1px solid rgba(56, 189, 248, 0.3); padding: 20px; border-radius: 8px; text-align: left; width: 240px;">
            <div class="panel-item" style="margin-bottom: 15px;"><span class="panel-label" style="display: block; font-size: 10px; color: #888;">CORE TEMPERATURE</span><span class="panel-value" style="font-size: 18px; color: #fff; font-family: 'Orbitron', sans-serif;">6,000 <span style="font-size:11px; color:#38bdf8;">°C</span></span></div>
            <div class="panel-item" style="margin-bottom: 15px;"><span class="panel-label" style="display: block; font-size: 10px; color: #888;">CORE COMPOSITION</span><span class="panel-value" style="font-size: 18px; color: #fff; font-family: 'Orbitron', sans-serif;">85% <span style="font-size:11px; color:#38bdf8;">FE-NI</span></span></div>
            <div class="panel-item"><span class="panel-label" style="display: block; font-size: 10px; color: #888;">SCHUMANN RESONANCE</span><span class="panel-value" style="font-size: 18px; color: #fff; font-family: 'Orbitron', sans-serif;">7.83 <span style="font-size:11px; color:#38bdf8;">HZ</span></span></div>
        </div>
    </div>
    <a href="#reservation" class="warp-btn" style="display: inline-block; margin-top: 30px; padding: 12px 30px; background: linear-gradient(135deg, #38bdf8, #1d4ed8); color: #fff; text-decoration: none; border-radius: 4px; font-family: 'Orbitron', sans-serif; font-weight: bold; letter-spacing: 1px;">กดเข้าวาปไปในแกนโลก [INITIATE CORE WARP]</a>
</section>

<!-- Three.js Realistic Script -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
<script>
    const container = document.getElementById('canvas-container');
    const scene = new THREE.Scene();
    const camera = new THREE.PerspectiveCamera(45, 1, 0.1, 1000);
    camera.position.z = 2.7;

    const renderer = new THREE.WebGLRenderer({ antialias: true, alpha: true });
    renderer.setSize(418, 418);
    renderer.setPixelRatio(window.devicePixelRatio);
    container.innerHTML = '';
    container.appendChild(renderer.domElement);

    const earthGroup = new THREE.Group();
    scene.add(earthGroup);

    // จัดแสงสว่าง
    scene.add(new THREE.AmbientLight(0x333333, 1.5));
    const sunLight = new THREE.DirectionalLight(0xffffff, 2.0);
    sunLight.position.set(5, 3, 5);
    scene.add(sunLight);

    // โหลดเท็กเจอร์พื้นผิวโลกแบบสมจริง
    const textureLoader = new THREE.TextureLoader();
    const earthGeometry = new THREE.SphereGeometry(1, 64, 64);
    
    const earthMaterial = new THREE.MeshStandardMaterial({
        roughness: 0.6,
        metalness: 0.1,
        map: textureLoader.load('https://threejs.org/examples/textures/planets/earth_atmos_2048.jpg'),
        bumpMap: textureLoader.load('https://threejs.org/examples/textures/planets/earth_normal_2048.jpg'),
        bumpScale: 0.03,
        specularMap: textureLoader.load('https://threejs.org/examples/textures/planets/earth_specular_2048.jpg')
    });

    const earthMesh = new THREE.Mesh(earthGeometry, earthMaterial);
    earthGroup.add(earthMesh);

    // ชั้นบรรยากาศเรืองแสงรอบโลก (Atmosphere Glow)
    const atmosphereGeometry = new THREE.SphereGeometry(1.03, 64, 64);
    const atmosphereMaterial = new THREE.MeshStandardMaterial({
        color: 0x3b82f6,
        transparent: true,
        opacity: 0.2,
        blending: THREE.AdditiveBlending,
        side: THREE.BackSide
    });
    earthGroup.add(new THREE.Mesh(atmosphereGeometry, atmosphereMaterial));

    // เพิ่มวงโคจรดาวเทียมรอบโลก
    const orbitGroup = new THREE.Group();
    const orbitMat = new THREE.LineBasicMaterial({ color: 0x38bdf8, transparent: true, opacity: 0.4 });

    for (let i = 0; i < 3; i++) {
        const points = [];
        const radius = 1.18 + (i * 0.08);
        for (let j = 0; j <= 100; j++) {
            const theta = (j / 100) * Math.PI * 2;
            points.push(new THREE.Vector3(Math.cos(theta) * radius, 0, Math.sin(theta) * radius));
        }
        const orbitGeo = new THREE.BufferGeometry().setFromPoints(points);
        const orbitLine = new THREE.Line(orbitGeo, orbitMat);
        orbitLine.rotation.x = Math.random() * Math.PI;
        orbitLine.rotation.z = Math.random() * Math.PI;
        orbitGroup.add(orbitLine);
    }
    earthGroup.add(orbitGroup);

    // ควบคุมการหมุนด้วยเมาส์
    let isDragging = false, prevMouse = { x: 0, y: 0 };
    container.addEventListener('mousedown', (e) => { isDragging = true; prevMouse = { x: e.clientX, y: e.clientY }; });
    window.addEventListener('mousemove', (e) => {
        if (!isDragging) return;
        earthGroup.rotation.y += (e.clientX - prevMouse.x) * 0.005;
        earthGroup.rotation.x += (e.clientY - prevMouse.y) * 0.005;
        prevMouse = { x: e.clientX, y: e.clientY };
    });
    window.addEventListener('mouseup', () => { isDragging = false; });

    // ลูปอนิเมชัน
    function animate() {
        requestAnimationFrame(animate);
        if (!isDragging) {
            earthGroup.rotation.y += 0.001;
            orbitGroup.rotation.y -= 0.0005;
        }
        renderer.render(scene, camera);
    }
    animate();
</script>

    <!-- Reservation Section -->
    <section id="reservation">
        <div class="reservation-box">
            <h2 style="color: var(--gold); font-family: 'Orbitron', sans-serif; margin-bottom: 8px; font-size: 22px;">สำรองที่นั่ง VIP ของคุณ</h2>
            <p style="color: #aaa; font-size: 13px; margin-bottom: 25px; font-family: 'Chakra Petch', sans-serif;">กรอกข้อมูลให้ครบถ้วนเพื่อลงทะเบียนเข้าร่วมภารกิจพิเศษ</p>
            
            <form id="reservation-form">
                <div class="form-group">
                    <label>ชื่อ-นามสกุล / โค้ดเนม (NAME)</label>
                    <input type="text" id="res-name" placeholder="ระบุชื่อของคุณ" required>
                </div>
                <div class="form-group">
                    <label>ช่องทางติดต่อสื่อสาร (COMMUNICATION CHANNEL)</label>
                    <input type="email" id="res-email" placeholder="name@domain.com" required>
                </div>
                <div class="form-group">
                    <label>ระดับที่นั่งและการสมัครสมาชิก (VIP TIER)</label>
                    <select id="res-tier" required>
                        <option value="" disabled selected>-- เลือกระดับที่นั่ง / รอบสมาชิก --</option>
                        <option value="Commander Class">Commander Class (ระดับผู้บัญชาการ)</option>
                        <option value="Pilot Class">Pilot Class (ระดับนักบินอวกาศ)</option>
                        <option value="Observer Class">Observer Class (ระดับผู้สังเกตการณ์)</option>
                        <option value="Monthly Member Pass">Monthly Member Pass (สมาชิกรายเดือน)</option>
                    </select>
                </div>
                <button type="submit" class="submit-btn">ยืนยันการสำรองที่นั่ง [CONFIRM RESERVATION]</button>
            </form>

            <div id="success-ticket-card" class="success-ticket">
                <h3 style="color: #22c55e; font-family: 'Orbitron', sans-serif; margin-bottom: 10px;"><i class="fa-solid fa-circle-check"></i> ลงทะเบียนสำเร็จ!</h3>
                <p>รหัสตั๋ว VIP: <span id="out-ticket-id" style="color:var(--gold); font-weight:bold;"></span></p>
                <p>ชื่อ: <span id="out-name" style="color:#fff;"></span></p>
                <p>แพ็กเกจ: <span id="out-tier" style="color:var(--gold);"></span></p>
            </div>
        </div>
    </section>

    <!-- Modal Popup -->
    <div class="modal-overlay" id="storyModal" onclick="closeModalOutside(event)">
        <div class="modal-box">
            <img id="modalImg" src="" alt="Modal Image" class="modal-header-img">
            <div class="modal-body">
                <div id="modalTag" class="modal-tag" style="color:var(--gold); font-size:12px; margin-bottom:10px;"></div>
                <h3 id="modalTitle" class="modal-title" style="font-family:'Orbitron', sans-serif; font-size:20px; color:#fff; margin-bottom:15px;"></h3>
                <p id="modalText" class="modal-full-text" style="font-size:14px; color:#d1d5db; line-height:1.8; margin-bottom:20px;"></p>
                <button class="modal-close-btn" onclick="closeModal()">ปิดหน้าต่าง [CLOSE]</button>
            </div>
        </div>
    </div>

    <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
    <script>
        // Modal Data
        const storyData = {
            1: { tag: "CHRONICLE 01 // 1969 APOLLO", title: "แสงวาบแรกกับการจุดระเบิด", text: "เสียงคำรามของเครื่องยนต์ Saturn V ขับเคลื่อนมวลมนุษย์ ฉีกผ่านแรงโน้มถ่วง มุ่งหน้าสู่มหาสมุทรแห่งความเงียบงัน", img: "https://images.unsplash.com/photo-1541185933-ef5d8ed016c2?q=80&w=1000&auto=format&fit=crop" },
            2: { tag: "CHRONICLE 02 // RADIO SILENCE", title: "ความลับบนเงามืดที่ไร้เสียงสะท้อน", text: "เมื่อยานอวกาศเคลื่อนผ่านเข้าสู่ด้านไกลของดวงจันทร์ สัญญาณวิทยุจากโลกถูกตัดขาดโดยสิ้นเชิง", img: "https://images.unsplash.com/photo-1506703719100-a0f3a48c0f86?q=80&w=1000&auto=format&fit=crop" },
            3: { tag: "CHRONICLE 03 // 6,371 KM DEPTH", title: "ไดนาโมพลังงานใต้แกนโลก", text: "ลึกลงไปใต้เปลือกหินคือโลหะเหลวร้อนราว 4,000-5,000 องศาเซลเซียส สร้างสนามแม่เหล็กปกป้องโลก", img: "https://images.unsplash.com/photo-1446776811953-b23d57bd21aa?q=80&w=1000&auto=format&fit=crop" },
            4: { tag: "CHRONICLE 04 // LUNAR GRID", title: "โครงข่ายพลังงานดาวบริวาร", text: "การสร้างสถานีส่งกำลังไฟฟ้าและขุดเจาะน้ำแข็งที่บริเวณขั้วดวงจันทร์ เพื่อเป็นฐานเสบียงหลัก", img: "https://images.unsplash.com/photo-1618005182384-a83a8bd57fbe?q=80&w=1000&auto=format&fit=crop" },
            5: { tag: "CHRONICLE 05 // MARS HORIZON", title: "นิคมมนุษยชาติแห่งดาวอังคาร", text: "การตั้งถิ่นฐานถาวรแห่งแรกบนดาวอังคาร ด้วยระบบปิดอัจฉริยะ (Closed-Loop Ecosystem)", img: "https://images.unsplash.com/photo-1502134249126-9f3755a50d78?q=80&w=1000&auto=format&fit=crop" },
            6: { tag: "CHRONICLE 06 // DEEP SPACE", title: "ขอบเขตห้วงอวกาศลึก", text: "ก้าวข้ามขีดจำกัดระบบสุริยะด้วยเทคโนโลยีขับเคลื่อนความเร็วสูง เปิดประตูสู่ดาวเคราะห์นอกระบบ", img: "https://images.unsplash.com/photo-1507499739999-097706ad8914?q=80&w=1000&auto=format&fit=crop" }
        };

        function openModal(id) {
            const data = storyData[id];
            if (!data) return;
            document.getElementById('modalImg').src = data.img;
            document.getElementById('modalTag').innerText = data.tag;
            document.getElementById('modalTitle').innerText = data.title;
            document.getElementById('modalText').innerText = data.text;
            document.getElementById('storyModal').classList.add('active');
        }
        function closeModal() { document.getElementById('storyModal').classList.remove('active'); }
        function closeModalOutside(e) { if (e.target.id === 'storyModal') closeModal(); }

        // YouTube Dynamic Integration
        const youtubeData = {
            "items": [{
                "id": "dQw4w9WgXcQ",
                "snippet": {
                    "title": "Rick Astley - Never Gonna Give You Up (Official Video) (4K Remaster)",
                    "description": "The official video for “Never Gonna Give You Up” was a global smash on its release in July 1987, topping the charts in 25 countries...",
                    "channelTitle": "Rick Astley",
                    "thumbnails": { "maxres": { "url": "https://i.ytimg.com/vi/dQw4w9WgXcQ/maxresdefault.jpg" } }
                }
            }]
        };

        window.addEventListener('DOMContentLoaded', () => {
            const item = youtubeData.items[0];
            if (item) {
                document.getElementById('yt-channel').innerText = "CHANNEL: " + item.snippet.channelTitle.toUpperCase();
                document.getElementById('yt-title').innerText = item.snippet.title;
                document.getElementById('yt-desc').innerText = item.snippet.description;
                document.getElementById('yt-link').href = "https://www.youtube.com/watch?v=" + item.id;
                if(item.snippet.thumbnails.maxres) document.getElementById('yt-img').src = item.snippet.thumbnails.maxres.url;
            }
        });

        // Comm Audio
        const commBtn = document.getElementById('comm-toggle');
        const commText = document.getElementById('comm-text');
        const audio = document.getElementById('bg-audio');
        let isComm = false;
        commBtn.addEventListener('click', () => {
            isComm = !isComm;
            if (isComm) { audio.volume = 0.4; audio.play(); commBtn.classList.add('active'); commText.innerText = "COMM: ONLINE"; }
            else { audio.pause(); commBtn.classList.remove('active'); commText.innerText = "COMM: MUTE"; }
        });

        // Three.js Globe
        const container = document.getElementById('canvas-container');
        const scene = new THREE.Scene();
        const camera = new THREE.PerspectiveCamera(45, 1, 0.1, 1000);
        camera.position.z = 2.7;
        const renderer = new THREE.WebGLRenderer({ antialias: true, alpha: true });
        renderer.setSize(418, 418);
        container.appendChild(renderer.domElement);

        const earthGroup = new THREE.Group();
        scene.add(earthGroup);
        scene.add(new THREE.AmbientLight(0xffffff, 0.8));
        const pl = new THREE.PointLight(0xffffff, 1.5);
        pl.position.set(5, 3, 5);
        scene.add(pl);

        earthGroup.add(new THREE.Mesh(new THREE.SphereGeometry(1, 32, 32), new THREE.MeshStandardMaterial({ color: 0x1d4ed8, roughness: 0.4, metalness: 0.3 })));
        earthGroup.add(new THREE.Mesh(new THREE.SphereGeometry(1.01, 16, 16), new THREE.MeshBasicMaterial({ color: 0xd4af37, wireframe: true, transparent: true, opacity: 0.25 })));

        let isDragging = false, prevMouse = { x: 0, y: 0 };
        container.addEventListener('mousedown', (e) => { isDragging = true; prevMouse = { x: e.clientX, y: e.clientY }; });
        window.addEventListener('mousemove', (e) => {
            if (!isDragging) return;
            earthGroup.rotation.y += (e.clientX - prevMouse.x) * 0.005;
            earthGroup.rotation.x += (e.clientY - prevMouse.y) * 0.005;
            prevMouse = { x: e.clientX, y: e.clientY };
        });
        window.addEventListener('mouseup', () => { isDragging = false; });

        function animate() {
            requestAnimationFrame(animate);
            if (!isDragging) earthGroup.rotation.y += 0.002;
            renderer.render(scene, camera);
        }
        animate();

        // Reservation Form
        const resForm = document.getElementById('reservation-form');
        resForm.addEventListener('submit', (e) => {
            e.preventDefault();
            const name = document.getElementById('res-name').value.trim();
            const tier = document.getElementById('res-tier').value;
            if (!name || !tier) return;
            const code = 'KMHUD-' + Math.floor(100000 + Math.random() * 900000);
            document.getElementById('out-ticket-id').innerText = code;
            document.getElementById('out-name').innerText = name;
            document.getElementById('out-tier').innerText = tier;
            resForm.style.display = 'none';
            document.getElementById('success-ticket-card').style.display = 'block';
        });
    </script>
 <script>
    // ฟังก์ชันแจ้งเตือนสไตล์ล้ำๆ เมื่อกด "อ่านเพิ่มเติม"
    function triggerWarpAlert() {
        const alertOverlay = document.createElement('div');
        alertOverlay.style.cssText = `
            position: fixed; top: 0; left: 0; width: 100vw; height: 100vh;
            background: rgba(0, 5, 15, 0.85); backdrop-filter: blur(8px);
            display: flex; justify-content: center; align-items: center; z-index: 9999;
            font-family: 'Orbitron', sans-serif; animation: fadeIn 0.3s ease;
        `;

        alertOverlay.innerHTML = `
            <div style="
                background: linear-gradient(135deg, rgba(15, 23, 42, 0.95), rgba(3, 7, 18, 0.95));
                border: 2px solid #38bdf8; box-shadow: 0 0 30px rgba(56, 189, 248, 0.4);
                padding: 30px; border-radius: 12px; text-align: center; max-width: 420px; width: 90%;
                position: relative;
            ">
                <div style="color: #38bdf8; font-size: 12px; letter-spacing: 3px; margin-bottom: 10px;">[ SECURITY CLEARANCE REQUIRED ]</div>
                <h3 style="color: #fff; font-size: 18px; margin-bottom: 15px; letter-spacing: 1px;">สิทธิ์การเข้าถึงข้อมูลลับถูกจำกัด</h3>
                <p style="color: #94a3b8; font-size: 13px; font-family: 'Chakra Petch', sans-serif; margin-bottom: 25px; line-height: 1.6;">
                    โปรดสำรองที่นั่ง รับสิทธิ์วาปแกนโลกเต็มรูปแบบ เพื่อปลดล็อกฐานข้อมูลมหากาพย์และเน็ตเวิร์กทั้งหมด
                </p>
                <div style="display: flex; gap: 10px; justify-content: center;">
                    <button id="warp-action-btn" style="
                        background: linear-gradient(135deg, #38bdf8, #1d4ed8); color: #fff; border: none;
                        padding: 10px 20px; border-radius: 4px; font-family: 'Orbitron', sans-serif; font-weight: bold;
                        cursor: pointer; letter-spacing: 1px; box-shadow: 0 0 15px rgba(56, 189, 248, 0.5);
                    ">ยืนยันสำรองที่นั่ง</button>
                    <button id="warp-close-btn" style="
                        background: transparent; color: #94a3b8; border: 1px solid #475569;
                        padding: 10px 20px; border-radius: 4px; font-family: 'Orbitron', sans-serif;
                        cursor: pointer;
                    ">ปิดหน้าต่าง</button>
                </div>
            </div>
        `;
        document.body.appendChild(alertOverlay);

        document.getElementById('warp-action-btn').onclick = function() {
            document.body.removeChild(alertOverlay);
            const reservationSection = document.getElementById('reservation');
            if (reservationSection) {
                reservationSection.scrollIntoView({ behavior: 'smooth' });
            }
        };

        document.getElementById('warp-close-btn').onclick = function() {
            document.body.removeChild(alertOverlay);
        };
    }
</script>
</body>
