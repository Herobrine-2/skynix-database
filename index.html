<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Skynix Manager - NextGen</title>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    <!-- Firebase Realtime Live Server SDK -->
    <script src="https://www.gstatic.com/firebasejs/10.8.0/firebase-app-compat.js"></script>
    <script src="https://www.gstatic.com/firebasejs/10.8.0/firebase-database-compat.js"></script>
    <style>
        :root {
            --bg-main: #05070b;
            --bg-card: rgba(11, 16, 25, 0.94);
            --border-color: #1a2332;
            --accent-color: #06b6d4;
            --accent-glow: rgba(6, 182, 212, 0.35);
            --text-main: #f1f5f9;
            --text-muted: #64748b;
            --start-btn-bg: #06b6d4;
            --start-btn-img: none;
            --start-btn-scale: 1;
            
            --widget-top: auto;
            --widget-bottom: 20px;
            --widget-left: auto;
            --widget-right: 20px;
            --widget-scale: 1;
            --border-radius-main: 16px;
        }

        /* Performans Modu (FPS Modu) Aktifken Çalışacak Sınıf */
        body.performance-mode *, body.performance-mode *::before, body.performance-mode *::after {
            backdrop-filter: none !important;
            animation: none !important;
            box-shadow: none !important;
            transition: none !important;
        }
        body.performance-mode {
            background: #020305 !important;
        }
        body.performance-mode .bg-card, body.performance-mode .modal, body.performance-mode .custom-card-frame {
            background: #0a0e17 !important;
        }

        * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Plus Jakarta Sans', sans-serif; user-select: none; }
        
        ::-webkit-scrollbar { width: 8px; height: 8px; }
        ::-webkit-scrollbar-track { background: var(--bg-main); }
        ::-webkit-scrollbar-thumb {
            background: var(--border-color);
            border-radius: 8px;
            border: 2px solid rgba(0,0,0,0.2);
            transition: background 0.3s ease;
        }
        ::-webkit-scrollbar-thumb:hover { background: var(--accent-color); }

        body { 
            background-color: var(--bg-main); color: var(--text-main); 
            overflow: hidden; height: 100vh; width: 100vw; display: flex; flex-direction: column; 
            font-size: 14px; position: relative; transition: background 0.3s ease, color 0.3s ease;
        }

        /* Üst Navigasyon Modu */
        body.top-nav-mode .main-container { flex-direction: column; }
        body.top-nav-mode .sidebar {
            width: 100%; height: 50px; flex-direction: row; padding: 0 20px;
            border-right: none; border-bottom: 1px solid var(--border-color);
            justify-content: flex-start; align-items: center;
        }
        body.top-nav-mode .nav-item {
            border-left: none; border-bottom: 3px solid transparent; height: 100%;
            padding: 0 16px; justify-content: center;
        }
        body.top-nav-mode .nav-item:hover, body.top-nav-mode .nav-item.active {
            border-left-color: transparent; border-bottom-color: var(--accent-color);
            background: rgba(255,255,255,0.03);
        }

        .icon-svg { width: 16px; height: 16px; fill: currentColor; display: inline-block; vertical-align: middle; }
        .icon-lg { width: 22px; height: 22px; }

        /* Sabit Metalik Beyaz Kanat Logosu Stilleri */
        .wings-logo-fixed {
            width: 32px; height: 32px; object-fit: contain;
            filter: drop-shadow(0 0 10px var(--accent-glow));
            transition: transform 0.3s ease;
        }
        .wings-logo-fixed:hover { transform: scale(1.1); }

        .wings-logo-hero-fixed {
            width: 95px; height: 95px; margin-bottom: 8px; object-fit: contain;
            filter: drop-shadow(0 0 25px var(--accent-glow)) drop-shadow(0 0 14px #ffffff);
            animation: wingPulse 3s infinite ease-in-out;
        }
        @keyframes wingPulse {
            0%, 100% { transform: translateY(0) scale(1); }
            50% { transform: translateY(-6px) scale(1.04); }
        }

        /* Arka Plan Görseli */
        #appBackground { position: fixed; top: 0; left: 0; width: 100%; height: 100%; z-index: -1; overflow: hidden; pointer-events: none; }
        #mainAppBackground { width: 100%; height: 100%; object-fit: cover; filter: brightness(0.22); transition: opacity 0.5s ease; }

        /* Toast Bildirimleri */
        #toastContainer { position: fixed; top: 52px; right: 20px; z-index: 9999; display: flex; flex-direction: column; gap: 8px; pointer-events: none; }
        .app-toast {
            background: var(--bg-card); backdrop-filter: blur(12px);
            border: 1px solid var(--accent-color); border-radius: 10px; padding: 12px 18px;
            color: var(--text-main); font-size: 13px; font-weight: 700; box-shadow: 0 10px 30px rgba(0,0,0,0.7);
            display: flex; align-items: center; gap: 10px; animation: toastIn 0.3s ease; pointer-events: auto;
            min-width: 280px; max-width: 400px;
        }
        @keyframes toastIn { from { opacity: 0; transform: translateY(-10px); } to { opacity: 1; transform: translateY(0); } }

        /* Yükleme Ekranı */
        #loadingScreen {
            position: fixed; top: 0; left: 0; width: 100vw; height: 100vh;
            background: #020305; z-index: 9999; display: flex; flex-direction: column;
            justify-content: flex-end; align-items: center; padding-bottom: 90px;
            transition: opacity 0.6s ease, visibility 0.6s ease;
        }
        .loading-title-container { position: absolute; top: 70px; left: 50%; transform: translateX(-50%); z-index: 3; text-align: center; display: flex; flex-direction: column; align-items: center; }
        .loading-app-title { font-size: 42px; font-weight: 800; color: #fff; letter-spacing: 3px; text-transform: uppercase; text-shadow: 0 0 25px var(--accent-glow); }
        .loading-app-sub { font-size: 14px; font-weight: 700; color: var(--accent-color); letter-spacing: 5px; margin-top: 4px; }
        .loading-content { position: relative; z-index: 2; width: 600px; max-width: 90vw; text-align: center; background: var(--bg-card); padding: 24px; border-radius: 16px; border: 1px solid var(--border-color); backdrop-filter: blur(10px); }
        .loading-subtitle { color: var(--text-main); font-size: 14px; margin-bottom: 16px; font-weight: 600; }
        .progress-bar-container { width: 100%; height: 10px; background: rgba(255,255,255,0.08); border-radius: 8px; overflow: hidden; border: 1px solid var(--border-color); }
        .progress-bar { width: 0%; height: 100%; background: linear-gradient(90deg, var(--accent-color), #38bdf8); transition: width 0.3s ease; box-shadow: 0 0 12px var(--accent-color); }

        /* Üst Başlık Çubuğu */
        .titlebar { height: 46px; background: var(--bg-card); backdrop-filter: blur(12px); display: flex; justify-content: space-between; align-items: center; border-bottom: 1px solid var(--border-color); -webkit-app-region: drag; z-index: 100; padding: 0 16px; }
        .titlebar .title { font-size: 13px; font-weight: 800; color: var(--text-main); letter-spacing: 1px; display: flex; align-items: center; gap: 10px; }
        .titlebar-right { display: flex; align-items: center; gap: 12px; height: 100%; -webkit-app-region: no-drag; }

        .client-status-badge {
            display: flex; align-items: center; gap: 6px; font-size: 11px; font-weight: 700;
            background: rgba(16, 185, 129, 0.1); border: 1px solid #10b981; color: #10b981;
            padding: 4px 10px; border-radius: 12px; transition: all 0.3s ease;
        }
        .client-status-badge.disconnected {
            background: rgba(239, 68, 68, 0.1); border-color: #ef4444; color: #ef4444;
        }
        .client-status-dot { width: 8px; height: 8px; border-radius: 50%; background: #10b981; box-shadow: 0 0 8px #10b981; transition: all 0.3s ease; }
        .client-status-badge.disconnected .client-status-dot { background: #ef4444; box-shadow: 0 0 8px #ef4444; }

        .active-status-dot-pulse {
            width: 10px; height: 10px; border-radius: 50%;
            background: #10b981; box-shadow: 0 0 10px #10b981;
            animation: statusPulse 1.8s infinite ease-in-out; display: inline-block;
        }
        @keyframes statusPulse {
            0%, 100% { transform: scale(1); opacity: 1; box-shadow: 0 0 8px #10b981; }
            50% { transform: scale(1.25); opacity: 0.85; box-shadow: 0 0 15px #10b981; }
        }

        .profile-trigger {
            display: flex; align-items: center; gap: 8px; background: var(--bg-card); border: 1px solid var(--border-color);
            padding: 4px 12px; border-radius: 20px; transition: 0.2s; cursor: pointer;
        }
        .profile-trigger:hover { border-color: var(--accent-color); box-shadow: 0 0 10px var(--accent-glow); }
        .profile-avatar-sm { width: 26px; height: 26px; border-radius: 50%; object-fit: cover; border: 1px solid var(--accent-color); }
        .profile-name-sm { font-size: 12px; font-weight: 700; color: var(--text-main); }

        .window-controls { display: flex; height: 100%; }
        .window-controls button { background: transparent; border: none; color: var(--text-muted); width: 40px; height: 100%; font-size: 13px; cursor: pointer; display: flex; align-items: center; justify-content: center; transition: 0.2s; }
        .window-controls button:hover { background: rgba(255,255,255,0.1); color: #fff; }
        .window-controls button.close:hover { background: #ef4444; color: #fff; }

        /* Ana Düzen */
        .main-container { display: flex; flex: 1; height: calc(100vh - 46px); overflow: hidden; position: relative; }
        .sidebar { width: 230px; background: var(--bg-card); backdrop-filter: blur(14px); border-right: 1px solid var(--border-color); display: flex; flex-direction: column; padding: 20px 0; transition: all 0.3s ease; }
        .nav-item { padding: 14px 24px; color: var(--text-muted); font-size: 13px; font-weight: 700; border-left: 4px solid transparent; transition: 0.25s ease; cursor: pointer; display: flex; align-items: center; gap: 12px; }
        .nav-item:hover, .nav-item.active { background: linear-gradient(90deg, var(--accent-glow) 0%, rgba(0,0,0,0) 100%); color: var(--text-main); border-left-color: var(--accent-color); }

        .content-area { flex: 1; padding: 28px; overflow-y: auto; padding-bottom: 140px; }
        .panel { display: none; }
        .panel.active { display: block; animation: panelFade 0.4s cubic-bezier(0.16, 1, 0.3, 1); }
        @keyframes panelFade { from { opacity: 0; transform: translateY(8px); } to { opacity: 1; transform: translateY(0); } }

        /* Home Vitrin Tasarımı & Anime Karakter Görseli */
        .home-hero { display: flex; flex-direction: column; align-items: center; text-align: center; margin-bottom: 28px; position: relative; }
        .home-title { font-size: 36px; font-weight: 800; color: #fff; letter-spacing: 2px; margin-bottom: 4px; text-shadow: 0 0 25px var(--accent-glow); }
        
        .hero-avatar-wrapper {
            margin: 12px 0 10px 0; display: flex; justify-content: center; align-items: center; position: relative;
        }
        .hero-author-avatar {
            width: 86px; height: 86px; border-radius: 50%;
            border: 3px solid var(--accent-color);
            box-shadow: 0 0 25px var(--accent-glow), 0 0 15px rgba(255,255,255,0.5);
            object-fit: cover; transition: transform 0.3s ease, box-shadow 0.3s ease;
            background: #000;
        }
        .hero-author-avatar:hover {
            transform: scale(1.08); box-shadow: 0 0 35px var(--accent-glow), 0 0 20px rgba(255,255,255,0.9);
        }

        .author-badge { 
            font-size: 11px; font-weight: 800; color: #ffffff !important; 
            letter-spacing: 2px; text-transform: uppercase;
            background: var(--accent-glow); padding: 4px 16px; border-radius: 20px; border: 1px solid var(--accent-color);
        }
        .home-subtitle { font-size: 14px; color: var(--text-muted); font-weight: 600; margin-bottom: 18px; margin-top: 12px; max-width: 600px; }

        .home-quick-stats {
            display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 16px; width: 100%; margin-bottom: 24px;
        }
        .quick-stat-box {
            background: var(--bg-card); border: 1px solid var(--border-color); border-radius: var(--border-radius-main);
            padding: 16px 20px; backdrop-filter: blur(12px); display: flex; align-items: center; gap: 16px;
            transition: 0.3s ease;
        }
        .quick-stat-box:hover { border-color: var(--accent-color); transform: translateY(-3px); box-shadow: 0 8px 25px var(--accent-glow); }
        .quick-stat-icon { width: 44px; height: 44px; border-radius: 12px; background: var(--accent-glow); color: var(--accent-color); display: flex; align-items: center; justify-content: center; }
        .quick-stat-val { font-size: 18px; font-weight: 800; color: var(--text-main); }
        .quick-stat-lbl { font-size: 11px; font-weight: 700; color: var(--text-muted); text-transform: uppercase; }

        /* Showcase Izgarası */
        .showcase-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 18px; margin-bottom: 24px; }
        .showcase-card {
            position: relative; height: 160px; border-radius: var(--border-radius-main); overflow: hidden;
            border: 1px solid var(--border-color); transition: 0.3s ease; cursor: pointer;
        }
        .showcase-card:hover { border-color: var(--accent-color); transform: translateY(-4px); box-shadow: 0 10px 30px var(--accent-glow); }
        .showcase-card img { width: 100%; height: 100%; object-fit: cover; object-position: center 20%; filter: brightness(0.7); transition: 0.3s ease; }
        .showcase-card:hover img { filter: brightness(0.9) scale(1.03); }
        .showcase-overlay {
            position: absolute; bottom: 0; left: 0; width: 100%; padding: 16px;
            background: linear-gradient(to top, rgba(5,7,11,0.95) 0%, rgba(5,7,11,0) 100%);
            display: flex; flex-direction: column; gap: 4px;
        }
        .showcase-title { font-size: 15px; font-weight: 800; color: #fff; text-shadow: 0 2px 10px rgba(0,0,0,0.8); }
        .showcase-tag { font-size: 11px; font-weight: 700; color: var(--accent-color); text-transform: uppercase; }

        .discord-btn {
            display: inline-flex; align-items: center; gap: 10px; background: #5865F2; color: #fff;
            padding: 10px 22px; border-radius: 12px; font-size: 13px; font-weight: 800; text-decoration: none;
            transition: all 0.25s ease; box-shadow: 0 6px 20px rgba(88,101,242,0.4); margin-top: 4px;
        }
        .discord-btn:hover { background: #4752C4; transform: translateY(-2px); box-shadow: 0 10px 25px rgba(88,101,242,0.6); }

        .home-dashboard-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 20px; margin-top: 20px; }
        .news-card {
            background: var(--bg-card); border: 1px solid var(--border-color); border-radius: var(--border-radius-main);
            padding: 20px; backdrop-filter: blur(10px); display: flex; flex-direction: column; gap: 10px;
        }
        .news-card-title { font-size: 15px; font-weight: 800; color: var(--accent-color); display: flex; align-items: center; gap: 8px; }
        .news-card-body { font-size: 12px; color: var(--text-main); line-height: 1.6; }

        /* Profil Kartı & Spotify */
        .profile-page-card {
            background: var(--bg-card); border-radius: 20px; border: 1px solid var(--border-color);
            overflow: hidden; box-shadow: 0 15px 40px rgba(0,0,0,0.6); backdrop-filter: blur(12px);
            margin-bottom: 24px;
        }
        .profile-page-banner {
            height: 200px; background-size: cover; background-position: center 20%; position: relative;
            border-bottom: 1px solid var(--border-color); transition: background-image 0.4s ease;
        }
        .profile-page-avatar {
            position: absolute; bottom: -35px; left: 32px; width: 85px; height: 85px;
            border-radius: 50%; border: 4px solid var(--accent-color); object-fit: cover; background: #000;
        }
        .profile-page-body { padding: 48px 32px 28px 32px; }
        .profile-stats-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 16px; margin-top: 20px; }
        .profile-stat-card {
            background: rgba(255,255,255,0.03); border: 1px solid var(--border-color);
            border-radius: 14px; padding: 16px; display: flex; align-items: center; gap: 16px;
        }
        .profile-stat-icon { width: 40px; height: 40px; border-radius: 12px; background: var(--accent-glow); color: var(--accent-color); display: flex; align-items: center; justify-content: center; }
        .profile-stat-val { font-size: 16px; font-weight: 800; color: var(--text-main); }
        .profile-stat-lbl { font-size: 11px; font-weight: 700; color: var(--text-muted); text-transform: uppercase; }

        .spotify-container {
            background: var(--bg-card); border: 1px solid var(--border-color); border-radius: var(--border-radius-main);
            padding: 20px; backdrop-filter: blur(10px); margin-top: 20px;
        }
        .spotify-header { display: flex; align-items: center; gap: 10px; font-weight: 800; font-size: 15px; color: #1DB954; margin-bottom: 12px; }

        /* ŞAMPİYON & SKİN KARTLARI */
        .champion-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(180px, 1fr)); gap: 18px; }
        .champion-card {
            background: var(--bg-card); border-radius: var(--border-radius-main); overflow: hidden; border: 1px solid var(--border-color);
            transition: 0.25s ease; position: relative; display: flex; flex-direction: column; min-height: 290px; cursor: pointer;
        }
        .champion-card:hover { transform: translateY(-6px); border-color: var(--accent-color); box-shadow: 0 10px 25px var(--accent-glow); }
        
        .champ-delete-btn {
            position: absolute; top: 8px; right: 8px; z-index: 10;
            background: rgba(239, 68, 68, 0.85); border: 1px solid #ef4444; color: #fff;
            width: 28px; height: 28px; border-radius: 8px; font-size: 14px;
            display: flex; align-items: center; justify-content: center; cursor: pointer; transition: 0.2s;
        }
        .champ-delete-btn:hover { background: #ef4444; transform: scale(1.1); box-shadow: 0 0 10px rgba(239,68,68,0.5); }

        .champion-card img, .skin-card img { 
            width: 100%; height: 230px; object-fit: cover; object-position: center top; 
            border-bottom: 1px solid var(--border-color); transition: transform 0.3s ease;
        }
        .champion-card:hover img, .skin-card:hover img { transform: scale(1.05); }

        .champion-info { padding: 12px; background: var(--bg-card); display: flex; flex-direction: column; justify-content: space-between; flex: 1; }
        .champion-name { font-size: 14px; font-weight: 800; color: var(--text-main); }
        .champion-title { font-size: 11px; font-weight: 600; color: var(--text-muted); text-transform: uppercase; margin-top: 2px; }

        /* RGB CHROMA BUTONU */
        .rgb-chroma-btn {
            position: absolute; bottom: 65px; left: 50%; transform: translateX(-50%);
            width: 38px; height: 38px; border-radius: 50%;
            background: linear-gradient(135deg, var(--accent-color), #a1783b, var(--accent-color));
            border: 2px solid #05070b; box-shadow: 0 0 15px var(--accent-glow), inset 0 0 6px rgba(0,0,0,0.8);
            cursor: pointer; transition: all 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            z-index: 20; display: flex; align-items: center; justify-content: center; overflow: hidden;
        }

        .rgb-chroma-btn::before {
            content: ''; position: absolute; width: 140%; height: 140%;
            background: conic-gradient(from 0deg, var(--accent-color), #ffff00, #00ff00, #00ffff, #0000ff, var(--accent-color), var(--accent-color));
            animation: chromaSpinFast 3s linear infinite; opacity: 0.85;
        }

        .rgb-chroma-btn::after {
            content: ''; position: absolute; width: 70%; height: 70%;
            background: #111; border-radius: 50%; border: 2px solid var(--accent-color); z-index: 2;
        }

        @keyframes chromaSpinFast { 100% { transform: rotate(360deg); } }
        .rgb-chroma-btn:hover { transform: translateX(-50%) scale(1.2); box-shadow: 0 0 25px var(--accent-glow); }

        /* Özel Skin Kartı */
        .custom-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(240px, 1fr)); gap: 20px; }
        .custom-card-frame {
            background: var(--bg-card); backdrop-filter: blur(14px);
            border: 1px solid var(--border-color); border-radius: var(--border-radius-main);
            overflow: hidden; display: flex; flex-direction: column; transition: 0.3s ease; position: relative;
            min-height: 220px; justify-content: space-between;
        }
        .custom-card-frame:hover { border-color: var(--accent-color); transform: translateY(-4px); box-shadow: 0 12px 30px var(--accent-glow); }
        
        .custom-card-banner {
            height: 140px; width: 100%; position: relative;
            background: linear-gradient(135deg, var(--bg-main) 0%, var(--border-color) 100%);
            display: flex; align-items: center; justify-content: center; border-bottom: 1px solid var(--border-color);
            background-size: cover; background-position: center 20%;
        }
        .custom-card-badge {
            position: absolute; top: 10px; left: 10px;
            background: rgba(0,0,0,0.75); backdrop-filter: blur(4px); border: 1px solid var(--accent-color);
            color: var(--accent-color); font-size: 10px; font-weight: 800; padding: 2px 8px; border-radius: 6px;
        }
        .price-badge {
            position: absolute; bottom: 10px; right: 10px;
            background: rgba(16, 185, 129, 0.85); color: #fff; font-size: 10px; font-weight: 800;
            padding: 3px 8px; border-radius: 6px; text-transform: uppercase;
        }
        .price-badge.paid { background: rgba(239, 68, 68, 0.85); }

        .custom-card-body { padding: 14px; display: flex; flex-direction: column; gap: 6px; }
        .custom-skin-title { font-size: 15px; font-weight: 800; color: var(--text-main); word-break: break-word; }
        .custom-skin-champ { font-size: 11px; font-weight: 700; color: var(--accent-color); text-transform: uppercase; }

        .three-dots-btn {
            position: absolute; top: 8px; right: 8px; z-index: 15;
            background: rgba(5, 7, 11, 0.85); border: 1px solid var(--border-color); color: #fff;
            width: 28px; height: 28px; border-radius: 8px; font-size: 14px; font-weight: bold;
            display: flex; align-items: center; justify-content: center; cursor: pointer; transition: all 0.2s ease;
        }
        .three-dots-btn:hover { border-color: var(--accent-color); color: var(--accent-color); }

        .card-menu-dropdown {
            display: none; position: absolute; top: 40px; right: 8px; z-index: 30;
            background: var(--bg-card); border: 1px solid var(--border-color);
            border-radius: 12px; width: 180px; padding: 6px; box-shadow: 0 10px 25px rgba(0,0,0,0.85);
        }
        .card-menu-dropdown.show { display: block; }
        .dropdown-item { padding: 8px 12px; border-radius: 8px; font-size: 12px; font-weight: 700; color: var(--text-main); cursor: pointer; transition: 0.2s; }
        .dropdown-item:hover { background: rgba(255,255,255,0.06); color: var(--accent-color); }
        .dropdown-item.danger:hover { background: rgba(239,68,68,0.15); color: #ef4444; }

        /* Başlat Butonu & Live Terminal Widget */
        #activeLauncherWidget {
            position: fixed; 
            top: var(--widget-top); bottom: var(--widget-bottom);
            left: var(--widget-left); right: var(--widget-right);
            transform: scale(var(--widget-scale)); transform-origin: bottom right;
            width: 380px; background: var(--bg-card); backdrop-filter: blur(18px);
            border: 1px solid var(--accent-color); border-radius: 16px; z-index: 3500;
            box-shadow: 0 15px 45px rgba(0,0,0,0.85); overflow: hidden; transition: all 0.3s cubic-bezier(0.16, 1, 0.3, 1);
        }
        #activeLauncherWidget.expanded { width: 460px; }
        
        .launcher-header {
            background: var(--accent-glow); padding: 12px 18px;
            display: flex; justify-content: space-between; align-items: center;
            border-bottom: 1px solid var(--border-color); font-weight: 800; font-size: 13px; color: var(--accent-color);
        }
        .launcher-body { padding: 12px; max-height: 180px; overflow-y: auto; display: flex; flex-direction: column; gap: 8px; }
        .active-skin-row { background: rgba(255,255,255,0.04); border: 1px solid var(--border-color); padding: 8px 12px; border-radius: 10px; display: flex; justify-content: space-between; align-items: center; gap: 10px; }
        .active-status-dot-pulse {
            display: inline-block; width: 12px; height: 12px; border-radius: 50%; background: #22c55e;
            box-shadow: 0 0 0 0 rgba(34,197,94,0.7);
            animation: statusPulse 1.5s infinite;
            flex-shrink: 0;
        }
        @keyframes statusPulse {
            0%   { box-shadow: 0 0 0 0 rgba(34,197,94,0.7); }
            70%  { box-shadow: 0 0 0 8px rgba(34,197,94,0); }
            100% { box-shadow: 0 0 0 0 rgba(34,197,94,0); }
        }

        /* DEVASA MODERN LAUNCH OVERLAY / MODAL */
        .launch-modal-container {
            width: 85vw; max-width: 980px; height: 75vh; max-height: 640px;
            background: var(--bg-card); border: 1.5px solid var(--accent-color);
            border-radius: 24px; box-shadow: 0 25px 60px rgba(0,0,0,0.95), 0 0 40px var(--accent-glow);
            display: flex; flex-direction: column; overflow: hidden; position: relative;
            animation: modalPop 0.4s cubic-bezier(0.16, 1, 0.3, 1);
            backdrop-filter: blur(25px);
        }
        .launch-modal-header {
            padding: 18px 28px; background: rgba(0,0,0,0.4); border-bottom: 1px solid var(--border-color);
            display: flex; justify-content: space-between; align-items: center;
        }
        .launch-modal-body {
            flex: 1; padding: 24px 28px; overflow-y: auto; display: flex; flex-direction: column;
            align-items: center; justify-content: center; gap: 20px;
        }
        .launch-cards-grid {
            display: flex; gap: 24px; flex-wrap: wrap; justify-content: center; align-items: center; width: 100%;
        }
        .launch-skin-card {
            width: 210px; height: 300px; border-radius: 18px; border: 2px solid var(--accent-color);
            position: relative; overflow: hidden; background: #000;
            box-shadow: 0 12px 30px var(--accent-glow);
            animation: launchCardGlow 2.5s infinite ease-in-out;
            transition: transform 0.3s ease;
        }
        @keyframes launchCardGlow {
            0%, 100% { box-shadow: 0 10px 25px var(--accent-glow); transform: translateY(0); }
            50% { box-shadow: 0 18px 40px var(--accent-color); transform: translateY(-5px); }
        }
        .launch-skin-card img {
            width: 100%; height: 100%; object-fit: cover; object-position: center top; filter: brightness(0.85);
        }
        .launch-skin-card-overlay {
            position: absolute; bottom: 0; left: 0; width: 100%; padding: 14px;
            background: linear-gradient(to top, rgba(5,7,11,0.98) 0%, rgba(5,7,11,0) 100%);
            display: flex; flex-direction: column; gap: 4px;
        }
        .launch-modal-footer {
            padding: 18px 28px; background: rgba(0,0,0,0.5); border-top: 1px solid var(--border-color);
            display: flex; align-items: center; justify-content: space-between; gap: 24px;
        }

        .btn-massive-start {
            width: 100%; padding: calc(14px * var(--start-btn-scale)); font-size: calc(13px * var(--start-btn-scale)); font-weight: 800; text-transform: uppercase;
            color: #020617; background: var(--start-btn-bg); border: none; border-radius: 10px; cursor: pointer;
            box-shadow: 0 4px 20px var(--accent-glow); transition: 0.25s ease; display: flex; justify-content: center; align-items: center; gap: 10px;
            background-size: cover; background-position: center; position: relative; overflow: hidden;
        }
        .btn-massive-start:hover { filter: brightness(1.15); transform: translateY(-1px); }
        .btn-massive-start.stop-mode {
            background: linear-gradient(135deg, #ef4444, #b91c1c) !important;
            color: #ffffff !important;
            box-shadow: 0 4px 20px rgba(239, 68, 68, 0.5) !important;
        }
        .btn-massive-start.stop-mode:hover { filter: brightness(1.1); }

        /* Formlar & Modern Butonlar */
        .modal { display: none; position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.85); z-index: 5000; justify-content: center; align-items: center; backdrop-filter: blur(6px); }
        .form-modal-content { background: var(--bg-card); backdrop-filter: blur(18px); width: 520px; max-width: 90vw; border-radius: 16px; border: 1px solid var(--border-color); display: flex; flex-direction: column; overflow: hidden; padding: 26px; box-shadow: 0 20px 50px rgba(0,0,0,0.85); max-height: 90vh; overflow-y: auto; }
        .form-group { margin-bottom: 16px; }
        .form-group label { display: block; font-size: 11px; font-weight: 800; color: var(--text-muted); margin-bottom: 6px; text-transform: uppercase; }

        .custom-file-upload {
            display: flex; align-items: center; justify-content: center; gap: 8px; padding: 10px 14px;
            background: var(--bg-main); border: 1px dashed var(--accent-color); border-radius: 8px;
            color: var(--accent-color); font-weight: 700; font-size: 12px; cursor: pointer; transition: 0.2s;
        }
        .custom-file-upload:hover { background: var(--accent-glow); }

        .settings-card { background: var(--bg-card); border: 1px solid var(--border-color); border-radius: var(--border-radius-main); padding: 22px 26px; backdrop-filter: blur(10px); margin-bottom: 16px; }
        .setting-row { display: flex; justify-content: space-between; align-items: center; padding: 12px 0; border-bottom: 1px solid rgba(255,255,255,0.04); flex-wrap: wrap; gap: 10px; }
        .setting-row:last-child { border-bottom: none; }
        .form-control { width: 100%; padding: 10px 14px; background: var(--bg-main); border: 1px solid var(--border-color); color: var(--text-main); border-radius: 8px; font-size: 13px; outline: none; }
        .form-control:focus { border-color: var(--accent-color); }

        select.form-control, select#langSelect {
            background-color: #0b1019 !important;
            color: #f1f5f9 !important;
            border: 1px solid var(--accent-color) !important;
            padding: 8px 14px !important;
            border-radius: 8px !important;
            font-size: 13px !important;
            font-weight: 700 !important;
            outline: none !important;
            cursor: pointer !important;
            appearance: auto !important;
            -webkit-appearance: auto !important;
        }
        select.form-control:focus, select#langSelect:focus {
            border-color: var(--accent-color) !important;
            box-shadow: 0 0 0 3px var(--accent-glow) !important;
        }
        select.form-control option, select#langSelect option {
            background-color: #0b1019 !important;
            color: #f1f5f9 !important;
            padding: 8px !important;
        }

        /* FRIENDS PANEL CSS */
        .friends-container {
            display: grid;
            grid-template-columns: 300px 1fr;
            gap: 20px;
            height: calc(100vh - 210px);
            min-height: 480px;
        }
        .friends-sidebar {
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: var(--border-radius-main);
            display: flex;
            flex-direction: column;
            overflow: hidden;
            backdrop-filter: blur(10px);
        }
        .friends-header {
            padding: 16px;
            border-bottom: 1px solid var(--border-color);
            display: flex;
            flex-direction: column;
            gap: 12px;
        }
        .friends-list {
            flex: 1;
            overflow-y: auto;
            display: flex;
            flex-direction: column;
        }
        .friend-item {
            padding: 12px 16px;
            display: flex;
            align-items: center;
            gap: 12px;
            border-bottom: 1px solid rgba(255,255,255,0.03);
            cursor: pointer;
            transition: background 0.2s ease;
        }
        .friend-item:hover, .friend-item.active {
            background: rgba(6, 182, 212, 0.1);
        }
        .friend-avatar-wrapper {
            position: relative;
        }
        .friend-avatar {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            object-fit: cover;
            border: 1.5px solid var(--border-color);
        }
        .friend-status-dot {
            position: absolute;
            bottom: 0;
            right: 0;
            width: 11px;
            height: 11px;
            border-radius: 50%;
            border: 2px solid #05070b;
        }
        .friend-status-dot.online { background: #10b981; box-shadow: 0 0 8px #10b981; }
        .friend-status-dot.offline { background: #64748b; }

        .chat-container {
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: var(--border-radius-main);
            display: flex;
            flex-direction: column;
            overflow: hidden;
            backdrop-filter: blur(10px);
        }
        .chat-header {
            padding: 16px 20px;
            border-bottom: 1px solid var(--border-color);
            display: flex;
            justify-content: space-between;
            align-items: center;
            background: rgba(0,0,0,0.2);
        }
        .chat-messages {
            flex: 1;
            padding: 20px;
            overflow-y: auto;
            display: flex;
            flex-direction: column;
            gap: 12px;
        }
        .message-bubble {
            max-width: 70%;
            padding: 10px 16px;
            border-radius: 14px;
            font-size: 13px;
            line-height: 1.4;
            word-wrap: break-word;
        }
        .message-bubble.incoming {
            background: rgba(255,255,255,0.06);
            color: var(--text-main);
            align-self: flex-start;
            border-bottom-left-radius: 2px;
        }
        .message-bubble.outgoing {
            background: var(--accent-color);
            color: #020617;
            font-weight: 600;
            align-self: flex-end;
            border-bottom-right-radius: 2px;
        }
        .chat-input-area {
            padding: 14px 20px;
            border-top: 1px solid var(--border-color);
            display: flex;
            gap: 10px;
            align-items: center;
            background: rgba(0,0,0,0.2);
        }

        /* Modern Toggle Switch */
        .toggle-switch {
            position: relative;
            display: inline-flex;
            align-items: center;
            width: 50px;
            height: 26px;
            flex-shrink: 0;
            cursor: pointer;
        }
        .toggle-switch input { opacity: 0; width: 0; height: 0; }
        .toggle-slider {
            position: absolute;
            top: 0; left: 0; right: 0; bottom: 0;
            background: rgba(255,255,255,0.1);
            border: 1px solid var(--border-color);
            border-radius: 26px;
            transition: 0.3s cubic-bezier(0.16, 1, 0.3, 1);
        }
        .toggle-slider:before {
            position: absolute;
            content: "";
            height: 18px; width: 18px;
            left: 3px; bottom: 3px;
            background: var(--text-muted);
            border-radius: 50%;
            transition: 0.3s cubic-bezier(0.16, 1, 0.3, 1);
            box-shadow: 0 2px 6px rgba(0,0,0,0.4);
        }
        .toggle-switch input:checked + .toggle-slider {
            background: var(--accent-color);
            border-color: var(--accent-color);
            box-shadow: 0 0 12px var(--accent-glow);
        }
        .toggle-switch input:checked + .toggle-slider:before {
            transform: translateX(24px);
            background: #020617;
        }

        .btn-primary {
            background: var(--accent-color); color: #020617; border: none; padding: 10px 20px; border-radius: 10px;
            font-size: 13px; font-weight: 800; transition: 0.2s; cursor: pointer; display: inline-flex; align-items: center; gap: 8px;
        }
        .btn-primary:hover { filter: brightness(1.15); transform: translateY(-2px); }

        /* Temalar Izgarası */
        .theme-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(120px, 1fr)); gap: 12px; margin-top: 10px; }
        .theme-card {
            border: 1px solid var(--border-color); border-radius: 8px; padding: 10px; text-align: center;
            cursor: pointer; transition: 0.2s; font-size: 11px; font-weight: 700; background: rgba(255,255,255,0.02);
        }
        .theme-card:hover, .theme-card.active { border-color: var(--accent-color); box-shadow: 0 0 10px var(--accent-glow); transform: translateY(-2px); }
        .theme-preview-box { height: 28px; border-radius: 6px; margin-bottom: 6px; }

        /* Filter Chips */
        .filter-chip-list { display: flex; gap: 8px; flex-wrap: wrap; margin-bottom: 16px; }
        .filter-chip { padding: 6px 14px; border-radius: 20px; background: rgba(255,255,255,0.04); border: 1px solid var(--border-color); color: var(--text-muted); font-size: 12px; font-weight: 700; cursor: pointer; transition: 0.2s; }
        .filter-chip.active, .filter-chip:hover { background: var(--accent-color); color: #020617; border-color: var(--accent-color); }
        
        /* Drag Overlay */
        #dragDropOverlay {
            display: none; position: fixed; top: 0; left: 0; width: 100vw; height: 100vh;
            background: rgba(6, 182, 212, 0.25); backdrop-filter: blur(8px); z-index: 10000;
            border: 4px dashed var(--accent-color); align-items: center; justify-content: center;
            flex-direction: column; color: #fff; font-size: 20px; font-weight: 800; text-shadow: 0 0 20px var(--accent-glow);
            pointer-events: none;
        }

        /* YENİ NESİL CHROMA MODALI (Tam Ekran ve Devasa Splash Art Destekli) */
        .chroma-fullscreen-container {
            width: 90vw; height: 90vh; max-width: 1400px;
            background: rgba(5, 7, 11, 0.95);
            border: 1px solid var(--accent-color); border-radius: 24px;
            overflow: hidden; display: flex; flex-direction: column; position: relative;
            box-shadow: 0 25px 60px rgba(0,0,0,0.9);
            animation: modalPop 0.4s cubic-bezier(0.16, 1, 0.3, 1);
        }

        @keyframes modalPop {
            from { opacity: 0; transform: scale(0.95) translateY(20px); }
            to { opacity: 1; transform: scale(1) translateY(0); }
        }

        .chroma-close-btn {
            position: absolute; top: 20px; right: 20px;
            background: rgba(0,0,0,0.6); border: 1px solid var(--accent-color);
            color: #fff; padding: 8px 16px; border-radius: 12px;
            font-size: 14px; font-weight: 800; cursor: pointer; z-index: 100;
            transition: all 0.2s; backdrop-filter: blur(5px);
        }
        .chroma-close-btn:hover { background: var(--accent-color); color: #000; transform: scale(1.05); }

        .chroma-hero-section {
            width: 100%; flex: 1; position: relative;
            display: flex; align-items: center; justify-content: center; overflow: hidden;
        }

        #chromaHeroBg {
            position: absolute; top: 0; left: 0; width: 100%; height: 100%;
            object-fit: cover; filter: blur(25px) brightness(0.25); z-index: 1;
        }

        .chroma-hero-overlay {
            position: absolute; bottom: 0; left: 0; width: 100%; height: 50%;
            background: linear-gradient(to top, rgba(5,7,11,1) 0%, rgba(5,7,11,0) 100%); z-index: 2;
        }

        #chromaHeroImg {
            position: relative; z-index: 3;
            max-width: 95%; max-height: 90%; object-fit: contain;
            filter: drop-shadow(0 25px 40px rgba(0,0,0,0.9)); transition: all 0.3s ease;
        }

        .chroma-hero-title {
            position: absolute; bottom: 30px; left: 40px; z-index: 4;
            font-size: 38px; font-weight: 900; color: var(--text-main); text-transform: uppercase;
            letter-spacing: 2px; text-shadow: 0 5px 20px rgba(0,0,0,0.9), 0 0 15px var(--accent-glow);
        }

        .chroma-thumbnails-wrapper {
            width: 100%; height: 260px;
            background: rgba(0,0,0,0.5); border-top: 1px solid var(--accent-color);
            padding: 20px 40px; display: flex; flex-direction: column; z-index: 5;
        }

        .chroma-thumbnails-grid {
            display: flex; gap: 20px; overflow-x: auto; padding-bottom: 10px; height: 100%; align-items: center;
        }

        .chroma-thumbnails-grid::-webkit-scrollbar { height: 8px; }
        .chroma-thumbnails-grid::-webkit-scrollbar-track { background: rgba(255,255,255,0.05); border-radius: 4px; }
        .chroma-thumbnails-grid::-webkit-scrollbar-thumb { background: var(--accent-color); border-radius: 4px; }

        .chroma-thumb-card {
            min-width: 160px; width: 160px; height: 160px;
            border-radius: 14px; border: 2px solid var(--border-color); overflow: hidden;
            position: relative; cursor: pointer; background: #111;
            transition: all 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }

        .chroma-thumb-card img { width: 100%; height: 100%; object-fit: cover; transition: all 0.3s ease; }
        .chroma-thumb-card:hover { transform: translateY(-8px) scale(1.04); border-color: var(--accent-color); box-shadow: 0 10px 30px var(--accent-glow); }
        .chroma-thumb-card:hover img { filter: brightness(1.2); }

        .chroma-thumb-name {
            position: absolute; bottom: 0; left: 0; width: 100%;
            background: rgba(0,0,0,0.85); color: var(--text-main); font-size: 11px; font-weight: 800;
            text-align: center; padding: 6px 4px; backdrop-filter: blur(4px);
        }
        
        .chroma-add-badge {
            position: absolute; top: 50%; left: 50%;
            transform: translate(-50%, -50%) scale(0);
            background: var(--accent-color); color: #000;
            width: 42px; height: 42px; border-radius: 50%;
            font-size: 24px; font-weight: 900; display: flex; align-items: center; justify-content: center;
            opacity: 0; transition: transform 0.2s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            box-shadow: 0 0 15px rgba(0,0,0,0.5);
        }

        .chroma-thumb-card:hover .chroma-add-badge {
            transform: translate(-50%, -50%) scale(1); opacity: 1;
        }
    </style>
</head>
<body>

    <div id="toastContainer"></div>
    <div id="dragDropOverlay">
        <img src="https://i.hizliresim.com/7d9qpuq.png" class="wings-logo-hero-fixed" alt="Wings Logo">
        <span id="txt-drag-drop-label">Sadece .ZIP veya .FANTOME Dosyası Bırakın</span>
    </div>

    <!-- Gizli Dosya Seçici -->
    <input type="file" id="directSkinFileInput" accept=".zip,.fantome" style="display:none;" onchange="handleDirectSkinFileUpload(event)">

    <div id="appBackground">
        <img id="mainAppBackground" src="https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Yasuo_1.jpg" alt="Background">
    </div>

    <!-- LOGIN / DISCORD AUTH SCREEN -->
    <div id="loginScreen" style="position:fixed; top:0; left:0; width:100vw; height:100vh; background:#020305; z-index:99999; display:flex; flex-direction:column; align-items:center; justify-content:center;">
        <div id="appBackground2" style="position:absolute; top:0; left:0; width:100%; height:100%; z-index:-1; overflow:hidden;">
            <img src="https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Akali_32.jpg" style="width:100%; height:100%; object-fit:cover; filter:brightness(0.12) blur(6px);" alt="Bg">
        </div>

        <!-- Logo & Title -->
        <div style="text-align:center; margin-bottom:36px; animation: fadeInDown 0.7s ease;">
            <img src="https://i.hizliresim.com/7d9qpuq.png" style="width:80px; height:80px; filter:drop-shadow(0 0 30px #5865F2); animation:wingPulse 3s infinite ease-in-out;" alt="Logo">
            <div style="font-size:38px; font-weight:900; color:#fff; letter-spacing:4px; margin-top:14px; text-shadow: 0 0 40px rgba(88,101,242,0.6);">SKYNIX</div>
            <div style="font-size:11px; font-weight:800; color:#5865F2; letter-spacing:6px; margin-top:4px;">MANAGER NEXTGEN</div>
        </div>

        <!-- Login Card -->
        <div id="loginBox" style="background:rgba(8,10,18,0.96); border:1px solid rgba(88,101,242,0.3); border-radius:24px; padding:36px 40px; width:420px; max-width:92vw; backdrop-filter:blur(24px); box-shadow:0 40px 100px rgba(0,0,0,0.95), 0 0 60px rgba(88,101,242,0.08);">

            <div style="text-align:center; margin-bottom:28px;">
                <div style="font-size:18px; font-weight:800; color:#fff; margin-bottom:8px;">Discord ile Giriş Yap</div>
                <div style="font-size:12px; color:#64748b; line-height:1.6;">
                    Skynix'e erişmek için Discord sunucumuza katılman ve<br>
                    <strong style="color:#5865F2;">Üye</strong> rolünü alman gerekiyor.
                </div>
            </div>

            <!-- Discord Steps -->
            <div style="display:flex; flex-direction:column; gap:12px; margin-bottom:28px;">
                <div style="display:flex; align-items:center; gap:12px; background:rgba(88,101,242,0.08); border:1px solid rgba(88,101,242,0.15); border-radius:12px; padding:12px 16px;">
                    <span style="font-size:20px; min-width:28px; text-align:center;">1️⃣</span>
                    <div>
                        <div style="font-size:13px; font-weight:700; color:#e2e8f0;">Sunucumuza katıl</div>
                        <a href="https://discord.gg/2cTNwPWTeE" style="font-size:11px; color:#5865F2; text-decoration:none;" target="_blank">discord.gg/2cTNwPWTeE →</a>
                    </div>
                </div>
                <div style="display:flex; align-items:center; gap:12px; background:rgba(88,101,242,0.08); border:1px solid rgba(88,101,242,0.15); border-radius:12px; padding:12px 16px;">
                    <span style="font-size:20px; min-width:28px; text-align:center;">2️⃣</span>
                    <div>
                        <div style="font-size:13px; font-weight:700; color:#e2e8f0;">Üye rolünü al</div>
                        <div style="font-size:11px; color:#64748b;">Sunucu kurallarını kabul et ve rolünü al</div>
                    </div>
                </div>
                <div style="display:flex; align-items:center; gap:12px; background:rgba(88,101,242,0.08); border:1px solid rgba(88,101,242,0.15); border-radius:12px; padding:12px 16px;">
                    <span style="font-size:20px; min-width:28px; text-align:center;">3️⃣</span>
                    <div>
                        <div style="font-size:13px; font-weight:700; color:#e2e8f0;">Discord ile giriş yap</div>
                        <div style="font-size:11px; color:#64748b;">Hesabını bağla, uygulamaya eriş</div>
                    </div>
                </div>
            </div>

            <!-- Discord Login Button -->
            <button id="discordLoginBtn" onclick="startDiscordLogin()" style="width:100%; padding:16px; background:#5865F2; color:#fff; border:none; border-radius:14px; font-size:16px; font-weight:900; cursor:pointer; transition:all 0.25s; letter-spacing:0.5px; display:flex; align-items:center; justify-content:center; gap:12px;" onmouseover="this.style.background='#4752c4'; this.style.transform='translateY(-2px)'; this.style.boxShadow='0 8px 30px rgba(88,101,242,0.5)'" onmouseout="this.style.background='#5865F2'; this.style.transform='translateY(0)'; this.style.boxShadow='none'">
                <svg width="24" height="24" viewBox="0 0 127.14 96.36" fill="white"><path d="M107.7,8.07A105.15,105.15,0,0,0,81.47,0a72.06,72.06,0,0,0-3.36,6.83A97.68,97.68,0,0,0,49,6.83,72.37,72.37,0,0,0,45.64,0,105.89,105.89,0,0,0,19.39,8.09C2.79,32.65-1.71,56.6.54,80.21A105.73,105.73,0,0,0,32.71,96.36,77.7,77.7,0,0,0,39.6,85.25a68.42,68.42,0,0,1-10.85-5.18c.91-.66,1.8-1.34,2.66-2a75.57,75.57,0,0,0,64.32,0c.87.71,1.76,1.39,2.66,2a68.68,68.68,0,0,1-10.87,5.19,77,77,0,0,0,6.89,11.1,105.25,105.25,0,0,0,32.19-16.14c2.64-27.38-4.51-51.11-18.91-72.15ZM42.45,65.69C36.18,65.69,31,60,31,53s5-12.74,11.43-12.74S54,45.91,53.87,53,48.8,65.69,42.45,65.69Zm42.24,0C78.41,65.69,73.25,60,73.25,53s5-12.74,11.44-12.74S96.23,45.91,96.1,53,91,65.69,84.69,65.69Z"/></svg>
                Discord ile Giriş Yap
            </button>

            <!-- Status message -->
            <div id="discordLoginStatus" style="margin-top:14px; font-size:12px; font-weight:700; text-align:center; color:#64748b; min-height:18px;"></div>
        </div>

        <div style="margin-top:20px; font-size:11px; color:#334155; text-align:center; animation: fadeIn 1.2s ease;">Skynix Manager v2.0 • By Herobrine • discord.gg/2cTNwPWTeE</div>
    </div>

    <!-- Yükleme Ekranı -->
    <div id="loadingScreen">
        <div class="loading-title-container">
            <img src="https://i.hizliresim.com/7d9qpuq.png" class="wings-logo-hero-fixed" alt="Wings Logo">
            <div class="loading-app-title">SKYNIX</div>
            <div class="loading-app-sub">SKYNIX MANAGER NEXTGEN</div>
        </div>
        <div class="loading-content">
            <div class="loading-subtitle" id="loadSubtitle">Veriler hazırlanıyor...</div>
            <div class="progress-bar-container">
                <div class="progress-bar" id="progressBar"></div>
            </div>
        </div>
    </div>

    <!-- Üst Başlık Çubuğu -->
    <div class="titlebar">
        <div class="title">
            <img src="https://i.hizliresim.com/7d9qpuq.png" class="wings-logo-fixed" alt="Wings Logo">
            <span>SKYNIX MANAGER</span>
        </div>
        <div class="titlebar-right">
            <div class="client-status-badge" title="LeagueClient Connection Active">
                <span class="client-status-dot"></span>
                <span id="txt-client-status">LOL BAĞLI</span>
            </div>

            <div class="profile-trigger" onclick="switchTab('profile', document.getElementById('nav-profile-item'))">
                <img id="navProfileAvatar" src="https://i.postimg.cc/y89X380H/shizuku-anime.png" class="profile-avatar-sm" alt="Avatar" onerror="this.src='https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Ahri_0.jpg';">
                <span class="profile-name-sm" id="navProfileName">Oyuncu</span>
            </div>

            <div class="window-controls">
                <button onclick="handleWindowAction('minimize')" title="Küçült">🗕</button>
                <button onclick="handleWindowAction('maximize')" title="Büyüt">🗖</button>
                <button class="close" onclick="handleWindowAction('close')" title="Kapat">✕</button>
            </div>
        </div>
    </div>

    <!-- Başlatma Widget'ı -->
    <div id="activeLauncherWidget">
        <div class="launcher-header">
            <span id="txt-queue-title">Seçili Modlar (Sıradaki)</span>
            <button onclick="toggleLauncherMinimize()" style="background:none; border:none; color:var(--accent-color); font-weight:bold; font-size:16px; cursor:pointer;">_</button>
        </div>
        <div class="launcher-body" id="activeLauncherList">
            <div style="font-size:12px; color:var(--text-muted); text-align:center; padding:10px;" id="txt-queue-empty">Çalıştırılacak mod bulunmuyor.</div>
        </div>

        <div style="padding:12px; border-top:1px solid rgba(255,255,255,0.06);" class="launcher-footer">
            <button id="masterStartBtn" class="btn-massive-start" onclick="injectActiveMods()">
                <svg class="icon-svg" viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg>
                <span id="txt-start-btn">SKİNLERİ BAŞLAT</span>
            </button>
        </div>
    </div>

    <!-- Ana Kontrol Paneli Düzeni -->
    <div class="main-container">
        <div class="sidebar" id="appSidebar">
            <div class="nav-item active" onclick="switchTab('home', this)">
                <svg class="icon-svg" viewBox="0 0 24 24"><path d="M10 20v-6h4v6h5v-8h3L12 3 2 12h3v8z"/></svg>
                <span id="txt-nav-home">Ana Ekran</span>
            </div>
            <div class="nav-item" id="nav-profile-item" onclick="switchTab('profile', this)">
                <svg class="icon-svg" viewBox="0 0 24 24"><path d="M12 12c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm0 2c-2.67 0-8 1.34-8 4v2h16v-2c0-2.66-5.33-4-8-4z"/></svg>
                <span id="txt-nav-profile">Profilim</span>
            </div>
            <div class="nav-item" onclick="switchTab('champions', this)">
                <svg class="icon-svg" viewBox="0 0 24 24"><path d="M12 2L1 21h22L12 2zm0 3.8L19.3 19H4.7L12 5.8z"/></svg>
                <span id="txt-nav-champions">Şampiyonlar</span>
            </div>
            <div class="nav-item" onclick="switchTab('customSkins', this)">
                <svg class="icon-svg" viewBox="0 0 24 24"><path d="M20 6h-8l-2-2H4c-1.1 0-1.99.9-1.99 2L2 18c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V8c0-1.1-.9-2-2-2z"/></svg>
                <span id="txt-nav-custom">Özel Skinlerim</span>
            </div>
            <div class="nav-item" onclick="switchTab('store', this)">
                <svg class="icon-svg" viewBox="0 0 24 24"><path d="M7 18c-1.1 0-1.99.9-1.99 2S5.9 22 7 22s2-.9 2-2-.9-2-2-2zM1 2v2h2l3.6 7.59-1.35 2.45c-.16.28-.25.61-.25.96 0 1.1.9 2 2 2h12v-2H7.42c-.14 0-.25-.11-.25-.25l.03-.12.9-1.63h7.45c.75 0 1.41-.41 1.75-1.03l3.58-6.49c.08-.14.12-.31.12-.48 0-.55-.45-1-1-1H5.21l-.94-2H1zm16 16c-1.1 0-1.99 2s.89 2 1.99 2 2-.9 2-2-.9-2-2-2z"/></svg>
                <span id="txt-nav-store">Mağaza</span>
            </div>
            <div class="nav-item" onclick="switchTab('themes', this)">
                <svg class="icon-svg" viewBox="0 0 24 24"><path d="M12 3c-4.97 0-9 4.03-9 9 0 2.12.74 4.07 1.97 5.61.43.53.28 1.32-.34 1.66-.46.26-1.04.14-1.36-.28A10.93 10.93 0 0 1 1 12C1 5.93 5.93 1 12 1s11 4.93 11 11c0 2.76-1.02 5.28-2.72 7.21-.33.37-.9.44-1.31.14-.42-.3-.52-.89-.22-1.32A8.96 8.96 0 0 0 21 12c0-4.97-4.03-9-9-9z"/></svg>
                <span id="txt-nav-themes">Temalar & Tasarım</span>
            </div>
            <div class="nav-item" onclick="switchTab('settings', this)">
                <svg class="icon-svg" viewBox="0 0 24 24"><path d="M19.14 12.94c.04-.3.06-.61.06-.94 0-.32-.02-.64-.07-.94l2.03-1.58c.18-.14.23-.41.12-.61l-1.92-3.32c-.12-.22-.37-.29-.59-.22l-2.39.96c-.5-.38-1.03-.7-1.62-.94l-.36-2.54c-.04-.24-.24-.41-.48-.41h-3.84c-.24 0-.43.17-.47.41l-.36 2.54c-.59.24-1.13.57-1.62.94l-2.39-.96c-.22-.08-.47 0-.59.22L2.74 8.87c-.12.21-.08.47.12.61l2.03 1.58c-.05.3-.09.63-.09.94s.02.64.07.94l-2.03 1.58c-.18.14-.23.41-.12.61l1.92 3.32c.12.22.37.29.59.22l2.39-.96c.5.38 1.03.7 1.62.94l.36 2.54c.05.24.24.41.48.41h3.84c.24 0 .44-.17.47-.41l.36-2.54c.59-.24 1.13-.56 1.62-.94l2.39.96c.22.08.47 0 .59-.22l1.92-3.32c.12-.22.07-.47-.12-.61l-2.01-1.58zM12 15.6c-1.98 0-3.6-1.62-3.6-3.6s1.62-3.6 3.6-3.6 3.6 1.62 3.6 3.6-1.62 3.6-3.6-3.6z"/></svg>
                <span id="txt-nav-settings">Ayarlar</span>
            </div>
        </div>

        <div class="content-area">
            
            <!-- ANA EKRAN PANELİ -->
            <div id="home-panel" class="panel active">
                <!-- HERO BAŞLIK -->
                <div class="home-hero">
                    <img src="https://i.hizliresim.com/7d9qpuq.png" class="wings-logo-hero-fixed" alt="Wings Logo">
                    <h1 class="home-title">SKYNIX MANAGER</h1>
                    <div class="hero-avatar-wrapper">
                        <img id="heroAuthorImg" src="https://i.hizliresim.com/5oi1b6z.jpg" class="hero-author-avatar" alt="Character" onerror="this.src='https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Ahri_0.jpg';">
                    </div>
                    <div class="author-badge">By Herobrine</div>
                    <p class="home-subtitle" id="txt-home-sub">Skynix ile Favori Kostümlerini Yönet ve Sihirdar Vadisi'ne Hükmet</p>
                    <a href="https://discord.gg/2cTNwPWTeE" target="_blank" class="discord-btn">
                        <svg width="20" height="20" viewBox="0 0 127.14 96.36" fill="currentColor"><path d="M107.7,8.07A105.15,105.15,0,0,0,81.47,0a72.06,72.06,0,0,0, -3.36,6.83A97.68,97.68,0,0,0,49,6.83,72.37,72.37,0,0,0,45.64,0,105.89,105.89,0,0,0,19.39,8.09C2.79,32.65-1.71,56.6.54,80.21A105.73,105.73,0,0,0,32.71,96.36,77.7,77.7,0,0,0,39.6,85.25a68.42,68.42,0,0,1-10.85-5.18c.91-.66,1.8-1.34,2.66-2a75.57,75.57,0,0,0,64.32,0c.87.71,1.76,1.39,2.66,2a68.68,68.68,0,0,1-10.87,5.19,77,77,0,0,0,6.89,11.1,105.25,105.25,0,0,0,32.19-16.14c2.64-27.38-4.51-51.11-18.91-72.15ZM42.45,65.69C36.18,65.69,31,60,31,53s5-12.74,11.43-12.74S54,45.91,53.87,53,48.8,65.69,42.45,65.69Zm42.24,0C78.41,65.69,73.25,60,73.25,53s5-12.74,11.44-12.74S96.23,45.91,96.1,53,91,65.69,84.69,65.69Z"/></svg>
                        <span id="txt-discord-btn">Discord Sunucumuza Katıl</span>
                    </a>
                </div>

                <!-- HIZLI İSTATİSTİKLER -->
                <div class="home-quick-stats">
                    <div class="quick-stat-box">
                        <div class="quick-stat-icon"><svg class="icon-svg icon-lg" viewBox="0 0 24 24"><path d="M12 2L2 7l10 5 10-5-10-5zm0 9l10-5v11l-10 5-10-5V6l10 5z"/></svg></div>
                        <div>
                            <div class="quick-stat-val" id="homeTotalSkinsVal">0</div>
                            <div class="quick-stat-lbl" id="txt-stat-customs">Yüklü Özel Skin</div>
                        </div>
                    </div>
                    <div class="quick-stat-box">
                        <div class="quick-stat-icon"><svg class="icon-svg icon-lg" viewBox="0 0 24 24"><path d="M13 2L3 14h9l-1 8 10-12h-9l1-8z"/></svg></div>
                        <div>
                            <div class="quick-stat-val" id="homeActiveQueueVal">0</div>
                            <div class="quick-stat-lbl" id="txt-stat-activeq">Sıradaki Modlar</div>
                        </div>
                    </div>
                    <div class="quick-stat-box">
                        <div class="quick-stat-icon"><svg class="icon-svg icon-lg" viewBox="0 0 24 24"><path d="M11.99 2C6.47 2 2 6.48 2 12s4.47 10 9.99 10C17.52 22 22 17.52 22 12S17.52 2 11.99 2zm4.24 16L12 15.45 7.77 18l1.12-4.81-3.73-3.23 4.92-.42L12 5l2.02 4.54 4.92.42-3.73 3.23L16.23 18z"/></svg></div>
                        <div>
                            <div class="quick-stat-val" id="homeTimeVal">0 dk</div>
                            <div class="quick-stat-lbl" id="txt-stat-timer">Toplam Süre</div>
                        </div>
                    </div>
                </div>

                <!-- ÖZELLİK + SPLASH ART KARTI BÖLÜMÜ -->
                <h2 style="font-size:18px; font-weight:800; color:var(--text-main); margin:24px 0 14px 0; display:flex; align-items:center; gap:8px;">
                    <span style="color:var(--accent-color);">⚡</span>
                    <span id="txt-home-features-header">Uygulama Özellikleri</span>
                </h2>

                <div class="home-features-grid">
                    <!-- Özellik 1: Özel Skin Sistemi -->
                    <div class="home-feature-card" onclick="switchTab('customSkins', document.querySelector('[onclick*=customSkins]'))">
                        <div class="home-feature-splash">
                            <img src="https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Akali_32.jpg" alt="Prestige Star Guardian Akali" loading="lazy">
                            <div class="home-feature-splash-overlay"></div>
                        </div>
                        <div class="home-feature-content">
                            <div class="home-feature-icon">🎨</div>
                            <h3 class="home-feature-title" id="txt-feat-custom-title">Özel Skin Yöneticisi</h3>
                            <p class="home-feature-desc" id="txt-feat-custom-desc">Kendi .fantome ve .zip skin dosyalarını yükle, yönet ve tek tıkla etkinleştir.</p>
                            <span class="home-feature-tag">Özel Skinlerim →</span>
                        </div>
                    </div>

                    <!-- Özellik 2: Şampiyon Kütüphanesi -->
                    <div class="home-feature-card" onclick="switchTab('champions', document.querySelector('[onclick*=champions]'))">
                        <div class="home-feature-splash">
                            <img src="https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Ahri_86.jpg" alt="Prestige Coven Ahri" loading="lazy">
                            <div class="home-feature-splash-overlay"></div>
                        </div>
                        <div class="home-feature-content">
                            <div class="home-feature-icon">🏆</div>
                            <h3 class="home-feature-title" id="txt-feat-champ-title">Şampiyon Kütüphanesi</h3>
                            <p class="home-feature-desc" id="txt-feat-champ-desc">165+ şampiyon ve tüm skin splash artlarına göz at, favori kostümünü kuyruğa ekle.</p>
                            <span class="home-feature-tag">Şampiyonlara Git →</span>
                        </div>
                    </div>

                    <!-- Özellik 3: Tema & Tasarım -->
                    <div class="home-feature-card" onclick="switchTab('themes', document.querySelector('[onclick*=themes]'))">
                        <div class="home-feature-splash">
                            <img src="https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Zed_30.jpg" alt="Spirit Blossom Zed" loading="lazy">
                            <div class="home-feature-splash-overlay"></div>
                        </div>
                        <div class="home-feature-content">
                            <div class="home-feature-icon">🌈</div>
                            <h3 class="home-feature-title" id="txt-feat-theme-title">Tema & Tasarım</h3>
                            <p class="home-feature-desc" id="txt-feat-theme-desc">20+ hazır tema paketi ve tam özelleştirilebilir renk sistemiyle arayüzü kişiselleştir.</p>
                            <span class="home-feature-tag">Temaları Keşfet →</span>
                        </div>
                    </div>

                    <!-- Özellik 4: Topluluk Mağazası -->
                    <div class="home-feature-card" onclick="switchTab('store', document.querySelector('[onclick*=store]'))">
                        <div class="home-feature-splash">
                            <img src="https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Janna_27.jpg" alt="Prestige Cyber Halo Janna" loading="lazy">
                            <div class="home-feature-splash-overlay"></div>
                        </div>
                        <div class="home-feature-content">
                            <div class="home-feature-icon">🏪</div>
                            <h3 class="home-feature-title" id="txt-feat-store-title">Topluluk Mağazası</h3>
                            <p class="home-feature-desc" id="txt-feat-store-desc">Topluluk tarafından yapılan özel mod paketlerini keşfet ve bir tıkla yükle.</p>
                            <span class="home-feature-tag">Mağazaya Git →</span>
                        </div>
                    </div>
                    
                    <!-- Özellik 5: Akıllı Dosya Eşleştirme -->
                    <div class="home-feature-card" onclick="switchTab('customSkins', document.querySelector('[onclick*=customSkins]'))">
                        <div class="home-feature-splash">
                            <img src="https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Akali_15.jpg" alt="Prestige K/DA Akali" loading="lazy">
                            <div class="home-feature-splash-overlay"></div>
                        </div>
                        <div class="home-feature-content">
                            <div class="home-feature-icon">⚡</div>
                            <h3 class="home-feature-title" id="txt-feat-smart-title">Akıllı Dosya Eşleştirme</h3>
                            <p class="home-feature-desc" id="txt-feat-smart-desc">Yüklediğin skin dosyasından otomatik şampiyon tespiti ve splash art çekme sistemi.</p>
                            <span class="home-feature-tag">Skin Ekle →</span>
                        </div>
                    </div>
                </div>

                <style>
                    .home-features-grid {
                        display: grid;
                        grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
                        gap: 16px;
                        margin-bottom: 24px;
                    }
                    .home-feature-card {
                        position: relative;
                        border-radius: 16px;
                        overflow: hidden;
                        cursor: pointer;
                        border: 2px solid var(--border-color);
                        background: var(--bg-card);
                        transition: transform 0.3s cubic-bezier(0.16, 1, 0.3, 1), box-shadow 0.3s cubic-bezier(0.16, 1, 0.3, 1), border-color 0.3s ease;
                        display: flex;
                        flex-direction: column;
                        box-shadow: 0 8px 24px rgba(0,0,0,0.5);
                    }
                    .home-feature-card:hover {
                        transform: translateY(-6px);
                        box-shadow: 0 16px 40px var(--accent-glow);
                        border-color: var(--accent-color);
                    }
                    .home-feature-splash {
                        position: relative;
                        height: 160px;
                        overflow: hidden;
                    }
                    .home-feature-splash img {
                        width: 100%;
                        height: 100%;
                        object-fit: cover;
                        object-position: center top;
                        transition: transform 0.5s ease;
                    }
                    .home-feature-card:hover .home-feature-splash img {
                        transform: scale(1.08);
                    }
                    .home-feature-splash-overlay {
                        position: absolute;
                        inset: 0;
                        background: linear-gradient(to bottom, rgba(0,0,0,0.1) 0%, rgba(2,6,23,0.85) 100%);
                    }
                    .home-feature-content {
                        padding: 16px;
                        display: flex;
                        flex-direction: column;
                        gap: 6px;
                        flex: 1;
                    }
                    .home-feature-icon {
                        font-size: 22px;
                        margin-top: -4px;
                    }
                    .home-feature-title {
                        font-size: 15px;
                        font-weight: 800;
                        color: var(--text-main);
                        margin: 0;
                    }
                    .home-feature-desc {
                        font-size: 12px;
                        color: var(--text-muted);
                        line-height: 1.5;
                        margin: 0;
                    }
                    .home-feature-tag {
                        font-size: 11px;
                        font-weight: 800;
                        color: var(--accent-color);
                        margin-top: auto;
                        padding-top: 8px;
                        letter-spacing: 0.04em;
                    }
                </style>
            </div>


            <!-- PROFİL PANELİ & SPOTIFY -->
            <div id="profile-panel" class="panel">
                <div class="profile-page-card">
                    <div class="profile-page-banner" id="mainProfilePageBanner" style="background-image: url('https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Zed_1.jpg');">
                        <img id="mainProfilePageAvatar" src="https://i.postimg.cc/y89X380H/shizuku-anime.png" class="profile-page-avatar" alt="Avatar" onerror="this.src='https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Ahri_0.jpg';">
                    </div>
                    <div class="profile-page-body">
                        <div style="display:flex; justify-content:space-between; align-items:flex-start;">
                            <div>
                                <h2 style="font-size:24px; font-weight:800; color:var(--text-main);" id="profilePageName">Oyuncu</h2>
                                <p style="font-size:13px; color:var(--accent-color); font-weight:700; margin-top:2px;" id="txt-profile-sub">Skynix Koleksiyoneri & Tasarımcı</p>
                            </div>
                            <button class="btn-primary" onclick="openProfileEditModal()" id="txt-edit-profile-btn">Profili Düzenle</button>
                        </div>

                        <div class="profile-stats-grid">
                            <div class="profile-stat-card">
                                <div class="profile-stat-icon">
                                    <svg class="icon-svg icon-lg" viewBox="0 0 24 24"><path d="M11.99 2C6.47 2 2 6.48 2 12s4.47 10 9.99 10C17.52 22 22 17.52 22 12S17.52 2 11.99 2zm4.24 16L12 15.45 7.77 18l1.12-4.81-3.73-3.23 4.92-.42L12 5l2.02 4.54 4.92.42-3.73 3.23L16.23 18z"/></svg>
                                </div>
                                <div>
                                    <div class="profile-stat-val" id="timeSpentMinutesDisplay">0 dk</div>
                                    <div class="profile-stat-lbl" id="txt-stat-time">Uygulamada Geçirilen Süre</div>
                                </div>
                            </div>

                            <div class="profile-stat-card">
                                <div class="profile-stat-icon">
                                    <svg class="icon-svg icon-lg" viewBox="0 0 24 24"><path d="M12 2L2 7l10 5 10-5-10-5zm0 9l10-5v11l-10 5-10-5V6l10 5z"/></svg>
                                </div>
                                <div>
                                    <div class="profile-stat-val" id="totalCustomSkinsCount">0</div>
                                    <div class="profile-stat-lbl" id="txt-stat-skins">Özel Kostüm Sayısı</div>
                                </div>
                            </div>

                            <div class="profile-stat-card">
                                <div class="profile-stat-icon">
                                    <svg class="icon-svg icon-lg" viewBox="0 0 24 24"><path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zm-5 14H7v-2h7v2zm3-4H7v-2h10v2zm0-4H7V7h10v2z"/></svg>
                                </div>
                                <div>
                                    <div class="profile-stat-val" id="topUsedSkinDisplay">-</div>
                                    <div class="profile-stat-lbl" id="txt-stat-topskin">En Çok Çalıştırılan Skin</div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="spotify-container">
                    <div class="spotify-header">
                        <svg class="icon-svg icon-lg" viewBox="0 0 24 24"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm5.52 14.5c-.2.3-.58.4-.88.2-2.42-1.48-5.46-1.82-9.05-1-1-.34-.23-.67.12-.88.35.38 4.14 2.18 8.01 1.02.3-.18.68-.08.88.22zm1.48-3.26c-.26.43-.82.56-1.25.3-3.05-1.87-7.7-2.42-11.31-1.32-.48.14-.99-.13-1.13-.61-.14-.48.13-.99.61-1.13 4.13-1.25 9.27-.64 12.78 1.51.43.26.56.82.3 1.25zm.13-3.41c-3.66-2.17-9.7-2.37-13.2-1.31-.56.17-1.16-.15-1.33-.71-.17-.56.15-1.16.71-1.33 4.03-1.22 10.71-.99 14.91 1.5.5.3.66.95.36 1.45-.3.5-.95.66-1.45.36z"/></svg>
                        <span id="txt-spotify-title">Spotify Favori Playlist</span>
                    </div>
                    <iframe id="spotifyIframe" style="border-radius:12px;" src="https://open.spotify.com/embed/playlist/37i9dQZF1DXcBWIGoYBM5M?utm_source=generator&theme=0" width="100%" height="152" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
                    <div style="margin-top:10px; display:flex; gap:10px;">
                        <input type="text" id="spotifyEmbedInput" class="form-control" placeholder="Spotify Playlist URL veya Embed Linki girin...">
                        <button class="btn-primary" onclick="updateSpotifyEmbed()"><span id="txt-spotify-save">Güncelle & Sabitle</span></button>
                    </div>
                </div>
            </div>

            <!-- ARKADAŞLARIM PANELİ -->
            <div id="friends-panel" class="panel">
                <div class="settings-card" style="display:flex; justify-content:space-between; align-items:center; flex-wrap:wrap; gap:10px; margin-bottom:16px;">
                    <div>
                        <h1 style="font-size:22px; font-weight:800; color:var(--text-main);" id="txt-friends-title">Arkadaşlarım & Sohbet</h1>
                        <p style="font-size:13px; color:var(--text-muted);" id="txt-friends-sub">Arkadaşlarınla mesajlaş, çevrimiçi durumlarını gör ve özel skin paylaş</p>
                    </div>
                    <button class="btn-primary" onclick="openAddFriendModal()" id="txt-friends-add-btn">+ Arkadaş Ekle</button>
                </div>

                <div class="friends-container">
                    <!-- Arkadaş Listesi Sidebar -->
                    <div class="friends-sidebar">
                        <div class="friends-header">
                            <input type="text" id="friendSearchInput" class="form-control" placeholder="Arkadaş ara..." onkeyup="renderFriendsList()">
                        </div>
                        <div class="friends-list" id="friendsListContainer">
                            <!-- Dinamik arkadaşlar yüklenir -->
                        </div>
                    </div>

                    <!-- Sohbet Alanı -->
                    <div class="chat-container">
                        <div class="chat-header" id="chatHeader">
                            <div style="display:flex; align-items:center; gap:12px;">
                                <div class="friend-avatar-wrapper">
                                    <img id="activeChatAvatar" src="https://i.postimg.cc/y89X380H/shizuku-anime.png" class="friend-avatar">
                                    <span id="activeChatStatusDot" class="friend-status-dot online"></span>
                                </div>
                                <div>
                                    <div style="font-weight:800; font-size:14px;" id="activeChatName">...</div>
                                    <div style="font-size:11px; color:var(--text-muted);" id="activeChatStatusText">...</div>
                                </div>
                            </div>
                            <div style="display:flex; gap:8px;">
                                <input type="file" id="friendSkinFileInput" accept=".zip,.fantome" style="display:none;" onchange="handleFriendSkinSendFile(event)">
                                <button class="btn-primary" style="font-size:12px; padding:6px 14px;" onclick="document.getElementById('friendSkinFileInput').click()" id="txt-friends-send-skin">🎁 Skin Gönder</button>
                            </div>
                        </div>

                        <div class="chat-messages" id="chatMessagesContainer">
                            <div style="text-align:center; color:var(--text-muted); margin:auto; padding:40px;" id="txt-chat-select-friend">Sohbet etmek için sol taraftan bir arkadaşınızı seçin.</div>
                        </div>

                        <div class="chat-input-area">
                            <input type="text" id="chatMessageInput" class="form-control" placeholder="Mesajınızı yazın..." onkeydown="if(event.key==='Enter') sendChatMessage()">
                            <button class="btn-primary" onclick="sendChatMessage()" id="txt-friends-send-btn">Gönder</button>
                        </div>
                    </div>
                </div>
            </div>

            <!-- ŞAMPİYONLAR PANELİ -->
            <div id="champions-panel" class="panel">
                <div class="settings-card" style="margin-bottom:20px;">
                    <h1 style="font-size:22px; font-weight:800; color:var(--text-main);" id="txt-champ-title">Şampiyon Kütüphanesi</h1>
                    <p style="font-size:13px; color:var(--text-muted); font-weight:600;" id="txt-champ-sub">Kostümleri incelemek ve listeye eklemek için şampiyon seçin</p>
                </div>

                <div class="setting-row" id="mainFilterBar" style="margin-bottom:20px;">
                    <input type="text" id="championSearch" class="form-control" style="flex:1;" placeholder="Şampiyon ara..." onkeyup="filterChampions()">
                </div>

                <div id="championGrid" class="champion-grid"></div>

                <div id="skinViewContainer" style="display: none;">
                    <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 20px;">
                        <button class="btn-primary" onclick="backToChampionsGrid()" id="txt-back-btn">← Şampiyonlara Dön</button>
                        <h2 id="selectedChampTitleName" style="font-size: 20px; font-weight: 800; color: #fff;">Kostümler</h2>
                    </div>
                    <div id="skinGrid" class="champion-grid"></div>
                </div>
            </div>

            <!-- ÖZEL SKİNLERİM PANELİ -->
            <div id="customSkins-panel" class="panel">
                <div class="settings-card" style="display:flex; justify-content:space-between; align-items:center; flex-wrap:wrap; gap:10px;">
                    <div>
                        <h1 style="font-size:22px; font-weight:800; color:var(--text-main);" id="txt-custom-title">Özel Skinlerim</h1>
                        <p style="font-size:13px; color:var(--text-muted);" id="txt-custom-sub">Fantome (.fantome, .zip) özel kostüm dosyalarınızı yükleyin ve yönetin</p>
                    </div>
                    <button class="btn-primary" onclick="addNewSkinFile()" id="txt-add-custom-btn">+ Yeni Özel Skin Ekle (.zip / .fantome)</button>
                </div>
                
                <div class="setting-row" style="margin-bottom:20px;">
                    <input type="text" id="customSkinSearch" class="form-control" placeholder="Özel skinlerimde ara..." onkeyup="renderCustomSkins()">
                </div>

                <div id="customSkinGrid" class="custom-grid"></div>
            </div>

            <!-- MAĞAZA PANELİ -->
            <div id="store-panel" class="panel">
                <div class="settings-card" style="display:flex; justify-content:space-between; align-items:center; flex-wrap:wrap; gap:10px;">
                    <div>
                        <h1 style="font-size:22px; font-weight:800; color:var(--text-main);" id="txt-store-title">Skynix Mod Mağazası</h1>
                        <p style="font-size:13px; color:var(--text-muted);" id="txt-store-sub">Topluluk tarafından hazırlanan özel mod ve kostümleri keşfedin</p>
                    </div>
                    <button class="btn-primary" onclick="openAdminUploadModal()" id="txt-admin-upload-btn">+ Mod Yükle (Admin)</button>
                </div>

                <div class="setting-row" style="margin-bottom:16px;">
                    <input type="text" id="storeSearch" class="form-control" placeholder="Mağazada mod ara..." onkeyup="renderStoreMods(currentStoreFilter)">
                </div>

                <div class="filter-chip-list">
                    <button class="filter-chip active" onclick="filterStore('all', this)" id="txt-store-all">Tümü</button>
                    <button class="filter-chip" onclick="filterStore('free', this)" id="txt-store-free">Ücretsiz</button>
                    <button class="filter-chip" onclick="filterStore('paid', this)" id="txt-store-paid">Ücretli</button>
                    <button class="filter-chip" onclick="filterStore('champion', this)" id="txt-store-champ">Şampiyon Skins</button>
                    <button class="filter-chip" onclick="filterStore('map', this)" id="txt-store-map">Harita (Map)</button>
                    <button class="filter-chip" onclick="filterStore('hud', this)" id="txt-store-hud">HUD Arayüz</button>
                    <button class="filter-chip" onclick="filterStore('audio', this)" id="txt-store-audio">Ses Modları</button>
                </div>

                <div id="storeGrid" class="custom-grid"></div>
            </div>

            <!-- TEMALAR & TASARIM PANELİ -->
            <div id="themes-panel" class="panel">
                <div class="settings-card">
                    <h1 style="font-size:22px; font-weight:800; color:var(--text-main); margin-bottom:6px;" id="txt-themes-page-title">Tema & Görsel Tasarım Yöneticisi</h1>
                    <p style="font-size:13px; color:var(--text-muted);" id="txt-themes-page-sub">Arayüz renklerini, buton boyutlarını ve temayı bu sayfadan detaylıca kişiselleştirin.</p>
                </div>

                <div class="settings-card">
                    <h1 style="font-size:18px; font-weight:800; color:var(--text-main); margin-bottom:16px;" id="txt-scale-section-title">Başlat Butonu ve Widget Boyutları</h1>
                    
                    <div class="setting-row">
                        <div>
                            <div style="font-weight:800; color:var(--text-main);" id="txt-btn-scale-title">Başlat Butonu Büyüklüğü</div>
                            <div style="font-size:12px; color:var(--text-muted);" id="txt-btn-scale-sub">Arayüzdeki "Skinleri Başlat" butonunun ölçeği</div>
                        </div>
                        <div style="display:flex; align-items:center; gap:12px; width:220px;">
                            <input type="range" id="btnScaleRange" min="0.8" max="1.6" step="0.05" value="1" oninput="updateStartBtnScale(this.value)" style="flex:1;">
                            <span id="btnScaleValueDisplay" style="font-weight:800; font-size:12px; width:40px;">1.0x</span>
                        </div>
                    </div>

                    <div class="setting-row">
                        <div>
                            <div style="font-weight:800; color:var(--text-main);" id="txt-widget-scale-title">Launcher Widget Ölçeği</div>
                            <div style="font-size:12px; color:var(--text-muted);" id="txt-widget-scale-sub">Sağ alt köşedeki başlatıcı paneli boyutu</div>
                        </div>
                        <div style="display:flex; align-items:center; gap:12px; width:220px;">
                            <input type="range" id="widgetScaleRange" min="0.75" max="1.3" step="0.05" value="1" oninput="updateWidgetScale(this.value)" style="flex:1;">
                            <span id="widgetScaleValueDisplay" style="font-weight:800; font-size:12px; width:40px;">1.0x</span>
                        </div>
                    </div>
                </div>

                <div class="settings-card">
                    <h1 style="font-size:18px; font-weight:800; color:var(--text-main); margin-bottom:12px;" id="txt-theme-header">Özel Renk Detayları</h1>
                    <div style="font-size:12px; color:var(--text-muted); margin-bottom:16px;" id="txt-theme-sub">Uygulamanın her bölümüne özel renk atayın</div>
                    
                    <div style="display:grid; grid-template-columns: repeat(auto-fit, minmax(180px, 1fr)); gap:16px; margin-bottom:20px; background:rgba(255,255,255,0.02); padding:16px; border-radius:12px; border:1px solid var(--border-color);">
                        <div>
                            <label style="font-weight:700; font-size:11px; display:block; margin-bottom:4px;" id="txt-lbl-accent-color">Vurgu Rengi (Accent):</label>
                            <input type="color" id="accentColorPicker" value="#06b6d4" class="form-control" style="height:38px; padding:2px;" onchange="updateGranularTheme('accent', this.value)">
                        </div>
                        <div>
                            <label style="font-weight:700; font-size:11px; display:block; margin-bottom:4px;" id="txt-lbl-bg-color">Ana Arka Plan:</label>
                            <input type="color" id="bgColorPicker" value="#05070b" class="form-control" style="height:38px; padding:2px;" onchange="updateGranularTheme('bg', this.value)">
                        </div>
                        <div>
                            <label style="font-weight:700; font-size:11px; display:block; margin-bottom:4px;" id="txt-lbl-card-color">Kart Arka Planı:</label>
                            <input type="color" id="cardColorPicker" value="#0b1019" class="form-control" style="height:38px; padding:2px;" onchange="updateGranularTheme('card', this.value)">
                        </div>
                        <div>
                            <label style="font-weight:700; font-size:11px; display:block; margin-bottom:4px;" id="txt-lbl-text-color">Metin Rengi:</label>
                            <input type="color" id="textColorPicker" value="#f1f5f9" class="form-control" style="height:38px; padding:2px;" onchange="updateGranularTheme('text', this.value)">
                        </div>
                        <div>
                            <label style="font-weight:700; font-size:11px; display:block; margin-bottom:4px;" id="txt-lbl-btn-color">Başlat Butonu Rengi:</label>
                            <input type="color" id="btnColorPicker" value="#06b6d4" class="form-control" style="height:38px; padding:2px;" onchange="updateGranularTheme('btn', this.value)">
                        </div>
                    </div>

                    <div style="font-weight:800; font-size:13px; color:var(--text-main); margin-bottom:8px;" id="txt-preset-themes-lbl">Hazır Tema Paketleri</div>
                    <div class="theme-grid" id="themeGrid"></div>
                </div>

                <div class="settings-card">
                    <h1 style="font-size:18px; font-weight:800; color:var(--text-main); margin-bottom:16px;" id="txt-bg-settings-header">Görsel Ayarları</h1>

                    <div class="setting-row">
                        <div>
                            <div style="font-weight:800; color:var(--text-main);" id="txt-bg-custom-title">Uygulama Arka Plan Görseli</div>
                            <div style="font-size:12px; color:var(--text-muted);" id="txt-bg-custom-sub">JPG, PNG veya GIF görsel URL/dosyası koyun</div>
                        </div>
                        <div style="display:flex; flex-direction:column; gap:8px; width:100%; max-width:320px;">
                            <input type="text" id="appBgUrlInput" class="form-control" placeholder="Görsel URL (PNG/JPG/GIF)">
                            <div style="display:flex; gap:8px;">
                                <label class="custom-file-upload" style="flex:1;">
                                    <span id="txt-btn-upload-local-bg">📁 Dosya Yükle</span>
                                    <input type="file" id="bgLocalFileInput" accept="image/*" style="display:none;" onchange="handleBgFileUpload(event)">
                                </label>
                                <button class="btn-primary" onclick="saveCustomAppBg()"><span id="txt-btn-apply-bg">Uygula</span></button>
                            </div>
                        </div>
                    </div>

                    <div class="setting-row">
                        <div>
                            <div style="font-weight:800; color:var(--text-main);" id="txt-startbg-title">Başlat Butonu Arka Plan Görseli</div>
                            <div style="font-size:12px; color:var(--text-muted);" id="txt-startbg-sub">Buton arka planına PNG/GIF/JPG ekleyin</div>
                        </div>
                        <div style="display:flex; flex-direction:column; gap:8px; width:100%; max-width:320px;">
                            <input type="text" id="startBtnBgInput" class="form-control" placeholder="Görsel URL...">
                            <div style="display:flex; gap:8px;">
                                <label class="custom-file-upload" style="flex:1;">
                                    <span id="txt-btn-upload-startbg">📁 Dosya Yükle</span>
                                    <input type="file" id="startBtnBgFileInput" accept="image/*" style="display:none;" onchange="handleStartBtnBgFileUpload(event)">
                                </label>
                                <button class="btn-primary" onclick="saveStartBtnBg()"><span id="txt-btn-apply-startbg">Ayarla</span></button>
                            </div>
                        </div>
                    </div>

                    <div class="setting-row" style="margin-top:16px; border-top:1px solid var(--border-color); padding-top:16px;">
                        <div>
                            <div style="font-weight:800; color:var(--text-main);" id="txt-reset-vis-title">Varsayılana Sıfırla (0-la)</div>
                            <div style="font-size:12px; color:var(--text-muted);" id="txt-reset-vis-sub">Tüm yüklenmiş GIF/PNG görsellerini, renkleri ve temaları fabrika ayarlarına döndürür</div>
                        </div>
                        <button class="btn-primary" style="background:#ef4444; color:#fff;" onclick="resetVisualsToDefault()"><span id="txt-btn-reset-vis">🔄 Görselleri Sıfırla (0-la)</span></button>
                    </div>
                </div>

            </div>

            <!-- AYARLAR PANELİ -->
            <div id="settings-panel" class="panel">
                <div class="settings-card">
                    <h1 style="font-size:20px; font-weight:800; color:var(--text-main); margin-bottom:16px;" id="txt-settings-title">Uygulama Ayarları</h1>
                    
                    <div class="setting-row">
                        <div>
                            <div style="font-weight:800; color:var(--text-main);" id="txt-account-mgmt-title">Hesap Yönetimi</div>
                            <div style="font-size:12px; color:var(--text-muted);" id="txt-account-mgmt-sub">Discord hesabınız ile oturum açtınız. Rolünüz: <strong id="userRoleBadge" style="color:var(--accent-color);">Skynix Kullanıcısı</strong></div>
                        </div>
                        <div style="display:flex; gap:8px; flex-wrap:wrap;">
                            <button onclick="doLogout()" style="padding:8px 14px; background:rgba(239,68,68,0.15); border:1px solid #ef4444; color:#ef4444; border-radius:10px; font-weight:800; font-size:12px; cursor:pointer; transition:0.2s;" id="txt-btn-logout">🚪 Discord Çıkış Yap</button>
                        </div>
                    </div>

                    <div class="setting-row">
                        <div>
                            <div style="font-weight:800; color:var(--text-main);" id="txt-fps-title">Performans Modu (FPS Modu)</div>
                            <div style="font-size:12px; color:var(--text-muted);" id="txt-fps-sub">Animasyonları ve görsel efektleri kapatarak performansı artırır</div>
                        </div>
                        <label class="toggle-switch" title="Performans Modu">
                            <input type="checkbox" id="performanceModeCheckbox" onchange="togglePerformanceMode(this.checked)">
                            <span class="toggle-slider"></span>
                        </label>
                    </div>

                    <div class="setting-row">
                        <div>
                            <div style="font-weight:800; color:var(--text-main);" id="txt-setting-lang-title">Uygulama Dili / Application Language</div>
                            <div style="font-size:12px; color:var(--text-muted);" id="txt-setting-lang-sub">Arayüz dilini anında değiştirin</div>
                        </div>
                        <div style="display:flex; gap:8px;">
                            <button onclick="applyLanguage('tr')" id="btnLangTR" style="padding:8px 16px; background:var(--accent-color); color:#020617; border:none; border-radius:10px; font-weight:800; font-size:12px; cursor:pointer; transition:0.2s;">🇹🇷 Türkçe</button>
                            <button onclick="applyLanguage('en')" id="btnLangEN" style="padding:8px 16px; background:rgba(255,255,255,0.06); color:var(--text-main); border:1px solid var(--border-color); border-radius:10px; font-weight:800; font-size:12px; cursor:pointer; transition:0.2s;">🇬🇧 English</button>
                        </div>
                    </div>

                    <div class="setting-row">
                        <div>
                            <div style="font-weight:800; color:var(--text-main);" id="txt-nav-pos-title">Menü Konumu</div>
                            <div style="font-size:12px; color:var(--text-muted);" id="txt-nav-pos-sub">Sol sidebar veya üst menü barı</div>
                        </div>
                        <select id="navPosSelect" class="form-control" style="width:160px;" onchange="changeNavPosition(this.value)">
                            <option value="side" id="txt-nav-pos-side">Sol Menü (Sidebar)</option>
                            <option value="top" id="txt-nav-pos-top">Üst Menü (Topbar)</option>
                        </select>
                    </div>

                    <div class="setting-row">
                        <div>
                            <div style="font-weight:800; color:var(--text-main);" id="txt-setting-path-title">League of Legends.exe Yolu</div>
                            <div style="font-size:12px; color:var(--text-muted);" id="currentLolPathDisplay">C:/Riot Games/League of Legends/LeagueClient.exe</div>
                        </div>
                        <div style="display:flex; gap:8px;">
                            <button class="btn-primary" onclick="autoDetectLolExe()" id="txt-auto-detect">Otomatik Tara</button>
                            <input type="file" id="lolExeInput" accept=".exe" style="display:none" onchange="handleLolExeSelection(event)">
                            <button class="btn-primary" onclick="document.getElementById('lolExeInput').click()" id="txt-select-exe">Manuel Seç</button>
                        </div>
                    </div>

                    <div class="setting-row">
                        <div>
                            <div style="font-weight:800; color:var(--text-main);" id="txt-dbpath-title">Skin Veritabanı Klasörü (Skynix Data base Skins)</div>
                            <div style="font-size:12px; color:var(--text-muted);" id="currentDbPathDisplay">Henüz Seçilmedi</div>
                        </div>
                        <div style="display:flex; gap:8px; align-items:center;">
                            <button class="btn-primary" onclick="autoDetectSkinsDbFolder()" id="txt-btn-db-autodetect">Otomatik Bul</button>
                            <button class="btn-primary" onclick="selectSkinsDbFolder()" id="txt-btn-db-select">Klasör Seç</button>
                        </div>
                    </div>

                    <div class="setting-row">
                        <div>
                            <div style="font-weight:800; color:var(--text-main);" id="txt-backup-title">Veri Yedekleme ve Geri Yükleme</div>
                            <div style="font-size:12px; color:var(--text-muted);" id="txt-backup-sub">Tüm özel skin kütüphanenizi ve ayarlarınızı yedekleyin veya aktarın</div>
                        </div>
                        <div style="display:flex; gap:8px;">
                            <button class="btn-primary" onclick="exportDataBackup()" id="txt-backup-export">💾 Yedek İndir (JSON)</button>
                            <input type="file" id="importBackupInput" accept=".json" style="display:none;" onchange="importDataBackup(event)">
                            <button class="btn-primary" onclick="document.getElementById('importBackupInput').click()" id="txt-backup-import">📥 Yedek Yükle</button>
                        </div>
                    </div>
                </div>
            </div>

        </div>
    </div>

    <!-- MODALLAR -->

    <!-- DEVASA MODERN MOD BAŞLATMA OVERLAY MODALI -->
    <div id="activeLaunchModal" class="modal" style="backdrop-filter: blur(20px);">
        <div class="launch-modal-container">
            <div class="launch-modal-header">
                <div style="display:flex; align-items:center; gap:12px;">
                    <img src="https://i.hizliresim.com/7d9qpuq.png" class="wings-logo-fixed" alt="Logo">
                    <div>
                        <h2 style="font-size:18px; font-weight:800; color:#fff;" id="txt-launch-modal-title">MOD ENJEKSİYON MERKEZİ</h2>
                        <p style="font-size:12px; color:var(--accent-color); font-weight:600;" id="launchModalStatusText">CSLoL Motoru Oyuna Bağlanıyor...</p>
                    </div>
                </div>
                <button class="close-modal" onclick="closeLaunchModal()" style="background:none; border:none; color:#fff; font-size:22px; cursor:pointer;">✕</button>
            </div>

            <div class="launch-modal-body">
                <div id="launchModalCardsGrid" class="launch-cards-grid">
                    <!-- Aktif skin kartları dinamik gösterilecek -->
                </div>
            </div>

            <div class="launch-modal-footer">
                <div class="launch-progress-wrapper" style="flex:1; display:flex; flex-direction:column; gap:6px;">
                    <div class="launch-progress-info" style="display:flex; justify-content:space-between; font-size:12px; font-weight:700; color:var(--text-main);">
                        <span id="launchProgressMsg">Skin paketleri hazırlanıyor...</span>
                        <span id="launchProgressPercent">0%</span>
                    </div>
                    <div class="progress-bar-container" style="height:10px;">
                        <div class="progress-bar" id="launchProgressBar" style="width:0%;"></div>
                    </div>
                </div>
                <button class="btn-primary" onclick="closeLaunchModal()" style="padding:10px 24px; font-weight:800;" id="txt-launch-close-btn">Tamam / Oyuna Geç</button>
            </div>
        </div>
    </div>

    <!-- YENİ NESİL CHROMA MODALI (Tam Ekran ve Devasa Splash Art Destekli) -->
    <div id="chromaModal" class="modal" style="backdrop-filter: blur(15px);">
        <div class="chroma-fullscreen-container">
            <button class="close-modal chroma-close-btn" onclick="closeChromaModal()">✕ Kapat</button>
            
            <div class="chroma-hero-section">
                <img id="chromaHeroBg" src="" alt="Background">
                <div class="chroma-hero-overlay"></div>
                <img id="chromaHeroImg" src="" alt="Skin Splash">
                <h2 id="chromaModalTitle" class="chroma-hero-title">Skin Adı</h2>
            </div>

            <div class="chroma-thumbnails-wrapper">
                <div id="chromaLoadingText" style="color: var(--accent-color); font-weight: bold; font-size:16px;">Veriler Çekiliyor...</div>
                <div id="chromaThumbnailsGrid" class="chroma-thumbnails-grid">
                    <!-- Javascript ile otomatik doldurulacak -->
                </div>
            </div>
        </div>
    </div>

    <!-- PROFİL DÜZENLEME MODALI -->
    <div id="profileEditModal" class="modal">
        <div class="form-modal-content">
            <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:16px;">
                <h2 style="font-size:16px; font-weight:800; color:var(--text-main);" id="txt-modal-profile-title">Profili Düzenle</h2>
                <button class="close-modal" onclick="closeProfileEditModal()" style="background:none; border:none; color:#fff; font-size:18px; cursor:pointer;">✕</button>
            </div>
            <div class="form-group">
                <label id="txt-lbl-username">Kullanıcı Adı</label>
                <input type="text" id="editUsernameInput" class="form-control" value="Oyuncu">
            </div>
            <div class="form-group">
                <label id="txt-lbl-banner">Banner Görseli (PNG, JPG, GIF)</label>
                <input type="text" id="editBannerUrlInput" class="form-control" placeholder="https://.../banner.gif">
                <label class="custom-file-upload" style="margin-top:8px;">
                    📁 Dosya Seç
                    <input type="file" id="bannerFileInput" accept="image/*" style="display:none;" onchange="handleBannerFileUpload(event)">
                </label>
            </div>
            <div class="form-group">
                <label id="txt-lbl-avatar">Profil Resmi (PNG, JPG, GIF)</label>
                <input type="text" id="editAvatarUrlInput" class="form-control" placeholder="https://.../avatar.png">
                <label class="custom-file-upload" style="margin-top:8px;">
                    📁 Dosya Seç
                    <input type="file" id="avatarFileInput" accept="image/*" style="display:none;" onchange="handleAvatarFileUpload(event)">
                </label>
            </div>
            <button class="btn-primary" style="width:100%; justify-content:center; margin-top:10px;" onclick="saveProfileChanges()" id="txt-btn-save-profile">Kaydet</button>
        </div>
    </div>

    <!-- İSİM VE DOSYA TABANLI RESİM DÜZENLEME MODALI -->
    <div id="editSkinItemModal" class="modal">
        <div class="form-modal-content">
            <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:16px;">
                <h2 style="font-size:16px; font-weight:800; color:var(--text-main);" id="txt-modal-edit-skin">Skini Düzenle</h2>
                <button class="close-modal" onclick="closeEditSkinModal()" style="background:none; border:none; color:#fff; font-size:18px; cursor:pointer;">✕</button>
            </div>
            <div class="form-group">
                <label id="txt-lbl-editskin-name">Yeni Skin İsmi</label>
                <input type="text" id="editSkinItemNameInput" class="form-control">
            </div>
            <div class="form-group">
                <label>Skin Splash Art / Görsel Seç (JPG, PNG, GIF)</label>
                <input type="text" id="editSkinItemImgInput" class="form-control" placeholder="URL veya dosya seçin...">
                <label class="custom-file-upload" style="margin-top:8px;">
                    📁 Bilgisayardan Görsel Yükle (JPG/PNG/GIF)
                    <input type="file" id="editSkinImageFileInput" accept="image/jpeg,image/png,image/gif" style="display:none;" onchange="handleEditSkinImageUpload(event)">
                </label>
            </div>
            <button class="btn-primary" style="width:100%; justify-content:center;" onclick="saveSkinItemEdit()" id="txt-btn-save-skinedit">Değişiklikleri Kaydet</button>
        </div>
    </div>

    <!-- ADMIN MOD YÜKLEME MODALI -->
    <div id="adminUploadModal" class="modal">
        <div class="form-modal-content">
            <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:16px;">
                <h2 style="font-size:16px; font-weight:800; color:var(--text-main);" id="txt-admin-upload-head">Mağazaya Mod Yükle (Admin)</h2>
                <button class="close-modal" onclick="closeAdminUploadModal()" style="background:none; border:none; color:#fff; font-size:18px; cursor:pointer;">✕</button>
            </div>
            <div class="form-group">
                <label id="txt-lbl-admin-modtitle">Mod Adı</label>
                <input type="text" id="storeModTitle" class="form-control" placeholder="Örn: Project Vayne HUD">
            </div>
            <div class="form-group">
                <label id="txt-lbl-admin-cat">Kategori</label>
                <select id="storeModCategory" class="form-control">
                    <option value="champion">Şampiyon Skin</option>
                    <option value="map">Harita Modu</option>
                    <option value="hud">HUD Arayüz</option>
                    <option value="audio">Ses Modu</option>
                </select>
            </div>
            <div class="form-group">
                <label id="txt-lbl-admin-pricetype">Fiyat Tipi</label>
                <select id="storeModPriceType" class="form-control">
                    <option value="free">Ücretsiz / Free</option>
                    <option value="paid">Ücretli / Paid</option>
                </select>
            </div>
            <div class="form-group">
                <label id="txt-lbl-admin-file">Fantome (.fantome/.zip) Dosyası</label>
                <label class="custom-file-upload">
                    📦 Mod Zip / Fantome Seç
                    <input type="file" id="adminFantomeFile" accept=".fantome,.zip" style="display:none;">
                </label>
            </div>
            <div class="form-group">
                <label id="txt-lbl-admin-img">Önizleme Görseli (PNG/JPG/GIF)</label>
                <input type="text" id="storeModImg" class="form-control" placeholder="URL veya dosya seçin...">
                <label class="custom-file-upload" style="margin-top:8px;">
                    📁 Bilgisayardan Görsel Seç (JPG/PNG/GIF)
                    <input type="file" id="adminImageFileInput" accept="image/*" style="display:none;" onchange="handleAdminImageUpload(event)">
                </label>
            </div>
            <button class="btn-primary" style="width:100%; justify-content:center;" onclick="saveAdminStoreMod()" id="txt-btn-publish-mod">Mağazada Yayınla</button>
        </div>
    </div>

    <!-- JAVASCRIPT MOTORU -->
    <script>
        let latestLoLVersion = "14.1.1";
        let currentLang = localStorage.getItem('appLang') || 'tr';
        let allChampions = {};
        let activeQueue = [];
        let currentStoreFilter = 'all';
        let useLoadingArt = true;
        let skinsActive = false;
        let isAdminMode = localStorage.getItem('isAdminMode') === 'true';
        let customSkinsList = JSON.parse(localStorage.getItem('customSkinsList') || '[]');
        
        let activeChromaSkinTitle = "";
        let activeEditingSkinIndex = -1;
        let tempEditSkinImgData = "";

        let storeModsList = JSON.parse(localStorage.getItem('storeModsList') || '[]');

        let skinUsageCounts = JSON.parse(localStorage.getItem('skinUsageCounts') || '{}');
        let appUsageSeconds = parseInt(localStorage.getItem('appUsageSeconds') || '0');

        let tempBannerData = '';
        let tempAvatarData = '';
        
        let hiddenChampions = JSON.parse(localStorage.getItem('hiddenChampions') || '[]');

        // 21 HAZIR TEMA LİSTESİ (HER BİRİNE ÖZEL ŞAMPİYON DUVAR KAĞIDI ENTEGRELİ)
        const presetThemes = [
            { id: 'cyan', name: 'Neon Cyan', accent: '#06b6d4', bg: '#05070b', card: '#0b1019', text: '#f1f5f9', wallpaper: 'https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Yasuo_1.jpg' },
            { id: 'purple', name: 'Cyber Purple', accent: '#a855f7', bg: '#090511', card: '#150d24', text: '#f1f5f9', wallpaper: 'https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Zed_13.jpg' },
            { id: 'emerald', name: 'Emerald Dragon', accent: '#10b981', bg: '#02120d', card: '#0a1c15', text: '#f1f5f9', wallpaper: 'https://ddragon.leagueoflegends.com/cdn/img/champion/splash/LeeSin_27.jpg' },
            { id: 'crimson', name: 'Crimson Red', accent: '#ef4444', bg: '#110505', card: '#1c0a0a', text: '#f1f5f9', wallpaper: 'https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Yasuo_9.jpg' },
            { id: 'gold', name: 'Sunset Gold', accent: '#f59e0b', bg: '#120d03', card: '#1c1408', text: '#f1f5f9', wallpaper: 'https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Aatrox_8.jpg' },
            { id: 'blue', name: 'Royal Blue', accent: '#3b82f6', bg: '#040914', card: '#0a1224', text: '#f1f5f9', wallpaper: 'https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Vayne_11.jpg' },
            { id: 'pink', name: 'Rose Pink', accent: '#ec4899', bg: '#12040b', card: '#1c0a14', text: '#f1f5f9', wallpaper: 'https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Ahri_27.jpg' },
            { id: 'valorant', name: 'Valorant Red', accent: '#ff4655', bg: '#0f171e', card: '#182029', text: '#f1f5f9', wallpaper: 'https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Akali_14.jpg' },
            { id: 'arcane', name: 'Arcane Violet', accent: '#d946ef', bg: '#0f0514', card: '#1a0b21', text: '#f1f5f9', wallpaper: 'https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Jinx_37.jpg' },
            { id: 'toxic', name: 'Toxic Green', accent: '#84cc16', bg: '#070f03', card: '#101c08', text: '#f1f5f9', wallpaper: 'https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Zac_0.jpg' },
            { id: 'ice', name: 'Frostbyte', accent: '#38bdf8', bg: '#030d14', card: '#081621', text: '#f1f5f9', wallpaper: 'https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Anivia_0.jpg' },
            { id: 'orange', name: 'Solar Flare', accent: '#f97316', bg: '#120702', card: '#1c0e06', text: '#f1f5f9', wallpaper: 'https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Leona_0.jpg' },
            { id: 'darkness', name: 'Shadow Black', accent: '#64748b', bg: '#020203', card: '#0f0f12', text: '#f1f5f9', wallpaper: 'https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Nocturne_0.jpg' },
            { id: 'vaporwave', name: 'Vaporwave', accent: '#06b6d4', bg: '#18002e', card: '#280841', text: '#f1f5f9', wallpaper: 'https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Ahri_15.jpg' },
            { id: 'bloodmoon', name: 'Blood Moon', accent: '#991b1b', bg: '#080000', card: '#180404', text: '#f1f5f9', wallpaper: 'https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Yone_0.jpg' },
            { id: 'hextech', name: 'Hextech Gold', accent: '#c59b27', bg: '#051117', card: '#0a1c24', text: '#f1f5f9', wallpaper: 'https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Kassadin_6.jpg' },
            { id: 'ocean', name: 'Deep Ocean', accent: '#0284c7', bg: '#010c17', card: '#041626', text: '#f1f5f9', wallpaper: 'https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Nami_0.jpg' },
            { id: 'cherry', name: 'Cherry Blossom', accent: '#fb7185', bg: '#120508', card: '#1c0c12', text: '#f1f5f9', wallpaper: 'https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Lillia_0.jpg' },
            { id: 'mint', name: 'Mint Fresh', accent: '#2dd4bf', bg: '#021210', card: '#061c19', text: '#f1f5f9', wallpaper: 'https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Karma_0.jpg' },
            { id: 'slate', name: 'Minimal Slate', accent: '#94a3b8', bg: '#0f172a', card: '#1e293b', text: '#f1f5f9', wallpaper: 'https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Pantheon_1.jpg' },
            { id: 'neon', name: 'Cyber Neon', accent: '#ccff00', bg: '#050a00', card: '#0c1600', text: '#f1f5f9', wallpaper: 'https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Ekko_19.jpg' }
        ];

        const dictionary = {
            tr: {
                loadSubtitle: "Veriler hazırlanıyor...",
                clientStatus: "LOL BAĞLI",
                navHome: "Ana Ekran",
                navProfile: "Profilim",
                navFriends: "Arkadaşlarım",
                navChampions: "Şampiyonlar",
                navCustom: "Özel Skinlerim",
                navStore: "Mağaza",
                navThemes: "Temalar & Tasarım",
                navSettings: "Ayarlar",
                homeSub: "Skynix ile Favori Kostümlerini Yönet ve Sihirdar Vadisi'ne Hükmet",
                discordBtn: "Discord Sunucumuza Katıl",
                statCustoms: "Yüklü Özel Skin",
                statActiveq: "Sıradaki Modlar",
                statTimer: "Toplam Süre",
                tagLegendary: "Efsanevi Kostümler",
                tagFeatured: "Öne Çıkan Modlar",
                tagCustomHud: "Özel HUD & Ses",
                homeNewsTitle: "Güncelleme Haberleri",
                homeNewsBody: "• <strong>NextGen v3.0</strong> sürümüne geçildi!<br>• Otomatik `installed/` klasörüne kopyalama ve sabitleme sistemi eklendi.<br>• Canlı enjektör terminal log konsolu entegre edildi.<br>• Oyun klasörü otomatik tespit motoru güncellendi.",
                homeStoreNewTitle: "Mağazaya Yeni Gelenler",
                homeStoreNewBody: "🔥 Cyberpunk Yasuo HUD Modu<br>🔥 Arcane Jinx Özel Ses Paketi<br>🔥 K/DA Ahri Özel Harita Teması",
                homeFeaturesTitle: "Uygulama Özellikleri",
                homeFeaturesBody: "⚡ Akıllı Dosya Eşleştirme & Otomatik Splash Art Çekici<br>🎨 Özelleştirilebilir 20+ Tema seçeneği<br>🎵 Dahili ve Sabit Spotify Playlist desteği",
                profileSub: "Skynix Koleksiyoneri & Tasarımcı",
                editProfileBtn: "Profili Düzenle",
                statTime: "Uygulamada Geçirilen Süre",
                statSkins: "Özel Kostüm Sayısı",
                statTopSkin: "En Çok Çalıştırılan Skin",
                spotifyTitle: "Spotify Favori Playlist",
                spotifySave: "Güncelle & Sabitle",
                champTitle: "Şampiyon Kütüphanesi",
                champSub: "Kostümleri incelemek ve listeye eklemek için şampiyon seçin",
                toggleArtBtn: useLoadingArt ? "Görünüm: Portre (Loading Art)" : "Görünüm: Yatay Splash",
                backBtn: "← Şampiyonlara Dön",
                customTitle: "Özel Skinlerim",
                customSub: "Fantome (.fantome, .zip) özel kostüm dosyalarınızı yükleyin ve yönetin",
                addCustomBtn: "+ Yeni Özel Skin Ekle (.zip / .fantome)",
                storeTitle: "Skynix Mod Mağazası",
                storeSub: "Topluluk tarafından hazırlanan özel mod ve kostümleri keşfedin",
                adminUploadBtn: "+ Mod Yükle (Admin)",
                storeAll: "Tümü",
                storeFree: "Ücretsiz",
                storePaid: "Ücretli",
                storeChamp: "Şampiyon Skins",
                storeMap: "Harita (Map)",
                storeHud: "HUD Arayüz",
                storeAudio: "Ses Modları",
                settingsTitle: "Uygulama Ayarları",
                settingLangTitle: "Uygulama Dili",
                settingLangSub: "Arayüz ve şampiyon dilini değiştirin",
                navPosTitle: "Menü Konumu",
                navPosSub: "Sol sidebar veya üst menü barı",
                navPosSide: "Sol Menü (Sidebar)",
                navPosTop: "Üst Menü (Topbar)",
                settingPathTitle: "League of Legends.exe Yolu",
                autoDetect: "Otomatik Tara",
                selectExe: "Manuel Seç",
                backupTitle: "Veri Yedekleme ve Geri Yükleme",
                backupSub: "Tüm özel skin kütüphanenizi ve ayarlarınızı yedekleyin veya aktarın",
                backupExport: "💾 Yedek İndir (JSON)",
                backupImport: "📥 Yedek Yükle",
                bgHeader: "Görsel Ayarları",
                bgCustomTitle: "Uygulama Arka Plan Görseli",
                bgCustomSub: "JPG, PNG veya GIF görsel URL/dosyası koyun",
                btnUploadLocalBg: "📁 Dosya Yükle",
                btnApplyBg: "Uygula",
                startbgTitle: "Başlat Butonu Arka Plan Görseli",
                startbgSub: "Buton arka planına PNG/GIF/JPG ekleyin",
                btnUploadStartBg: "📁 Dosya Yükle",
                btnApplyStartBg: "Ayarla",
                themeHeader: "Tema & Özel Renk Ayarları",
                themeSub: "Uygulamanın her bölümüne özel renk atayın veya hazır temalardan birini seçin",
                lblAccentColor: "Vurgu Rengi (Accent):",
                lblBgColor: "Ana Arka Plan:",
                lblCardColor: "Kart Arka Planı:",
                lblTextColor: "Metin Rengi:",
                lblBtnColor: "Başlat Butonu Rengi:",
                presetThemesLbl: "Hazır Tema Paketleri",
                scaleSectionTitle: "Başlat Butonu ve Widget Boyutları",
                btnScaleTitle: "Başlat Butonu Büyüklüğü",
                btnScaleSub: "Arayüzdeki 'Skinleri Başlat' butonunun ölçeği",
                widgetScaleTitle: "Launcher Widget Ölçeği",
                widgetScaleSub: "Sağ alt köşedeki başlatıcı paneli boyutu",
                queueTitle: "Seçili Modlar (Sıradaki)",
                queueEmpty: "Çalıştırılacak mod bulunmuyor.",
                startBtn: "SKİNLERİ BAŞLAT",
                lblUsername: "Kullanıcı Adı",
                lblBanner: "Banner Görseli (PNG, JPG, GIF)",
                lblAvatar: "Profil Resmi (PNG, JPG, GIF)",
                btnSaveProfile: "Kaydet",
                modalProfileTitle: "Profili Düzenle",
                modalEditSkin: "Skini Düzenle",
                lblEditSkinName: "Yeni Skin İsmi",
                lblEditSkinImg: "Yeni Görsel / PNG / JPG / GIF URL",
                btnSaveSkinEdit: "Değişiklikleri Kaydet",
                adminUploadHead: "Mağazaya Mod Yükle (Admin)",
                lblAdminModTitle: "Mod Adı",
                lblAdminCat: "Kategori",
                lblAdminPriceType: "Fiyat Tipi",
                lblAdminFile: "Fantome (.fantome/.zip) Dosyası",
                lblAdminImg: "Önizleme Görsel URL (PNG/JPG/GIF)",
                btnPublishMod: "Mağazada Yayınla",
                dragDropLabel: "Sadece .ZIP veya .FANTOME Dosyası Bırakın",
                themesPageTitle: "Tema & Görsel Tasarım Yöneticisi",
                themesPageSub: "Arayüz renklerini, buton boyutlarını ve temayı bu sayfadan detaylıca kişiselleştirin.",
                searchCustomPlaceholder: "Özel skinlerimde ara...",
                modFileBadge: "MOD DOSYASI",
                queueAddRemove: "Sıraya Ekle / Çıkar",
                btnEdit: "✏️ Düzenle",
                btnDelete: "🗑️ Sil",
                storeSearchPlaceholder: "Mağazada mod ara...",
                badgeFree: "ÜCRETSİZ",
                badgePaid: "ÜCRETLİ",
                btnDownloadAdd: "📥 İndir & Ekle",
                spotifyPlaceholder: "Spotify Playlist URL veya Embed Linki girin...",
                showcaseTitle1: "Gece Getiren Yasuo",
                showcaseTitle2: "Galaksi Katili Zed",
                showcaseTitle3: "PROJECT: Vayne",
                friendsTitle: "Arkadaşlarım & Sohbet",
                friendsSub: "Arkadaşlarınla mesajlaş, çevrimiçi durumlarını gör ve özel skin paylaş",
                friendsAddBtn: "+ Arkadaş Ekle",
                friendsSendSkin: "🎁 Skin Gönder",
                friendsSendBtn: "Gönder",
                friendsChatEmpty: "Sohbet etmek için sol taraftan bir arkadaşınızı seçin.",
                friendsChatSelectName: "Bir arkadaş seçin",
                friendsChatSelectStatus: "Sohbet başlatmak için tıklayın",
                friendsMsgPlaceholder: "Mesajınızı yazın...",
                friendsSearchPlaceholder: "Arkadaş ara...",
                homeFeaturesHeader: "Uygulama Özellikleri",
                featCustomTitle: "Özel Skin Yöneticisi",
                featCustomDesc: "Kendi .fantome ve .zip skin dosyalarını yükle, yönet ve tek tıkla etkinleştir.",
                featChampTitle: "Şampiyon Kütüphanesi",
                featChampDesc: "165+ şampiyon ve tüm skin splash artlarına göz at, favori kostümünü kuyruğa ekle.",
                featThemeTitle: "Tema & Tasarım",
                featThemeDesc: "20+ hazır tema paketi ve tam özelleştirilebilir renk sistemiyle arayüzü kişiselleştir.",
                featStoreTitle: "Topluluk Mağazası",
                featStoreDesc: "Topluluk tarafından yapılan özel mod paketlerini keşfet ve bir tıkla yükle.",
                featFriendsTitle: "Arkadaşlar & Sohbet",
                featFriendsDesc: "Arkadaşlarınla gerçek zamanlı mesajlaş, çevrimiçi durumlarını gör ve skin paylaş.",
                featSmartTitle: "Akıllı Dosya Eşleştirme",
                featSmartDesc: "Yüklediğin skin dosyasından otomatik şampiyon tespiti ve splash art çekme sistemi.",
                emptyCustomSkins: "Henüz eklenmiş özel skin bulunmuyor.",
                chromaTitle: "Renk Paketleri (Chromas)",
                btnSelectChroma: "Bu Rengi Seç",
                resetVisTitle: "Varsayılana Sıfırla (0-la)",
                resetVisSub: "Tüm yüklenmiş GIF/PNG görsellerini, renkleri ve temaları fabrika ayarlarına döndürür",
                btnResetVis: "🔄 Görselleri Sıfırla (0-la)",
                accountMgmtTitle: "Hesap Yönetimi",
                btnLogout: "🚪 Discord Çıkış Yap",
                fpsTitle: "Performans Modu (FPS Modu)",
                fpsSub: "Animasyonları ve görsel efektleri kapatarak performansı artırır",
                dbpathTitle: "Skin Veritabanı Klasörü (Skynix Data base Skins)",
                btnDbAuto: "Otomatik Bul",
                btnDbSelect: "Klasör Seç"
            },
            en: {
                friendsTitle: "My Friends & Chat",
                friendsSub: "Chat with friends, view online status, and share custom skins",
                friendsAddBtn: "+ Add Friend",
                friendsSendSkin: "🎁 Send Skin",
                friendsSendBtn: "Send",
                friendsChatEmpty: "Select a friend from the left to start chatting.",
                friendsChatSelectName: "Select a friend",
                friendsChatSelectStatus: "Click to start a chat",
                friendsMsgPlaceholder: "Type your message...",
                friendsSearchPlaceholder: "Search friends...",
                homeFeaturesHeader: "App Features",
                featCustomTitle: "Custom Skin Manager",
                featCustomDesc: "Upload, manage and activate your .fantome and .zip skin files with one click.",
                featChampTitle: "Champion Library",
                featChampDesc: "Browse 165+ champions and all skin splash arts, add your favorites to the queue.",
                featThemeTitle: "Themes & Design",
                featThemeDesc: "Customize interface colors and button sizes with 20+ preset theme packs.",
                featStoreTitle: "Community Store",
                featStoreDesc: "Discover custom mod packs created by the community and install with one click.",
                featFriendsTitle: "Friends & Chat",
                featFriendsDesc: "Chat with friends in real-time, view online status and share skins.",
                featSmartTitle: "Smart File Matching",
                featSmartDesc: "Auto-detect champion from your skin file name and fetch matching splash art.",
                loadSubtitle: "Preparing data...",
                clientStatus: "LOL CONNECTED",
                navHome: "Home",
                navProfile: "My Profile",
                navFriends: "Friends",
                navChampions: "Champions",
                navCustom: "Custom Skins",
                navStore: "Store",
                navThemes: "Themes & Design",
                navSettings: "Settings",
                homeSub: "Manage your favorite skins and dominate Summoner's Rift with Skynix",
                discordBtn: "Join Our Discord Server",
                statCustoms: "Installed Custom Skins",
                statActiveq: "Queue Mods",
                statTimer: "Total Time Spent",
                tagLegendary: "Legendary Skins",
                tagFeatured: "Featured Mods",
                tagCustomHud: "Custom HUD & Audio",
                homeNewsTitle: "Update News",
                homeNewsBody: "• <strong>NextGen v3.0</strong> is live!<br>• Auto-copy and persistence to `installed/` folder integrated.<br>• Live injector console log added.<br>• Game directory auto-detector updated.",
                homeStoreNewTitle: "New Store Arrivals",
                homeStoreNewBody: "🔥 Cyberpunk Yasuo HUD Mod<br>🔥 Arcane Jinx Voice Pack<br>🔥 K/DA Ahri Map Skin",
                homeFeaturesTitle: "App Key Features",
                homeFeaturesBody: "⚡ Smart File Reader & Automatic Splash Art Fetcher<br>🎨 Customizable 20+ Theme options<br>🎵 Built-in and Pinned Spotify Playlist support",
                profileSub: "Skynix Collector & Designer",
                editProfileBtn: "Edit Profile",
                statTime: "Time Spent in App",
                statSkins: "Custom Skin Count",
                statTopSkin: "Most Played Skin",
                spotifyTitle: "Spotify Favorite Playlist",
                spotifySave: "Update & Pin",
                champTitle: "Champion Library",
                champSub: "Select a champion to view and add skins to the queue",
                toggleArtBtn: useLoadingArt ? "View: Portrait (Loading Art)" : "View: Horizontal Splash",
                backBtn: "← Back to Champions",
                customTitle: "My Custom Skins",
                customSub: "Upload and manage your Fantome (.fantome, .zip) custom skin files",
                addCustomBtn: "+ Add New Custom Skin (.zip / .fantome)",
                storeTitle: "Skynix Mod Store",
                storeSub: "Discover custom mods and skins created by the community",
                adminUploadBtn: "+ Upload Mod (Admin)",
                storeAll: "All",
                storeFree: "Free",
                storePaid: "Paid",
                storeChamp: "Champion Skins",
                storeMap: "Map Mods",
                storeHud: "HUD Interface",
                storeAudio: "Audio Mods",
                settingsTitle: "Application Settings",
                settingLangTitle: "Application Language",
                settingLangSub: "Change the interface and champion language",
                navPosTitle: "Menu Position",
                navPosSub: "Left sidebar or top menu bar",
                navPosSide: "Left Sidebar",
                navPosTop: "Top Menu",
                settingPathTitle: "League of Legends.exe Path",
                autoDetect: "Auto Detect",
                selectExe: "Select Manually",
                backupTitle: "Data Backup & Restore",
                backupSub: "Backup or restore all your custom skins library and settings",
                backupExport: "💾 Export Backup (JSON)",
                backupImport: "📥 Import Backup",
                bgHeader: "Visual Settings",
                bgCustomTitle: "Application Background Image",
                bgCustomSub: "Set JPG, PNG or GIF image URL or file",
                btnUploadLocalBg: "📁 Upload File",
                btnApplyBg: "Apply",
                startbgTitle: "Start Button Background Image",
                startbgSub: "Add PNG/GIF/JPG to the button background",
                btnUploadStartBg: "📁 Upload File",
                btnApplyStartBg: "Set",
                themeHeader: "Theme & Custom Color Settings",
                themeSub: "Assign custom colors to each section or pick a preset theme",
                lblAccentColor: "Accent Color:",
                lblBgColor: "Main Background:",
                lblCardColor: "Card Background:",
                lblTextColor: "Text Color:",
                lblBtnColor: "Start Button Color:",
                presetThemesLbl: "Preset Theme Packs",
                scaleSectionTitle: "Start Button & Widget Sizes",
                btnScaleTitle: "Start Button Size Scale",
                btnScaleSub: "Scale size of the 'Launch Skins' button",
                widgetScaleTitle: "Launcher Widget Scale",
                widgetScaleSub: "Scale size of the bottom-right launcher panel",
                queueTitle: "Selected Mods (Queue)",
                queueEmpty: "No mod to run.",
                startBtn: "LAUNCH SKINS",
                lblUsername: "Username",
                lblBanner: "Banner Image (PNG, JPG, GIF)",
                lblAvatar: "Profile Picture (PNG, JPG, GIF)",
                btnSaveProfile: "Save",
                modalProfileTitle: "Edit Profile",
                modalEditSkin: "Edit Skin",
                lblEditSkinName: "New Skin Name",
                lblEditSkinImg: "New Image / PNG / JPG / GIF URL",
                btnSaveSkinEdit: "Save Changes",
                adminUploadHead: "Upload Mod to Store (Admin)",
                lblAdminModTitle: "Mod Title",
                lblAdminCat: "Category",
                lblAdminPriceType: "Price Type",
                lblAdminFile: "Fantome (.fantome/.zip) File",
                lblAdminImg: "Preview Image URL (PNG/JPG/GIF)",
                btnPublishMod: "Publish in Store",
                dragDropLabel: "Drop Only .ZIP or .FANTOME Files Here",
                themesPageTitle: "Theme & Visual Design Manager",
                themesPageSub: "Customize interface colors, button sizes, and theme in detail from this page.",
                searchCustomPlaceholder: "Search in my custom skins...",
                modFileBadge: "MOD FILE",
                queueAddRemove: "Add / Remove Queue",
                btnEdit: "✏️ Edit",
                btnDelete: "🗑️ Delete",
                storeSearchPlaceholder: "Search mods in store...",
                badgeFree: "FREE",
                badgePaid: "PAID",
                btnDownloadAdd: "📥 Download & Add",
                spotifyPlaceholder: "Enter Spotify Playlist URL or Embed Link...",
                showcaseTitle1: "Nightbringer Yasuo",
                showcaseTitle2: "Galaxy Slayer Zed",
                showcaseTitle3: "PROJECT: Vayne",
                emptyCustomSkins: "No custom skins added yet.",
                chromaTitle: "Chromas",
                btnSelectChroma: "Select This Chroma",
                resetVisTitle: "Reset to Default",
                resetVisSub: "Resets all loaded GIF/PNG visuals, colors and themes to factory settings",
                btnResetVis: "🔄 Reset Visuals",
                accountMgmtTitle: "Account Management",
                btnLogout: "🚪 Sign Out of Discord",
                fpsTitle: "Performance Mode (FPS Mode)",
                fpsSub: "Boost performance by disabling animations and visual effects",
                dbpathTitle: "Skin Database Folder (Skynix Data base Skins)",
                btnDbAuto: "Auto Find",
                btnDbSelect: "Select Folder"
            }
        };

        function applyLanguage(lang) {
            currentLang = lang;
            localStorage.setItem('appLang', lang);
            const dict = dictionary[lang];
            // Null-safe setter — element yoksa sessizce geç
            const setText = (id, val) => { const el = document.getElementById(id); if (el) el.innerText = val; };
            const setHTML = (id, val) => { const el = document.getElementById(id); if (el) el.innerHTML = val; };
            const setPlaceholder = (id, val) => { const el = document.getElementById(id); if (el) el.placeholder = val; };

            document.getElementById('loadSubtitle').innerText = dict.loadSubtitle;
            document.getElementById('txt-client-status').innerText = dict.clientStatus;
            setText('txt-nav-home', dict.navHome);
            setText('txt-nav-profile', dict.navProfile);
            setText('txt-nav-friends', dict.navFriends);
            setText('txt-nav-champions', dict.navChampions);
            setText('txt-nav-custom', dict.navCustom);
            setText('txt-nav-store', dict.navStore);
            setText('txt-nav-themes', dict.navThemes);
            setText('txt-nav-settings', dict.navSettings);
            
            setText('txt-home-sub', dict.homeSub);
            setText('txt-discord-btn', dict.discordBtn);
            setText('txt-stat-customs', dict.statCustoms);
            setText('txt-stat-activeq', dict.statActiveq);
            setText('txt-stat-timer', dict.statTimer);
            // Showcase tags - null check (eski id'ler kaldırıldı)
            const sc1 = document.getElementById('txt-showcase-1');
            const sc2 = document.getElementById('txt-showcase-2');
            const sc3 = document.getElementById('txt-showcase-3');
            if (sc1 && dict.showcaseTitle1) sc1.innerText = dict.showcaseTitle1;
            if (sc2 && dict.showcaseTitle2) sc2.innerText = dict.showcaseTitle2;
            if (sc3 && dict.showcaseTitle3) sc3.innerText = dict.showcaseTitle3;

            setPlaceholder('customSkinSearch', dict.searchCustomPlaceholder);
            setPlaceholder('storeSearch', dict.storeSearchPlaceholder);
            setPlaceholder('spotifyEmbedInput', dict.spotifyPlaceholder);
            setPlaceholder('friendSearchInput', dict.friendsSearchPlaceholder);
            setPlaceholder('chatMessageInput', dict.friendsMsgPlaceholder);

            setText('txt-friends-add-btn', dict.friendsAddBtn);
            setText('txt-friends-send-skin', dict.friendsSendSkin);
            setText('txt-friends-send-btn', dict.friendsSendBtn);
            setText('txt-chat-select-friend', dict.friendsChatEmpty);
            setText('txt-home-features-header', dict.homeFeaturesHeader);
            setText('txt-feat-custom-title', dict.featCustomTitle);
            setText('txt-feat-custom-desc', dict.featCustomDesc);
            setText('txt-feat-champ-title', dict.featChampTitle);
            setText('txt-feat-champ-desc', dict.featChampDesc);
            setText('txt-feat-theme-title', dict.featThemeTitle);
            setText('txt-feat-theme-desc', dict.featThemeDesc);
            setText('txt-feat-store-title', dict.featStoreTitle);
            setText('txt-feat-store-desc', dict.featStoreDesc);
            setText('txt-feat-friends-title', dict.featFriendsTitle);
            setText('txt-feat-friends-desc', dict.featFriendsDesc);
            setText('txt-feat-smart-title', dict.featSmartTitle);
            setText('txt-feat-smart-desc', dict.featSmartDesc);

            setText('txt-profile-sub', dict.profileSub);
            setHTML('txt-home-news-body', dict.homeNewsBody);
            setHTML('txt-home-storenew-title', `<svg class="icon-svg icon-lg" viewBox="0 0 24 24"><path d="M7 18c-1.1 0-1.99.9-1.99 2S5.9 22 7 22s2-.9 2-2-.9-2-2-2zM1 2v2h2l3.6 7.59-1.35 2.45c-.16.28-.25.61-.25.96 0 1.1.9 2 2 2h12v-2H7.42c-.14 0-.25-.11-.25-.25l.03-.12.9-1.63h7.45c.75 0 1.41-.41 1.75-1.03l3.58-6.49c.08-.14.12-.31.12-.48 0-.55-.45-1-1-1H5.21l-.94-2H1zm16 16c-1.1 0-1.99 2s.89 2 1.99 2 2-.9 2-2-.9-2-2-2z"/></svg> ${dict.homeStoreNewTitle}`);
            setHTML('txt-home-storenew-body', dict.homeStoreNewBody);
            setHTML('txt-home-features-title', `<svg class="icon-svg icon-lg" viewBox="0 0 24 24"><path d="M12 2L1 21h22L12 2zm0 3.8L19.3 19H4.7L12 5.8z"/></svg> ${dict.homeFeaturesTitle}`);
            setHTML('txt-home-features-body', dict.homeFeaturesBody);

            setText('txt-profile-sub', dict.profileSub);
            setText('txt-edit-profile-btn', dict.editProfileBtn);
            setText('txt-stat-time', dict.statTime);
            setText('txt-stat-skins', dict.statSkins);
            setText('txt-stat-topskin', dict.statTopSkin);
            
            setText('txt-spotify-title', dict.spotifyTitle);
            setText('txt-spotify-save', dict.spotifySave);

            setText('txt-champ-title', dict.champTitle);
            setText('txt-champ-sub', dict.champSub);
            setText('txt-toggle-art-btn', dict.toggleArtBtn);
            setText('txt-back-btn', dict.backBtn);

            setText('txt-custom-title', dict.customTitle);
            setText('txt-custom-sub', dict.customSub);
            setText('txt-add-custom-btn', dict.addCustomBtn);

            setText('txt-friends-title', dict.friendsTitle);
            setText('txt-friends-sub', dict.friendsSub);

            setText('txt-store-title', dict.storeTitle);
            setText('txt-store-sub', dict.storeSub);
            setText('txt-admin-upload-btn', dict.adminUploadBtn);
            setText('txt-store-all', dict.storeAll);
            setText('txt-store-free', dict.storeFree);
            setText('txt-store-paid', dict.storePaid);
            setText('txt-store-champ', dict.storeChamp);
            setText('txt-store-map', dict.storeMap);
            setText('txt-store-hud', dict.storeHud);
            setText('txt-store-audio', dict.storeAudio);

            setText('txt-settings-title', dict.settingsTitle);
            setText('txt-setting-lang-title', dict.settingLangTitle);
            setText('txt-setting-lang-sub', dict.settingLangSub);
            setText('txt-nav-pos-title', dict.navPosTitle);
            setText('txt-nav-pos-sub', dict.navPosSub);
            setText('txt-nav-pos-side', dict.navPosSide);
            setText('txt-nav-pos-top', dict.navPosTop);
            setText('txt-setting-path-title', dict.settingPathTitle);
            setText('txt-auto-detect', dict.autoDetect);
            setText('txt-select-exe', dict.selectExe);

            setText('txt-fps-title', dict.fpsTitle);
            setText('txt-fps-sub', dict.fpsSub);
            setText('txt-dbpath-title', dict.dbpathTitle);
            setText('txt-btn-db-autodetect', dict.btnDbAuto);
            setText('txt-btn-db-select', dict.btnDbSelect);
            setText('txt-account-mgmt-title', dict.accountMgmtTitle);
            setText('txt-btn-logout', dict.btnLogout);
            setText('txt-reset-vis-title', dict.resetVisTitle);
            setText('txt-reset-vis-sub', dict.resetVisSub);
            setText('txt-btn-reset-vis', dict.btnResetVis);

            setText('txt-backup-title', dict.backupTitle);
            setText('txt-backup-sub', dict.backupSub);
            setText('txt-backup-export', dict.backupExport);
            setText('txt-backup-import', dict.backupImport);

            setText('txt-themes-page-title', dict.themesPageTitle);
            setText('txt-themes-page-sub', dict.themesPageSub);

            setText('txt-scale-section-title', dict.scaleSectionTitle);
            setText('txt-btn-scale-title', dict.btnScaleTitle);
            setText('txt-btn-scale-sub', dict.btnScaleSub);
            setText('txt-widget-scale-title', dict.widgetScaleTitle);
            setText('txt-widget-scale-sub', dict.widgetScaleSub);

            setText('txt-bg-settings-header', dict.bgHeader);
            setText('txt-bg-custom-title', dict.bgCustomTitle);
            setText('txt-bg-custom-sub', dict.bgCustomSub);
            setText('txt-btn-upload-local-bg', dict.btnUploadLocalBg);
            setText('txt-btn-apply-bg', dict.btnApplyBg);

            setText('txt-startbg-title', dict.startbgTitle);
            setText('txt-startbg-sub', dict.startbgSub);
            setText('txt-btn-upload-startbg', dict.btnUploadStartBg);
            setText('txt-btn-apply-startbg', dict.btnApplyStartBg);

            setText('txt-theme-header', dict.themeHeader);
            setText('txt-theme-sub', dict.themeSub);
            setText('txt-lbl-accent-color', dict.lblAccentColor);
            setText('txt-lbl-bg-color', dict.lblBgColor);
            setText('txt-lbl-card-color', dict.lblCardColor);
            setText('txt-lbl-text-color', dict.lblTextColor);
            setText('txt-lbl-btn-color', dict.lblBtnColor);
            setText('txt-preset-themes-lbl', dict.presetThemesLbl);

            setText('txt-drag-drop-label', dict.dragDropLabel);

            setText('txt-lbl-username', dict.lblUsername);
            setText('txt-lbl-banner', dict.lblBanner);
            setText('txt-lbl-avatar', dict.lblAvatar);
            setText('txt-btn-save-profile', dict.btnSaveProfile);

            setText('txt-modal-profile-title', dict.modalProfileTitle);
            setText('txt-modal-edit-skin', dict.modalEditSkin);
            setText('txt-lbl-editskin-name', dict.lblEditSkinName);
            setText('txt-btn-save-skinedit', dict.btnSaveSkinEdit);

            setText('txt-admin-upload-head', dict.adminUploadHead);
            setText('txt-lbl-admin-modtitle', dict.lblAdminModTitle);
            setText('txt-lbl-admin-cat', dict.lblAdminCat);
            setText('txt-lbl-admin-pricetype', dict.lblAdminPriceType);
            setText('txt-lbl-admin-file', dict.lblAdminFile);
            setText('txt-lbl-admin-img', dict.lblAdminImg);
            setText('txt-btn-publish-mod', dict.btnPublishMod);
            
            renderActiveLauncherWidget();
            renderCustomSkins();
            renderStoreMods(currentStoreFilter);

            const startBtnText = document.getElementById('txt-start-btn');
            if (startBtnText) {
                if (skinsActive) {
                    startBtnText.innerText = lang === 'tr' ? 'SKİNLERİ DURDUR' : 'STOP SKINS';
                } else {
                    startBtnText.innerText = dict.startBtn || (lang === 'tr' ? 'SKİNLERİ BAŞLAT' : 'LAUNCH SKINS');
                }
            }

            const btnTR = document.getElementById('btnLangTR');
            const btnEN = document.getElementById('btnLangEN');
            if (btnTR && btnEN) {
                if (lang === 'tr') {
                    btnTR.style.background = 'var(--accent-color)';
                    btnTR.style.color = '#020617';
                    btnEN.style.background = 'rgba(255,255,255,0.06)';
                    btnEN.style.color = 'var(--text-main)';
                } else {
                    btnEN.style.background = 'var(--accent-color)';
                    btnEN.style.color = '#020617';
                    btnTR.style.background = 'rgba(255,255,255,0.06)';
                    btnTR.style.color = 'var(--text-main)';
                }
            }
            // Dil değişince şampiyon grid'ini de yeni dilde yenile
            if (allChampions && Object.keys(allChampions).length > 0) {
                fetchChampions();
            }
        }

        function showToast(msg) {
            const container = document.getElementById('toastContainer');
            const toast = document.createElement('div');
            toast.className = 'app-toast';
            toast.innerHTML = `<svg class="icon-svg" viewBox="0 0 24 24" style="color:var(--accent-color);"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-2 15l-5-5 1.41-1.41L10 14.17l7.59-7.59L19 8l-9 9z"/></svg> <span>${msg}</span>`;
            container.appendChild(toast);
            setTimeout(() => {
                toast.style.opacity = '0';
                setTimeout(() => toast.remove(), 300);
            }, 3000);
        }

        function appendLog(msg, type = 'info') {
            const box = document.getElementById('liveTerminalBox');
            if (!box) return;
            const entry = document.createElement('div');
            entry.className = `log-entry ${type}`;
            entry.innerText = msg;
            box.appendChild(entry);
            box.scrollTop = box.scrollHeight;
        }

        function toggleTerminalView() {
            const box = document.getElementById('liveTerminalBox');
            const widget = document.getElementById('activeLauncherWidget');
            if (box && widget) {
                box.classList.toggle('active');
                widget.classList.toggle('expanded');
            }
        }

        function renderThemeGrid() {
            const grid = document.getElementById('themeGrid');
            grid.innerHTML = '';
            presetThemes.forEach(t => {
                grid.innerHTML += `
                    <div class="theme-card" onclick="applyPresetTheme('${t.id}')">
                        <div class="theme-preview-box" style="background: linear-gradient(135deg, ${t.bg} 0%, ${t.accent} 100%);"></div>
                        ${t.name}
                    </div>
                `;
            });
        }

        function applyPresetTheme(themeId) {
            const t = presetThemes.find(x => x.id === themeId);
            if (!t) return;
            
            document.documentElement.style.setProperty('--accent-color', t.accent);
            document.documentElement.style.setProperty('--accent-glow', `${t.accent}59`);
            document.documentElement.style.setProperty('--bg-main', t.bg);
            document.documentElement.style.setProperty('--bg-card', t.card);
            document.documentElement.style.setProperty('--text-main', t.text);
            document.documentElement.style.setProperty('--start-btn-bg', t.accent);

            document.getElementById('accentColorPicker').value = t.accent;
            document.getElementById('bgColorPicker').value = t.bg;
            document.getElementById('cardColorPicker').value = t.card;
            document.getElementById('textColorPicker').value = t.text;
            document.getElementById('btnColorPicker').value = t.accent;

            if (t.wallpaper) {
                document.getElementById('mainAppBackground').src = t.wallpaper;
                document.getElementById('appBgUrlInput').value = t.wallpaper;
                localStorage.setItem('appBgUrl', t.wallpaper);
            }

            localStorage.setItem('themeAccent', t.accent);
            localStorage.setItem('themeBg', t.bg);
            localStorage.setItem('themeCard', t.card);
            localStorage.setItem('themeText', t.text);
            localStorage.setItem('themeBtn', t.accent);
            
            showToast(currentLang === 'tr' ? `Tema ve Duvar Kağıdı uygulandı: ${t.name}` : `Theme & Wallpaper applied: ${t.name}`);
        }

        function resetVisualsToDefault() {
            localStorage.removeItem('appBgUrl');
            localStorage.removeItem('startBtnBg');
            localStorage.removeItem('themeAccent');
            localStorage.removeItem('themeBg');
            localStorage.removeItem('themeCard');
            localStorage.removeItem('themeText');
            localStorage.removeItem('themeBtn');
            localStorage.removeItem('startBtnScale');
            localStorage.removeItem('widgetScale');

            document.documentElement.style.setProperty('--start-btn-img', 'none');
            const masterBtn = document.getElementById('masterStartBtn');
            if (masterBtn) masterBtn.style.backgroundImage = 'none';
            if (document.getElementById('startBtnBgInput')) document.getElementById('startBtnBgInput').value = '';

            applyPresetTheme('cyan');
            updateStartBtnScale(1);
            updateWidgetScale(1);

            showToast(currentLang === 'tr' ? 'Tüm görseller, GIF\'ler ve temalar varsayılana sıfırlandı! (0-landı)' : 'All visuals, GIFs and themes reset to default!');
        }

        function toggleAdminMode(enabled) {
            isAdminMode = enabled;
            localStorage.setItem('isAdminMode', enabled ? 'true' : 'false');
            updateProfileUI();
            renderStoreMods(currentStoreFilter);
            showToast(enabled ? (currentLang === 'tr' ? 'Yönetici (Admin) Yetkisi Aktif Edildi!' : 'Admin Mode Enabled!') : (currentLang === 'tr' ? 'Normal Kullanıcı (Public) Moduna Geçildi.' : 'Switched to Public Mode.'));
        }

        function updateGranularTheme(type, val) {
            if(type === 'accent') {
                document.documentElement.style.setProperty('--accent-color', val);
                document.documentElement.style.setProperty('--accent-glow', val + '59');
                localStorage.setItem('themeAccent', val);
            } else if(type === 'bg') {
                document.documentElement.style.setProperty('--bg-main', val);
                localStorage.setItem('themeBg', val);
            } else if(type === 'card') {
                document.documentElement.style.setProperty('--bg-card', val);
                localStorage.setItem('themeCard', val);
            } else if(type === 'text') {
                document.documentElement.style.setProperty('--text-main', val);
                localStorage.setItem('themeText', val);
            } else if(type === 'btn') {
                document.documentElement.style.setProperty('--start-btn-bg', val);
                localStorage.setItem('themeBtn', val);
            }
        }

        async function loadSavedSettings() {
            const sAccent = localStorage.getItem('themeAccent');
            const sBg = localStorage.getItem('themeBg');
            const sCard = localStorage.getItem('themeCard');
            const sText = localStorage.getItem('themeText');
            const sBtn = localStorage.getItem('themeBtn');

            if(sAccent) {
                document.documentElement.style.setProperty('--accent-color', sAccent);
                document.documentElement.style.setProperty('--accent-glow', sAccent + '59');
                document.getElementById('accentColorPicker').value = sAccent;
            }
            if(sBg) {
                document.documentElement.style.setProperty('--bg-main', sBg);
                document.getElementById('bgColorPicker').value = sBg;
            }
            if(sCard) {
                document.documentElement.style.setProperty('--bg-card', sCard);
                document.getElementById('cardColorPicker').value = sCard;
            }
            if(sText) {
                document.documentElement.style.setProperty('--text-main', sText);
                document.getElementById('textColorPicker').value = sText;
            }
            if(sBtn) {
                document.documentElement.style.setProperty('--start-btn-bg', sBtn);
                document.getElementById('btnColorPicker').value = sBtn;
            }

            const customBg = localStorage.getItem('appBgUrl');
            if (customBg) {
                document.getElementById('mainAppBackground').src = customBg;
                document.getElementById('appBgUrlInput').value = customBg;
            }
            
            const btnBg = localStorage.getItem('startBtnBg');
            if (btnBg) {
                document.documentElement.style.setProperty('--start-btn-img', `url('${btnBg}')`);
                document.getElementById('masterStartBtn').style.backgroundImage = `linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.3)), url('${btnBg}')`;
                document.getElementById('startBtnBgInput').value = btnBg;
            }

            const isPerf = localStorage.getItem('performanceMode') === 'true';
            document.getElementById('performanceModeCheckbox').checked = isPerf;
            togglePerformanceMode(isPerf, false);

            const isAdmin = localStorage.getItem('isAdminMode') === 'true';
            const adminChk = document.getElementById('adminModeCheckbox');
            if (adminChk) adminChk.checked = isAdmin;

            let savedDbFolder = localStorage.getItem('skinsDbFolder');
            if (!savedDbFolder && window.electronAPI && window.electronAPI.autoDetectDbFolder) {
                savedDbFolder = await window.electronAPI.autoDetectDbFolder();
                if (savedDbFolder) localStorage.setItem('skinsDbFolder', savedDbFolder);
            }
            if (savedDbFolder && document.getElementById('currentDbPathDisplay')) {
                document.getElementById('currentDbPathDisplay').innerText = savedDbFolder;
            }

            const savedLolPath = localStorage.getItem('lolExePath');
            if (savedLolPath) {
                document.getElementById('currentLolPathDisplay').innerText = savedLolPath;
            }

            updateProfileUI();
        }

        function togglePerformanceMode(enabled, showMsg = true) {
            if (enabled) {
                document.body.classList.add('performance-mode');
                localStorage.setItem('performanceMode', 'true');
                if (showMsg) showToast('Performans Modu (FPS) aktif edildi!');
            } else {
                document.body.classList.remove('performance-mode');
                localStorage.setItem('performanceMode', 'false');
                if (showMsg) showToast('Performans Modu kapatıldı.');
            }
        }

        function updateProfileUI() {
            const pName = localStorage.getItem('profileName') || 'Oyuncu';
            const pAvatar = localStorage.getItem('profileAvatar') || 'https://i.postimg.co/y89X380H/shizuku-anime.png';
            const pBanner = localStorage.getItem('profileBanner') || 'https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Zed_1.jpg';

            document.getElementById('navProfileName').innerText = pName;
            document.getElementById('navProfileAvatar').src = pAvatar;
            document.getElementById('profilePageName').innerText = pName;
            document.getElementById('mainProfilePageAvatar').src = pAvatar;
            document.getElementById('mainProfilePageBanner').style.backgroundImage = `url('${pBanner}')`;

            const isUserAdmin = localStorage.getItem('isAdminMode') === 'true';
            const defaultRoleStr = isUserAdmin 
                ? (currentLang === 'tr' ? 'Skynix Koleksiyoneri & Tasarımcı' : 'Skynix Collector & Designer')
                : (currentLang === 'tr' ? 'Skynix Sihirdarı' : 'Skynix Summoner');

            const subEl = document.getElementById('txt-profile-sub');
            if (subEl) subEl.innerText = defaultRoleStr;

            const adminUploadBtn = document.getElementById('txt-admin-upload-btn');
            if (adminUploadBtn) {
                adminUploadBtn.style.display = isUserAdmin ? 'inline-flex' : 'none';
            }

            const timeStr = Math.floor(appUsageSeconds / 60) + ' dk';
            document.getElementById('timeSpentMinutesDisplay').innerText = timeStr;
            document.getElementById('totalCustomSkinsCount').innerText = customSkinsList.length;

            document.getElementById('homeTotalSkinsVal').innerText = customSkinsList.length;
            document.getElementById('homeActiveQueueVal').innerText = activeQueue.length;
            document.getElementById('homeTimeVal').innerText = timeStr;

            let topSkin = '-';
            let maxCount = 0;
            for(const [skin, count] of Object.entries(skinUsageCounts)) {
                if(count > maxCount) { maxCount = count; topSkin = skin; }
            }
            document.getElementById('topUsedSkinDisplay').innerText = topSkin;
        }

        function openProfileEditModal() {
            document.getElementById('editUsernameInput').value = localStorage.getItem('profileName') || 'Oyuncu';
            document.getElementById('editBannerUrlInput').value = localStorage.getItem('profileBanner') || '';
            document.getElementById('editAvatarUrlInput').value = localStorage.getItem('profileAvatar') || '';
            document.getElementById('profileEditModal').style.display = 'flex';
        }

        function closeProfileEditModal() {
            document.getElementById('profileEditModal').style.display = 'none';
        }

        function handleBannerFileUpload(e) {
            const file = e.target.files[0];
            if (file) {
                const reader = new FileReader();
                reader.onload = function(evt) {
                    tempBannerData = evt.target.result;
                    document.getElementById('editBannerUrlInput').value = tempBannerData;
                };
                reader.readAsDataURL(file);
            }
        }

        function handleAvatarFileUpload(e) {
            const file = e.target.files[0];
            if (file) {
                const reader = new FileReader();
                reader.onload = function(evt) {
                    tempAvatarData = evt.target.result;
                    document.getElementById('editAvatarUrlInput').value = tempAvatarData;
                };
                reader.readAsDataURL(file);
            }
        }

        function handleAdminImageUpload(e) {
            const file = e.target.files[0];
            if (file) {
                const reader = new FileReader();
                reader.onload = function(evt) {
                    document.getElementById('storeModImg').value = evt.target.result;
                };
                reader.readAsDataURL(file);
            }
        }

        function saveProfileChanges() {
            const newName = document.getElementById('editUsernameInput').value.trim() || 'Oyuncu';
            const newBanner = document.getElementById('editBannerUrlInput').value.trim() || 'https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Zed_1.jpg';
            const newAvatar = document.getElementById('editAvatarUrlInput').value.trim() || 'https://i.postimg.co/y89X380H/shizuku-anime.png';

            localStorage.setItem('profileName', newName);
            localStorage.setItem('profileBanner', newBanner);
            localStorage.setItem('profileAvatar', newAvatar);

            updateProfileUI();
            closeProfileEditModal();
            showToast('Profil başarıyla güncellendi!');
        }

        function switchTab(tabId, el) {
            document.querySelectorAll('.panel').forEach(p => p.classList.remove('active'));
            document.querySelectorAll('.nav-item').forEach(n => n.classList.remove('active'));

            const targetPanel = document.getElementById(tabId + '-panel');
            if (targetPanel) {
                targetPanel.classList.add('active');
            } else {
                console.warn("Hedef panel bulunamadı:", tabId + '-panel');
            }

            if (el) {
                el.classList.add('active');
            } else {
                const matchedNav = document.querySelector(`.nav-item[onclick*="${tabId}"]`);
                if (matchedNav) matchedNav.classList.add('active');
            }

            if (tabId === 'customSkins') renderCustomSkins();
            if (tabId === 'store') renderStoreMods('all');
            if (tabId === 'profile') updateProfileUI();
            if (tabId === 'home') updateProfileUI();

            // Discord Activity update
            if (window.electronAPI && window.electronAPI.updatePresence) {
                let stateStr = 'Ana Ekran';
                let detailsStr = 'Geziniyor';
                if (tabId === 'home') { stateStr = currentLang === 'tr' ? 'Ana Ekran' : 'Home Screen'; detailsStr = currentLang === 'tr' ? 'Geziniyor' : 'Browsing'; }
                else if (tabId === 'champions') { stateStr = currentLang === 'tr' ? 'Şampiyonlar' : 'Champions'; detailsStr = currentLang === 'tr' ? 'Kütüphaneyi inceliyor' : 'Browsing Library'; }
                else if (tabId === 'customSkins') { stateStr = currentLang === 'tr' ? 'Özel Kostümler' : 'Custom Skins'; detailsStr = currentLang === 'tr' ? 'Kostümleri yönetiyor' : 'Managing Skins'; }
                else if (tabId === 'store') { stateStr = currentLang === 'tr' ? 'Mod Mağazası' : 'Mod Store'; detailsStr = currentLang === 'tr' ? 'Mağazaya göz atıyor' : 'Browsing Store'; }
                else if (tabId === 'themes') { stateStr = currentLang === 'tr' ? 'Temalar' : 'Themes'; detailsStr = currentLang === 'tr' ? 'Temayı düzenliyor' : 'Customizing UI'; }
                else if (tabId === 'settings') { stateStr = currentLang === 'tr' ? 'Ayarlar' : 'Settings'; detailsStr = currentLang === 'tr' ? 'Ayarları düzenliyor' : 'Editing settings'; }
                else if (tabId === 'profile') { stateStr = currentLang === 'tr' ? 'Profil' : 'Profile'; detailsStr = currentLang === 'tr' ? 'Profilini inceliyor' : 'Viewing profile'; }

                window.electronAPI.updatePresence(stateStr, detailsStr);
            }
        }

        function handleWindowAction(action) {
            if (window.electronAPI && window.electronAPI.windowControl) {
                window.electronAPI.windowControl(action);
            } else {
                if (action === 'close') showToast('Kapatma tetiklendi (Electron bağlantısı bekleniyor)');
                else showToast(`Pencere eylemi: ${action}`);
            }
        }

        let isLauncherMinimized = false;
        function toggleLauncherMinimize() {
            const body = document.querySelector('#activeLauncherWidget .launcher-body');
            const footer = document.querySelector('#activeLauncherWidget .launcher-footer');
            isLauncherMinimized = !isLauncherMinimized;
            if (isLauncherMinimized) {
                body.style.display = 'none';
                footer.style.display = 'none';
            } else {
                body.style.display = 'flex';
                footer.style.display = 'block';
            }
        }

        function cleanSkinTitle(rawName) {
            if (!rawName) return "Özel Kostüm";
            let name = rawName;
            if (name.includes('/') || name.includes('\\')) {
                name = name.split(/[/\\]/).pop();
            }
            name = name.replace(/\.(zip|fantome|raw)$/i, '');
            name = name.replace(/_/g, ' ').trim();
            name = name.replace(/.*installed[/\\]/i, '');
            return name;
        }

        function parseSkinCardDetails(skin) {
            let cleanName = cleanSkinTitle(skin.title || skin.file || skin.path);
            let champName = skin.champ || 'Özel Mod';
            let authorName = 'By Herobrine';

            if (cleanName.toLowerCase().includes('by ')) {
                const parts = cleanName.split(/by /i);
                cleanName = parts[0].trim();
                authorName = 'By ' + parts.slice(1).join('by ').trim();
            }

            return {
                title: cleanName || 'Özel Kostüm',
                champ: champName,
                author: authorName,
                img: skin.img
            };
        }

        function openLaunchModal() {
            const grid = document.getElementById('launchModalCardsGrid');
            grid.innerHTML = '';

            activeQueue.forEach((item) => {
                const skinObj = customSkinsList.find(s => s.title === item.title) || item;
                const details = parseSkinCardDetails(skinObj);

                grid.innerHTML += `
                    <div class="launch-skin-card">
                        <img src="${details.img || 'https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Yasuo_0.jpg'}" alt="${details.title}">
                        <div class="launch-skin-card-overlay">
                            <span style="font-size:10px; font-weight:800; color:var(--accent-color); text-transform:uppercase;">${details.champ}</span>
                            <span style="font-size:14px; font-weight:800; color:#fff; word-break:break-word;">${details.title}</span>
                            <span style="font-size:11px; font-weight:600; color:var(--text-muted);">${details.author}</span>
                        </div>
                    </div>
                `;
            });

            document.getElementById('launchModalStatusText').innerText = currentLang === 'tr' ? 'CSLoL Motoru Oyuna Bağlanıyor...' : 'CSLoL Engine Connecting...';
            document.getElementById('launchProgressMsg').innerText = currentLang === 'tr' ? 'Mod paketleri oyuna enjekte ediliyor...' : 'Injecting mod packages into game...';
            document.getElementById('launchProgressBar').style.width = '10%';
            document.getElementById('launchProgressPercent').innerText = '10%';
            document.getElementById('activeLaunchModal').style.display = 'flex';
        }

        function closeLaunchModal() {
            document.getElementById('activeLaunchModal').style.display = 'none';
        }

        async function addNewSkinFile() {
            if (window.electronAPI && window.electronAPI.selectSkinFile) {
                const filePath = await window.electronAPI.selectSkinFile();
                if (filePath) {
                    const fileName = filePath.split(/[/\\]/).pop();
                    const cleanTitle = cleanSkinTitle(fileName);
                    const matchedData = await detectSkinInfoAndSplash(fileName);

                    const newSkin = {
                        id: Date.now() + Math.random(),
                        title: cleanTitle,
                        champ: matchedData.champ,
                        img: matchedData.img,
                        path: filePath,
                        file: fileName
                    };

                    const existingIdx = customSkinsList.findIndex(s => s.title === cleanTitle || s.path === filePath);
                    if (existingIdx > -1) {
                        customSkinsList[existingIdx] = newSkin;
                    } else {
                        customSkinsList.push(newSkin);
                    }

                    localStorage.setItem('customSkinsList', JSON.stringify(customSkinsList));
                    renderCustomSkins();
                    updateProfileUI();
                    const msg = currentLang === 'tr' ? `'${cleanTitle}' installed/ klasörüne kaydedildi!` : `'${cleanTitle}' saved to installed/ folder!`;
                    showToast(msg);
                }
            } else {
                document.getElementById('directSkinFileInput').click();
            }
        }

        async function selectSkinsDbFolder() {
            if (window.electronAPI && window.electronAPI.selectDbFolder) {
                const folder = await window.electronAPI.selectDbFolder();
                if (folder) {
                    localStorage.setItem('skinsDbFolder', folder);
                    if (document.getElementById('currentDbPathDisplay')) {
                        document.getElementById('currentDbPathDisplay').innerText = folder;
                    }
                    showToast('Skin veritabanı klasörü (Skynix Data base Skins) kaydedildi!');
                }
            }
        }

        async function autoDetectSkinsDbFolder() {
            if (window.electronAPI && window.electronAPI.autoDetectDbFolder) {
                const folder = await window.electronAPI.autoDetectDbFolder();
                if (folder) {
                    localStorage.setItem('skinsDbFolder', folder);
                    if (document.getElementById('currentDbPathDisplay')) {
                        document.getElementById('currentDbPathDisplay').innerText = folder;
                    }
                    showToast('Skynix Data base Skins klasörü otomatik tespit edildi!');
                } else {
                    showToast('Veritabanı klasörü otomatik bulunamadı. Lütfen "Klasör Seç" ile manuel belirtin.');
                }
            }
        }

        async function injectActiveMods() {
            if (activeQueue.length === 0) {
                showToast(currentLang === 'tr' ? 'Lütfen önce bir mod veya skin seçin!' : 'Please select a mod or skin first!');
                return;
            }

            let lolPath = localStorage.getItem('lolExePath');
            if (!lolPath) {
                showToast(currentLang === 'tr' ? 'LeagueClient.exe yolu taranıyor...' : 'Scanning LeagueClient.exe path...');
                if (window.electronAPI && window.electronAPI.autoDetectLol) {
                    lolPath = await window.electronAPI.autoDetectLol();
                }
                if (!lolPath) lolPath = 'C:\\Riot Games\\League of Legends\\LeagueClient.exe';
                localStorage.setItem('lolExePath', lolPath);
                document.getElementById('currentLolPathDisplay').innerText = lolPath;
            }

            openLaunchModal();

            let successCount = 0;
            let errorCount = 0;
            const total = activeQueue.length;

            // Yüklü modları tara
            let diskSkins = [];
            if (window.electronAPI && window.electronAPI.scanInstalledSkins) {
                diskSkins = await window.electronAPI.scanInstalledSkins();
            }

            let skinsDbFolder = localStorage.getItem('skinsDbFolder');
            if (!skinsDbFolder && window.electronAPI && window.electronAPI.autoDetectDbFolder) {
                skinsDbFolder = await window.electronAPI.autoDetectDbFolder();
                if (skinsDbFolder) localStorage.setItem('skinsDbFolder', skinsDbFolder);
            }

            for (let i = 0; i < activeQueue.length; i++) {
                const item = activeQueue[i];
                const cleanItemTitle = item.title.toLowerCase().trim();

                // 1) customSkinsList içinde eşleşme ara
                let skinData = customSkinsList.find(s => {
                    if (!s) return false;
                    const st = (s.title || '').toLowerCase();
                    return st === cleanItemTitle || cleanItemTitle.includes(st) || st.includes(cleanItemTitle);
                });
                let selectedPath = skinData ? skinData.path : null;

                // 2) Skynix Data base Skins içinde otomatik ara (main.js kendi bulur)
                if (!selectedPath && window.electronAPI && window.electronAPI.findDbSkinFile) {
                    selectedPath = await window.electronAPI.findDbSkinFile({
                        champKey: item.champKey,
                        champId: item.champId,
                        skinNum: item.skinNum,
                        skinName: item.title
                    });
                }

                // 3) Eğer yoksa diskteki installed/ dosyaları arasında akıllı arama yap
                if (!selectedPath && diskSkins.length > 0) {
                    const words = cleanItemTitle.split(/\s+/).filter(w => w.length > 2);
                    const matchedDisk = diskSkins.find(d => {
                        const df = d.file.toLowerCase();
                        return df.includes(cleanItemTitle) || words.some(w => df.includes(w));
                    });
                    if (matchedDisk) {
                        selectedPath = matchedDisk.path;
                    }
                }

                const percent = Math.round(((i + 1) / total) * 90);
                document.getElementById('launchProgressBar').style.width = percent + '%';
                document.getElementById('launchProgressPercent').innerText = percent + '%';
                document.getElementById('launchProgressMsg').innerText = currentLang === 'tr' ? `'${item.title}' oyuna enjekte ediliyor...` : `Injecting '${item.title}' into game...`;

                // 4) Bulunamadıysa hata sayısını artır ve devam et (ASLA DOSYA PENCERESİ AÇMA)
                if (!selectedPath) {
                    errorCount++;
                    console.warn(`[LAUNCH] '${item.title}' için veritabanında veya installed klasöründe dosya bulunamadı.`);
                    showToast(`'${item.title}' için dosya bulunamadı.`);
                    continue;
                }

                if (!selectedPath) {
                    errorCount++;
                    continue;
                }

                try {
                    const result = await window.electronAPI.runCslolSkin({
                        skinPath: selectedPath,
                        lolExePath: lolPath
                    });

                    if (!result.success) {
                        showToast(currentLang === 'tr' ? `Başarısız (${item.title}): ${result.message}` : `Failed (${item.title}): ${result.message}`);
                        errorCount++;
                    } else {
                        successCount++;
                        skinUsageCounts[item.title] = (skinUsageCounts[item.title] || 0) + 1;
                    }
                } catch (err) {
                    showToast(currentLang === 'tr' ? `Sistem Hatası: Motorla iletişim kurulamadı.` : `System Error: Unable to communicate with engine.`);
                    errorCount++;
                }
            }

            localStorage.setItem('skinUsageCounts', JSON.stringify(skinUsageCounts));
            updateProfileUI();

            document.getElementById('launchProgressBar').style.width = '100%';
            document.getElementById('launchProgressPercent').innerText = '100%';

            if (successCount > 0 && errorCount === 0) {
                // Başarılı enjeksiyon: Butonu SKİNLERİ DURDUR'a çevir
                skinsActive = true;
                const btn = document.getElementById('masterStartBtn');
                btn.classList.add('stop-mode');
                btn.onclick = stopActiveMods;
                btn.innerHTML = `<svg class="icon-svg" viewBox="0 0 24 24"><path d="M6 6h12v12H6z"/></svg><span id="txt-start-btn">${currentLang === 'tr' ? 'SKİNLERİ DURDUR' : 'STOP SKINS'}</span>`;
                renderActiveLauncherWidget();

                document.getElementById('launchModalStatusText').innerText = currentLang === 'tr' ? '[BAŞARILI] Tüm modlar oyuna enjekte edildi!' : '[SUCCESS] All mods injected into game!';
                document.getElementById('launchProgressMsg').innerText = currentLang === 'tr' ? 'Tamamlandı! Oyuna sorunsuz girebilirsin.' : 'Completed! You can now join the game.';
                showToast(currentLang === 'tr' ? 'Tüm modlar eksiksiz ve sorunsuz tamamlandı!' : 'All mods injected successfully!');

                if (window.electronAPI && window.electronAPI.updatePresence) {
                    const count = activeQueue.length;
                    const firstSkin = activeQueue[0] ? activeQueue[0].title : '';
                    const skinSummary = count === 1 ? firstSkin : (count > 1 ? `${firstSkin} (+${count - 1} mod)` : '');
                    
                    const stateStr = currentLang === 'tr' ? `🎮 Oyunda (${count} Kostüm Aktif)` : `🎮 In Game (${count} Skins Active)`;
                    const detailsStr = skinSummary || (currentLang === 'tr' ? 'Özel Kostümler Çalışıyor' : 'Custom Skins Running');
                    window.electronAPI.updatePresence(stateStr, detailsStr);
                }
            } else if (errorCount > 0) {
                skinsActive = false;
                document.getElementById('launchModalStatusText').innerText = currentLang === 'tr' ? '[UYARI] Bazı modlarda hata oluştu!' : '[WARNING] Some mods failed!';
            }
        }

        async function stopActiveMods() {
            if (window.electronAPI && window.electronAPI.stopCslolSkin) {
                await window.electronAPI.stopCslolSkin();
            }
            skinsActive = false;
            const btn = document.getElementById('masterStartBtn');
            btn.classList.remove('stop-mode');
            btn.onclick = injectActiveMods;
            btn.innerHTML = `<svg class="icon-svg" viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg><span id="txt-start-btn">${currentLang === 'tr' ? 'SKİNLERİ BAŞLAT' : 'LAUNCH SKINS'}</span>`;
            renderActiveLauncherWidget();
            showToast(currentLang === 'tr' ? 'Skinler durduruldu.' : 'Skins stopped.');

            if (window.electronAPI && window.electronAPI.updatePresence) {
                window.electronAPI.updatePresence(currentLang === 'tr' ? 'Ana Ekran' : 'Home Screen', currentLang === 'tr' ? 'Boşta' : 'Idle');
            }
        }

        function toggleSkinQueue(title, img, champKey = null, skinNum = null, champId = null) {
            const idx = activeQueue.findIndex(x => x.title === title);
            if (idx > -1) {
                activeQueue.splice(idx, 1);
                showToast(`${title} kuyruktan çıkarıldı.`);
            } else {
                activeQueue.push({ title, img, champKey, skinNum, champId });
                showToast(`${title} kuyruğa eklendi!`);
            }
            renderActiveLauncherWidget();
            renderCustomSkins();
            updateProfileUI();
        }

        function renderActiveLauncherWidget() {
            const list = document.getElementById('activeLauncherList');
            const titleEl = document.getElementById('txt-queue-title');
            const dict = dictionary[currentLang];

            if (activeQueue.length === 0) {
                titleEl.innerText = `${dict.queueTitle}`;
                list.innerHTML = `<div style="font-size:12px; color:var(--text-muted); text-align:center; padding:10px;" id="txt-queue-empty">${dict.queueEmpty}</div>`;
                return;
            }

            titleEl.innerText = `${dict.queueTitle} (${activeQueue.length})`;
            list.innerHTML = '';
            activeQueue.forEach((item) => {
                const details = parseSkinCardDetails(customSkinsList.find(s => s.title === item.title) || item);
                const rightSide = skinsActive
                    ? `<span class="active-status-dot-pulse" title="Skin aktif - oyunda çalışıyor"></span>`
                    : `<button onclick="toggleSkinQueue('${item.title.replace(/'/g, "\\'")}', '${item.img}')" style="background:none; border:none; color:#ef4444; font-weight:bold; cursor:pointer;">✕</button>`;
                
                list.innerHTML += `
                    <div class="active-skin-row">
                        <div style="display:flex; align-items:center; gap:8px;">
                            <img src="${details.img || item.img}" style="width:32px; height:32px; border-radius:6px; object-fit:cover;">
                            <div style="display:flex; flex-direction:column;">
                                <span style="font-size:10px; font-weight:800; color:var(--accent-color); text-transform:uppercase;">${details.champ || ''}</span>
                                <span style="font-size:12px; font-weight:700;">${details.title || item.title}</span>
                            </div>
                        </div>
                        ${rightSide}
                    </div>
                `;
            });
        }

        async function fetchChampions() {
            try {
                const vRes = await fetch('https://ddragon.leagueoflegends.com/api/versions.json');
                const vData = await vRes.json();
                latestLoLVersion = vData[0] || "14.1.1";

                const cRes = await fetch(`https://ddragon.leagueoflegends.com/cdn/${latestLoLVersion}/data/${currentLang === 'tr' ? 'tr_TR' : 'en_US'}/champion.json`);
                const cData = await cRes.json();
                allChampions = cData.data;

                renderChampionGrid(Object.values(allChampions));
            } catch (e) {
                console.error("Data Dragon Yükleme Hatası:", e);
                showToast("Şampiyon verileri yüklenirken bir hata oluştu.");
            }
        }
        
        function toggleArtMode() {
            useLoadingArt = !useLoadingArt;
            applyLanguage(currentLang);
            const activeChamp = document.getElementById('selectedChampTitleName').innerText;
            if (activeChamp && activeChamp.includes('-')) {
                const champName = activeChamp.split('-')[0].trim();
                const found = Object.values(allChampions).find(c => c.name === champName);
                if (found) loadChampionSkins(found.id);
            } else {
                renderChampionGrid(Object.values(allChampions));
            }
        }

        function renderChampionGrid(champs) {
            const grid = document.getElementById('championGrid');
            grid.style.display = 'grid';
            document.getElementById('skinViewContainer').style.display = 'none';
            grid.innerHTML = '';

            champs.forEach(c => {
                if (hiddenChampions.includes(c.id)) return;

                const splashImg = `https://ddragon.leagueoflegends.com/cdn/img/champion/splash/${c.id}_0.jpg`;
                const loadingImg = `https://ddragon.leagueoflegends.com/cdn/img/champion/loading/${c.id}_0.jpg`;
                const cardImg = useLoadingArt ? loadingImg : splashImg;

                grid.innerHTML += `
                    <div class="champion-card" onclick="loadChampionSkins('${c.id}')">
                        <img src="${cardImg}" alt="${c.name}" onerror="this.src='${splashImg}';">
                        <div class="champion-info">
                            <div class="champion-name">${c.name}</div>
                            <div class="champion-title">${c.title}</div>
                        </div>
                    </div>
                `;
            });
        }

        function filterChampions() {
            const q = document.getElementById('championSearch').value.toLowerCase();
            const filtered = Object.values(allChampions).filter(c => 
                c.name.toLowerCase().includes(q) || c.id.toLowerCase().includes(q)
            );
            renderChampionGrid(filtered);
        }

        async function loadChampionSkins(champId) {
            try {
                const res = await fetch(`https://ddragon.leagueoflegends.com/cdn/${latestLoLVersion}/data/${currentLang === 'tr' ? 'tr_TR' : 'en_US'}/champion/${champId}.json`);
                const data = await res.json();
                const champData = data.data[champId];

                document.getElementById('championGrid').style.display = 'none';
                const container = document.getElementById('skinViewContainer');
                container.style.display = 'block';

                document.getElementById('selectedChampTitleName').innerText = `${champData.name} - Kostümler`;
                const skinGrid = document.getElementById('skinGrid');
                skinGrid.innerHTML = '';

                champData.skins.forEach(s => {
                    const lowerSkinName = s.name.toLowerCase();

                    if (s.name.includes('(') && s.name.includes(')')) return;
                    if (lowerSkinName.includes('traditional') || lowerSkinName.includes('legacy') || lowerSkinName.includes('eski')) return;

                    const skinName = s.name === 'default' ? champData.name : s.name;
                    const splashImg = `https://ddragon.leagueoflegends.com/cdn/img/champion/splash/${champId}_${s.num}.jpg`;
                    const loadingImg = `https://ddragon.leagueoflegends.com/cdn/img/champion/loading/${champId}_${s.num}.jpg`;
                    const cardImg = useLoadingArt ? loadingImg : splashImg;

                    let chromaBtnHTML = '';
                    if (s.num > 0) {
                        chromaBtnHTML = `<div class="rgb-chroma-btn" onclick="event.stopPropagation(); openChromaModal('${champData.key}', ${s.num}, '${skinName.replace(/'/g, "\\'")}', '${splashImg}')"></div>`;
                    }

                    skinGrid.innerHTML += `
                        <div class="champion-card" onclick="toggleSkinQueue('${skinName.replace(/'/g, "\\'")}', '${splashImg}', '${champData.key}', ${s.num}, '${champId}')">
                            ${chromaBtnHTML}
                            <img src="${cardImg}" alt="${skinName}" onerror="this.closest('.champion-card').remove();">
                            <div class="champion-info">
                                <div class="champion-name">${skinName}</div>
                                <div class="champion-title" style="color:var(--accent-color);">+ Seç / Kaldır</div>
                            </div>
                        </div>
                    `;
                });
            } catch (e) {
                console.error("Skin Yükleme Hatası:", e);
            }
        }

        // YENİ NESİL DEVASA SPLASH ART DESTEKLİ CHROMA SEÇİCİ
        function cDragonAssetUrl(path) {
            if (!path) return '';
            // CommunityDragon path'leri küçük harfe çevrilmiş olarak tutulur
            // /lol-game-data/assets/ → CDragon base
            return path.replace('/lol-game-data/assets/', 'https://raw.communitydragon.org/latest/plugins/rcp-be-lol-game-data/global/default/').toLowerCase();
        }

        async function openChromaModal(champNumericId, skinNum, skinName, baseImgUrl) {
            activeChromaSkinTitle = skinName;
            
            document.getElementById('chromaHeroBg').src = baseImgUrl;
            document.getElementById('chromaHeroImg').src = baseImgUrl;
            document.getElementById('chromaModalTitle').innerText = skinName;
            
            const grid = document.getElementById('chromaThumbnailsGrid');
            const loadingText = document.getElementById('chromaLoadingText');
            
            grid.innerHTML = '';
            loadingText.style.display = 'block'; 
            document.getElementById('chromaModal').style.display = 'flex';

            try {
                const res = await fetch(`https://raw.communitydragon.org/latest/plugins/rcp-be-lol-game-data/global/default/v1/champions/${champNumericId}.json`);
                if (!res.ok) throw new Error(`HTTP ${res.status}`);
                const data = await res.json();

                // Skin'i bul: skinNum tam ID'nin son 3 hanesidir (s.id % 1000)
                const skinData = data.skins.find(s => s.id % 1000 === skinNum || s.name === skinName);

                loadingText.style.display = 'none';

                // Hero splash'ı CDragon'dan güncelle (daha yüksek kaliteli)
                if (skinData && skinData.uncenteredSplashPath) {
                    const heroUrl = cDragonAssetUrl(skinData.uncenteredSplashPath);
                    document.getElementById('chromaHeroBg').src = heroUrl;
                    document.getElementById('chromaHeroImg').src = heroUrl;
                } else if (skinData && skinData.splashPath) {
                    const heroUrl = cDragonAssetUrl(skinData.splashPath);
                    document.getElementById('chromaHeroBg').src = heroUrl;
                }

                if (skinData && skinData.chromas && skinData.chromas.length > 0) {
                    skinData.chromas.forEach(chroma => {
                        // CDragon chroma resim URL'si — ID bazlı, küçük harfe çevrilmiş path
                        const chromaImgUrl = cDragonAssetUrl(chroma.chromaPath || chroma.tilePath);
                        
                        // Renk swatch'ları oluştur
                        const colorSwatches = (chroma.colors || []).slice(0, 2).map(c =>
                            `<span style="display:inline-block; width:10px; height:10px; border-radius:50%; background:${c}; border:1px solid rgba(255,255,255,0.3); flex-shrink:0;"></span>`
                        ).join('');

                        // Kısa isim: parantez içindekini al → "Sapphire", "Ruby" etc.
                        const shortName = (chroma.name.match(/\(([^)]+)\)/) || [, chroma.name])[1];

                        const fullTitle = `${skinName} (${shortName})`;
                        const escapedTitle = fullTitle.replace(/'/g, "\\'");
                        const escapedImgUrl = chromaImgUrl.replace(/'/g, "\\'");

                        grid.innerHTML += `
                            <div class="chroma-thumb-card" onclick="addChromaToQueue('${escapedTitle}', this.querySelector('.thumb-img').src)">
                                <img class="thumb-img" 
                                    src="${chromaImgUrl}" 
                                    onerror="this.onerror=null; this.src='${baseImgUrl}';"
                                    loading="lazy">
                                <div class="chroma-add-badge">+</div>
                                <div class="chroma-thumb-name">
                                    <span style="display:flex; align-items:center; gap:4px; justify-content:center; flex-wrap:wrap;">
                                        ${colorSwatches}
                                        ${shortName}
                                    </span>
                                </div>
                            </div>
                        `;
                    });
                } else {
                    grid.innerHTML = `<div style="color:#fff; font-weight:600; padding:20px; text-align:center; opacity:0.6;">Bu kostüm için chroma bulunamadı.</div>`;
                }

            } catch (error) {
                console.error("Chroma API Hatası:", error);
                loadingText.style.display = 'none';
                grid.innerHTML = `<div style="color:#ef4444; font-weight:600; padding:20px; text-align:center;">Veriler çekilirken hata oluştu.<br><small>${error.message}</small></div>`;
            }
        }


        function closeChromaModal() {
            document.getElementById('chromaModal').style.display = 'none';
        }

        function addChromaToQueue(fullTitle, imgUrl) {
            toggleSkinQueue(fullTitle, imgUrl);
        }

        function backToChampionsGrid() {
            document.getElementById('championGrid').style.display = 'grid';
            document.getElementById('skinViewContainer').style.display = 'none';
        }

        async function detectSkinInfoAndSplash(fileName) {
            const cleanName = fileName.replace(/\.[^/.]+$/, "").replace(/[_]/g, " ").replace(/-/g, " ");
            const lower = cleanName.toLowerCase();

            let matchedChampId = null;
            let matchedChampName = "Özel Mod";

            const champList = Object.values(allChampions);
            for (const c of champList) {
                const cNameLower = c.name.toLowerCase();
                const cIdLower = c.id.toLowerCase();
                if (lower.includes(cNameLower) || lower.includes(cIdLower)) {
                    matchedChampId = c.id;
                    matchedChampName = c.name;
                    break;
                }
            }

            if (matchedChampId) {
                try {
                    const res = await fetch(`https://ddragon.leagueoflegends.com/cdn/${latestLoLVersion}/data/${currentLang === 'tr' ? 'tr_TR' : 'en_US'}/champion/${matchedChampId}.json`);
                    const data = await res.json();
                    const skins = data.data[matchedChampId].skins;

                    let matchedSkinNum = 0;
                    for (const s of skins) {
                        const sNameLower = s.name.toLowerCase();
                        if (sNameLower !== 'default' && (lower.includes(sNameLower) || sNameLower.split(' ').some(w => w.length > 3 && lower.includes(w)))) {
                            matchedSkinNum = s.num;
                            break;
                        }
                    }

                    const splashUrl = `https://ddragon.leagueoflegends.com/cdn/img/champion/splash/${matchedChampId}_${matchedSkinNum}.jpg`;
                    return { title: cleanName, champ: matchedChampName, img: splashUrl };
                } catch (e) {
                    console.error("Skin Eşleme Hatası:", e);
                }
            }

            return {
                title: cleanName,
                champ: matchedChampName,
                img: `https://ddragon.leagueoflegends.com/cdn/img/champion/splash/${matchedChampId || 'Akali'}_0.jpg`
            };
        }

        async function handleDirectSkinFileUpload(e) {
            const files = Array.from(e.target.files);
            if (!files.length) return;

            let addedCount = 0;
            for (const file of files) {
                const ext = file.name.split('.').pop().toLowerCase();
                if (ext === 'zip' || ext === 'fantome') {
                    let finalPath = file.path;
                    if (window.electronAPI && window.electronAPI.copyToInstalled && file.path) {
                        const copied = await window.electronAPI.copyToInstalled(file.path);
                        if (copied) finalPath = copied;
                    }
                    const matchedData = await detectSkinInfoAndSplash(file.name);
                    customSkinsList.push({
                        id: Date.now() + Math.random(),
                        title: matchedData.title,
                        champ: matchedData.champ,
                        img: matchedData.img,
                        path: finalPath,
                        file: file.name
                    });
                    addedCount++;
                }
            }

            if (addedCount > 0) {
                localStorage.setItem('customSkinsList', JSON.stringify(customSkinsList));
                renderCustomSkins();
                updateProfileUI();
                const msg = currentLang === 'tr' ? `${addedCount} adet özel skin installed/ klasörüne kaydedildi!` : `${addedCount} skin(s) saved to installed/ folder!`;
                showToast(msg);
            } else {
                const errMsg = currentLang === 'tr' ? 'Lütfen sadece .zip veya .fantome uzantılı dosya seçin!' : 'Please select only .zip or .fantome files!';
                showToast(errMsg);
            }
            e.target.value = '';
        }

        function renderCustomSkins() {
            const grid = document.getElementById('customSkinGrid');
            const searchVal = (document.getElementById('customSkinSearch')?.value || '').toLowerCase();
            const dict = dictionary[currentLang];
            grid.innerHTML = '';
            
            let list = customSkinsList;
            if (searchVal) {
                list = list.filter(s => (s.title || '').toLowerCase().includes(searchVal) || (s.champ || '').toLowerCase().includes(searchVal));
            }

            if (list.length === 0) {
                grid.innerHTML = `<div style="grid-column: 1/-1; text-align:center; padding:40px; color:var(--text-muted);">${dict.emptyCustomSkins}</div>`;
                return;
            }

            list.forEach((skin, idx) => {
                const details = parseSkinCardDetails(skin);
                const isQueued = activeQueue.some(x => x.title === (skin.title || details.title));
                grid.innerHTML += `
                    <div class="custom-card-frame" style="cursor:pointer;" onclick="toggleSkinQueue('${(skin.title || details.title).replace(/'/g, "\\'")}', '${details.img}')">
                        <div class="three-dots-btn" onclick="toggleDropdownMenu(event, ${idx})">⋮</div>
                        <div class="card-menu-dropdown" id="dropdown-${idx}">
                            <div class="dropdown-item" onclick="event.stopPropagation(); openEditSkinModal(${idx})">${dict.btnEdit}</div>
                            <div class="dropdown-item danger" onclick="event.stopPropagation(); deleteCustomSkin(${idx})">${dict.btnDelete}</div>
                        </div>

                        <div class="custom-card-banner" style="background-image: url('${details.img || 'https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Yasuo_0.jpg'}');">
                            <span class="custom-card-badge">${dict.modFileBadge}</span>
                        </div>
                        <div class="custom-card-body">
                            <div class="custom-skin-champ">${details.champ}</div>
                            <div class="custom-skin-title">${details.title}</div>
                            <div style="font-size:11px; color:var(--text-muted); font-weight:600; margin-top:-2px;">${details.author}</div>
                            
                            <button class="btn-primary" style="margin-top:10px; width:100%; justify-content:center; ${isQueued ? 'background:#ef4444; color:#fff;' : ''}">
                                ${isQueued ? (currentLang === 'tr' ? '✕ Kuyruktan Çıkar' : '✕ Remove Queue') : (currentLang === 'tr' ? '➕ Kuyruğa Ekle' : '➕ Add to Queue')}
                            </button>
                        </div>
                    </div>
                `;
            });
        }

        function toggleDropdownMenu(e, idx) {
            e.stopPropagation();
            document.querySelectorAll('.card-menu-dropdown').forEach((d, i) => {
                if (i !== idx) d.classList.remove('show');
            });
            const target = document.getElementById(`dropdown-${idx}`);
            if (target) target.classList.toggle('show');
        }

        document.addEventListener('click', () => {
            document.querySelectorAll('.card-menu-dropdown').forEach(d => d.classList.remove('show'));
        });

        function openEditSkinModal(idx) {
            activeEditingSkinIndex = idx;
            const item = customSkinsList[idx];
            document.getElementById('editSkinItemNameInput').value = item.title;
            document.getElementById('editSkinItemImgInput').value = item.img;
            tempEditSkinImgData = item.img;
            document.getElementById('editSkinItemModal').style.display = 'flex';
        }

        function closeEditSkinModal() {
            document.getElementById('editSkinItemModal').style.display = 'none';
        }

        function handleEditSkinImageUpload(e) {
            const file = e.target.files[0];
            if (file) {
                const reader = new FileReader();
                reader.onload = function(evt) {
                    tempEditSkinImgData = evt.target.result;
                    document.getElementById('editSkinItemImgInput').value = "Yerel Dosya Yüklendi (" + file.name + ")";
                };
                reader.readAsDataURL(file);
            }
        }

        function saveSkinItemEdit() {
            if (activeEditingSkinIndex < 0) return;
            const newName = document.getElementById('editSkinItemNameInput').value.trim();
            const inputImgVal = document.getElementById('editSkinItemImgInput').value.trim();

            if (newName) customSkinsList[activeEditingSkinIndex].title = newName;
            if (inputImgVal && !inputImgVal.startsWith("Yerel Dosya")) {
                customSkinsList[activeEditingSkinIndex].img = inputImgVal;
            } else if (tempEditSkinImgData) {
                customSkinsList[activeEditingSkinIndex].img = tempEditSkinImgData;
            }

            localStorage.setItem('customSkinsList', JSON.stringify(customSkinsList));
            closeEditSkinModal();
            renderCustomSkins();
            showToast('Skin başarıyla güncellendi!');
        }

        async function deleteCustomSkin(idx) {
            const item = customSkinsList[idx];
            if (item && item.path) {
                if (window.electronAPI && window.electronAPI.deleteInstalledSkin) {
                    await window.electronAPI.deleteInstalledSkin(item.path);
                }
            }
            customSkinsList.splice(idx, 1);
            localStorage.setItem('customSkinsList', JSON.stringify(customSkinsList));
            renderCustomSkins();
            updateProfileUI();
            showToast('Skin ve dosyası bilgisayardan başarıyla silindi.');
        }

        function renderStoreMods(filterCategory = 'all') {
            currentStoreFilter = filterCategory;
            const grid = document.getElementById('storeGrid');
            if (!grid) return;
            const searchVal = (document.getElementById('storeSearch')?.value || '').toLowerCase();
            const dict = dictionary[currentLang];
            grid.innerHTML = '';

            let list = Array.isArray(storeModsList) ? storeModsList : [];
            
            // Güvenli kopyalama ve varsayılan alan atamaları
            list = list.map(m => ({
                id: m.id || m.title,
                title: m.title || 'Özel Mod',
                champ: m.champ || 'Şampiyon',
                category: (m.category || 'champion').toLowerCase(),
                priceType: (m.priceType || 'free').toLowerCase(),
                img: m.img || 'https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Yasuo_0.jpg',
                downloadUrl: m.downloadUrl || '',
                description: m.description || ''
            }));

            if (filterCategory === 'free') list = list.filter(m => m.priceType === 'free');
            else if (filterCategory === 'paid') list = list.filter(m => m.priceType === 'paid');
            else if (filterCategory !== 'all') list = list.filter(m => m.category === filterCategory || (filterCategory === 'champion' && !m.category));

            if (searchVal) {
                list = list.filter(m => m.title.toLowerCase().includes(searchVal) || m.champ.toLowerCase().includes(searchVal));
            }

            if (list.length === 0) {
                grid.innerHTML = `<div style="grid-column: 1/-1; text-align:center; padding:40px; color:var(--text-muted); font-weight:600;">Mağazada henüz gösterilecek mod bulunamadı.</div>`;
                return;
            }

            list.forEach((m, idx) => {
                const catLabel = (m.category || 'mod').toUpperCase();
                const priceLabel = m.priceType === 'paid' ? (dict.badgePaid || 'ÜCRETLİ') : (dict.badgeFree || 'ÜCRETSİZ');
                const isDownloaded = customSkinsList.some(s => s.title === m.title);

                grid.innerHTML += `
                    <div class="custom-card-frame" style="position:relative;">
                        <button onclick="event.stopPropagation(); deleteStoreMod(${idx})" style="position:absolute; top:8px; right:8px; z-index:10; background:rgba(239,68,68,0.85); color:#fff; border:none; border-radius:8px; width:28px; height:28px; font-weight:bold; cursor:pointer; display:flex; align-items:center; justify-content:center; backdrop-filter:blur(4px); transition:0.2s;" title="Modu Mağazadan Sil">✕</button>

                        <div class="custom-card-banner" style="background-image: url('${m.img}');">
                            <span class="custom-card-badge">${catLabel}</span>
                            <span class="price-badge ${m.priceType === 'paid' ? 'paid' : ''}">${priceLabel}</span>
                        </div>
                        <div class="custom-card-body">
                            <div class="custom-skin-title">${m.title}</div>
                            <div style="font-size:11px; color:var(--accent-color); font-weight:700; margin-top:2px;">${m.champ}</div>
                            <button class="btn-primary" style="margin-top:8px; width:100%; justify-content:center; ${isDownloaded ? 'background:#22c55e;' : ''}" onclick="downloadStoreMod('${m.title.replace(/'/g, "\\'")}', '${m.img}', '${(m.downloadUrl || '').replace(/'/g, "\\'")}')">
                                ${isDownloaded ? '✓ Yüklendi' : (dict.btnDownloadAdd || '📥 İndir & Ekle')}
                            </button>
                        </div>
                    </div>
                `;
            });
        }

        function deleteStoreMod(index) {
            if (confirm('Bu modu mağaza listenizden silmek istediğinize emin misiniz?')) {
                storeModsList.splice(index, 1);
                localStorage.setItem('storeModsList', JSON.stringify(storeModsList));
                renderStoreMods(currentStoreFilter);
                showToast('Mod mağazadan silindi.');
            }
        }

        function filterStore(cat, el) {
            document.querySelectorAll('.filter-chip').forEach(c => c.classList.remove('active'));
            if (el) el.classList.add('active');
            renderStoreMods(cat);
        }

        async function downloadStoreMod(title, img, downloadUrl) {
            const exists = customSkinsList.some(s => s.title === title);
            if (exists) {
                showToast(currentLang === 'tr' ? 'Bu mod zaten Özel Skinlerinizde mevcut!' : 'This mod is already in your Custom Skins!');
                return;
            }

            showToast(currentLang === 'tr' ? `Mod indiriliyor: ${title}...` : `Downloading mod: ${title}...`);

            let savedPath = null;
            if (window.electronAPI && window.electronAPI.downloadStoreModFile && downloadUrl) {
                savedPath = await window.electronAPI.downloadStoreModFile({ downloadUrl, title });
            }

            customSkinsList.push({
                id: Date.now(),
                title: title,
                champ: 'Store Mod',
                img: img,
                path: savedPath || '',
                file: `${title}.fantome`,
                downloadUrl: downloadUrl || ''
            });

            localStorage.setItem('customSkinsList', JSON.stringify(customSkinsList));
            showToast(currentLang === 'tr' ? `${title} başarıyla indirildi ve Özel Skinlerim'e eklendi!` : `${title} downloaded and added to Custom Skins!`);
            renderCustomSkins();
            renderStoreMods(currentStoreFilter);
            updateProfileUI();
        }

        function openAdminUploadModal() {
            document.getElementById('adminUploadModal').style.display = 'flex';
        }
        function closeAdminUploadModal() {
            document.getElementById('adminUploadModal').style.display = 'none';
        }

        function saveAdminStoreMod() {
            const title = document.getElementById('storeModTitle').value.trim();
            const category = document.getElementById('storeModCategory').value;
            const priceType = document.getElementById('storeModPriceType').value;
            const img = document.getElementById('storeModImg').value.trim() || 'https://ddragon.leagueoflegends.com/cdn/img/champion/splash/Yasuo_0.jpg';

            if (!title) {
                showToast('Lütfen mod adını girin!');
                return;
            }

            const newMod = { id: Date.now(), title, category, priceType, img };
            storeModsList.push(newMod);
            localStorage.setItem('storeModsList', JSON.stringify(storeModsList));

            closeAdminUploadModal();
            renderStoreMods('all');
            showToast('Yeni mod mağazada yayınlandı!');
        }

        function updateStartBtnScale(val) {
            document.documentElement.style.setProperty('--start-btn-scale', val);
            document.getElementById('btnScaleValueDisplay').innerText = val + 'x';
            localStorage.setItem('startBtnScale', val);
        }

        function updateWidgetScale(val) {
            document.documentElement.style.setProperty('--widget-scale', val);
            document.getElementById('widgetScaleValueDisplay').innerText = val + 'x';
            localStorage.setItem('widgetScale', val);
        }

        function saveCustomAppBg() {
            const url = document.getElementById('appBgUrlInput').value.trim();
            if (url) {
                document.getElementById('mainAppBackground').src = url;
                localStorage.setItem('appBgUrl', url);
                showToast('Arka plan görseli güncellendi!');
            }
        }

        function handleBgFileUpload(e) {
            const file = e.target.files[0];
            if (file) {
                const reader = new FileReader();
                reader.onload = function(evt) {
                    const data = evt.target.result;
                    document.getElementById('mainAppBackground').src = data;
                    document.getElementById('appBgUrlInput').value = data;
                    localStorage.setItem('appBgUrl', data);
                    showToast('Yerel arka plan yüklendi!');
                };
                reader.readAsDataURL(file);
            }
        }

        function saveStartBtnBg() {
            const url = document.getElementById('startBtnBgInput').value.trim();
            if (url) {
                document.documentElement.style.setProperty('--start-btn-img', `url('${url}')`);
                document.getElementById('masterStartBtn').style.backgroundImage = `linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.3)), url('${url}')`;
                localStorage.setItem('startBtnBg', url);
                showToast('Başlat butonu arka planı ayarlandı!');
            }
        }

        function handleStartBtnBgFileUpload(e) {
            const file = e.target.files[0];
            if (file) {
                const reader = new FileReader();
                reader.onload = function(evt) {
                    const data = evt.target.result;
                    document.documentElement.style.setProperty('--start-btn-img', `url('${data}')`);
                    document.getElementById('masterStartBtn').style.backgroundImage = `linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.3)), url('${data}')`;
                    document.getElementById('startBtnBgInput').value = data;
                    localStorage.setItem('startBtnBg', data);
                    showToast('Buton arka plan görseli yüklendi!');
                };
                reader.readAsDataURL(file);
            }
        }

        function changeNavPosition(pos) {
            if (pos === 'top') {
                document.body.classList.add('top-nav-mode');
            } else {
                document.body.classList.remove('top-nav-mode');
            }
            localStorage.setItem('navPos', pos);
        }

        async function startGithubDbSync() {
            const btn = document.getElementById('btnGithubSync');
            const msgEl = document.getElementById('githubSyncProgressMsg');
            if (btn) {
                btn.disabled = true;
                btn.style.opacity = '0.6';
                btn.innerText = '⏳ Senkronize Ediliyor...';
            }
            if (msgEl) {
                msgEl.style.display = 'block';
                msgEl.innerText = 'GitHub sunucusu ile bağlantı kuruluyor...';
            }

            if (window.electronAPI && window.electronAPI.onSyncDbProgress) {
                window.electronAPI.onSyncDbProgress((data) => {
                    if (msgEl) msgEl.innerText = data.msg || 'İşlem devam ediyor...';
                });
            }

            try {
                if (window.electronAPI && window.electronAPI.syncDbFromGithub) {
                    const result = await window.electronAPI.syncDbFromGithub();
                    if (result && result.success) {
                        showToast('✅ Tüm skin veritabanı başarıyla indirildi ve kuruldu!');
                        document.getElementById('currentDbPathDisplay').innerText = result.path;
                    } else {
                        showToast('❌ İndirme başarısız: ' + (result ? result.error : 'Bilinmeyen hata'));
                    }
                } else {
                    showToast('⚠️ Bu özellik sadece masaüstü sürümünde aktiftir.');
                }
            } catch (err) {
                showToast('❌ Hata oluştu: ' + err.message);
            } finally {
                if (btn) {
                    btn.disabled = false;
                    btn.style.opacity = '1';
                    btn.innerText = '☁️ GitHub\'dan İndir / Senkronize Et';
                }
            }
        }

        async function autoDetectLolExe() {
            if (window.electronAPI && window.electronAPI.autoDetectLol) {
                const detected = await window.electronAPI.autoDetectLol();
                if (detected) {
                    localStorage.setItem('lolExePath', detected);
                    document.getElementById('currentLolPathDisplay').innerText = detected;
                    showToast('LeagueClient.exe otomatik olarak tespit edildi!');
                    return;
                }
            }
            const defaultPath = "C:\\Riot Games\\League of Legends\\LeagueClient.exe";
            document.getElementById('currentLolPathDisplay').innerText = defaultPath;
            localStorage.setItem('lolExePath', defaultPath);
            showToast('LeagueClient.exe varsayılan yola ayarlandı!');
        }

        function handleLolExeSelection(e) {
            const file = e.target.files[0];
            if (file) {
                document.getElementById('currentLolPathDisplay').innerText = file.path || file.name;
                localStorage.setItem('lolExePath', file.path || file.name);
                showToast('League of Legends yolu güncellendi!');
            }
        }

        function updateSpotifyEmbed() {
            const val = document.getElementById('spotifyEmbedInput').value.trim();
            if (!val) return;
            let finalUrl = val;
            if (val.includes('open.spotify.com') && !val.includes('/embed/')) {
                finalUrl = val.replace('open.spotify.com/', 'open.spotify.com/embed/');
            }
            document.getElementById('spotifyIframe').src = finalUrl;
            localStorage.setItem('spotifyUrl', finalUrl);
            showToast('Spotify çalma listesi sabitlendi!');
        }

        function initDragAndDrop() {
            const overlay = document.getElementById('dragDropOverlay');
            window.addEventListener('dragover', (e) => {
                e.preventDefault();
                overlay.style.display = 'flex';
            });
            window.addEventListener('dragleave', (e) => {
                if (e.clientX <= 0 || e.clientY <= 0 || e.clientX >= window.innerWidth || e.clientY >= window.innerHeight) {
                    overlay.style.display = 'none';
                }
            });
            window.addEventListener('drop', async (e) => {
                e.preventDefault();
                overlay.style.display = 'none';
                if (e.dataTransfer.files && e.dataTransfer.files.length > 0) {
                    const files = Array.from(e.dataTransfer.files);
                    let addedCount = 0;

                    for (const file of files) {
                        const ext = file.name.split('.').pop().toLowerCase();
                        if (['fantome', 'zip'].includes(ext)) {
                            let finalPath = file.path;
                            if (window.electronAPI && window.electronAPI.copyToInstalled && file.path) {
                                const copied = await window.electronAPI.copyToInstalled(file.path);
                                if (copied) finalPath = copied;
                            }
                            const matchedData = await detectSkinInfoAndSplash(file.name);
                            customSkinsList.push({
                                id: Date.now() + Math.random(),
                                title: matchedData.title,
                                champ: matchedData.champ,
                                img: matchedData.img,
                                path: finalPath,
                                file: file.name
                            });
                            addedCount++;
                        }
                    }

                    if (addedCount > 0) {
                        localStorage.setItem('customSkinsList', JSON.stringify(customSkinsList));
                        showToast(`${addedCount} adet özel dosya eklendi ve şampiyon resmi eşleştirildi!`);
                        switchTab('customSkins');
                        renderCustomSkins();
                        updateProfileUI();
                    } else {
                        showToast('Lütfen yalnızca .zip veya .fantome uzantılı dosya bırakın!');
                    }
                }
            });
        }

        function exportDataBackup() {
            const backupObj = {
                customSkinsList,
                storeModsList,
                skinUsageCounts,
                profileName: localStorage.getItem('profileName'),
                profileBanner: localStorage.getItem('profileBanner'),
                profileAvatar: localStorage.getItem('profileAvatar'),
                themeAccent: localStorage.getItem('themeAccent'),
                themeBg: localStorage.getItem('themeBg')
            };
            const dataStr = "data:text/json;charset=utf-8," + encodeURIComponent(JSON.stringify(backupObj, null, 2));
            const downloadAnchor = document.createElement('a');
            downloadAnchor.setAttribute("href", dataStr);
            downloadAnchor.setAttribute("download", "skynix_manager_backup.json");
            document.body.appendChild(downloadAnchor);
            downloadAnchor.click();
            downloadAnchor.remove();
            showToast('Yedek JSON dosyası indirildi!');
        }

        function importDataBackup(e) {
            const file = e.target.files[0];
            if (!file) return;
            const reader = new FileReader();
            reader.onload = function(evt) {
                try {
                    const data = JSON.parse(evt.target.result);
                    if (data.customSkinsList) {
                        customSkinsList = data.customSkinsList;
                        localStorage.setItem('customSkinsList', JSON.stringify(customSkinsList));
                    }
                    if (data.storeModsList) {
                        storeModsList = data.storeModsList;
                        localStorage.setItem('storeModsList', JSON.stringify(storeModsList));
                    }
                    if (data.profileName) localStorage.setItem('profileName', data.profileName);
                    showToast('Yedek başarıyla aktarıldı!');
                    setTimeout(() => location.reload(), 1000);
                } catch(err) {
                    showToast('Yedek dosyası okunamadı veya geçersiz format!');
                }
            };
            reader.readAsText(file);
        }

        // ========== FIREBASE LIVE NETWORK & REALTIME CHAT ==========
        const firebaseConfig = {
            databaseURL: "https://skynix-manager-default-rtdb.firebaseio.com"
        };
        
        let firebaseApp = null;
        let db = null;
        try {
            if (typeof firebase !== 'undefined') {
                firebaseApp = firebase.initializeApp(firebaseConfig);
                db = firebase.database();
            }
        } catch (err) {
            console.log("Firebase Init Note:", err);
        }

        // ========== END FRIENDS SYSTEM ==========

        // ========== AUTH SYSTEM ==========
        const ADMIN_SECRET_KEY = 'SKYNIX_ADMIN_2024';

        function getUsers() {
            return JSON.parse(localStorage.getItem('skynix_users') || '[]');
        }
        function saveUsers(users) {
            localStorage.setItem('skynix_users', JSON.stringify(users));
        }
        function getCurrentUser() {
            const uid = localStorage.getItem('skynix_current_user');
            if (!uid) return null;
            return getUsers().find(u => u.id === uid) || null;
        }
        function simpleHash(str) {
            let hash = 0;
            for (let i = 0; i < str.length; i++) {
                const char = str.charCodeAt(i);
                hash = ((hash << 5) - hash) + char;
                hash = hash & hash;
            }
            return hash.toString(36) + '_skynix';
        }
        function switchAuthTab(tab) {
            const loginForm = document.getElementById('loginForm');
            const registerForm = document.getElementById('registerForm');
            const tabLoginBtn = document.getElementById('tabLoginBtn');
            const tabRegisterBtn = document.getElementById('tabRegisterBtn');
            if (tab === 'login') {
                loginForm.style.display = 'block';
                registerForm.style.display = 'none';
                tabLoginBtn.style.background = '#06b6d4';
                tabLoginBtn.style.color = '#020617';
                tabRegisterBtn.style.background = 'transparent';
                tabRegisterBtn.style.color = '#64748b';
            } else {
                loginForm.style.display = 'none';
                registerForm.style.display = 'block';
                tabLoginBtn.style.background = 'transparent';
                tabLoginBtn.style.color = '#64748b';
                tabRegisterBtn.style.background = '#06b6d4';
                tabRegisterBtn.style.color = '#020617';
            }
        }
        // ── DISCORD OAuth GİRİŞ FONKSİYONLARI ──────────────────────────────
        async function startDiscordLogin() {
            const btn = document.getElementById('discordLoginBtn');
            const status = document.getElementById('discordLoginStatus');
            if (btn) {
                btn.disabled = true;
                btn.style.opacity = '0.6';
                btn.innerHTML = '<span style="animation:spin 1s linear infinite;display:inline-block;">⏳</span> Discord\'a bağlanılıyor...';
            }
            if (status) status.textContent = 'Discord OAuth penceresi açılıyor...';

            try {
                const result = await window.electronAPI.discordLogin();
                if (result.success) {
                    const { user } = result;
                    // Discord kullanıcısını localStorage'a kaydet
                    const discordUser = {
                        id: 'discord_' + user.id,
                        username: user.globalName || user.username,
                        discordUsername: user.username,
                        discordId: user.id,
                        avatar: user.avatar,
                        isAdmin: user.isAdmin,
                        isDiscordUser: true,
                        createdAt: Date.now()
                    };
                    // Mevcut kullanıcı listesini güncelle
                    const users = getUsers();
                    const existing = users.findIndex(u => u.discordId === user.id);
                    if (existing >= 0) {
                        users[existing] = { ...users[existing], ...discordUser };
                    } else {
                        users.push(discordUser);
                    }
                    saveUsers(users);
                    localStorage.setItem('skynix_current_user', discordUser.id);
                    localStorage.setItem('isAdminMode', user.isAdmin ? 'true' : 'false');
                    if (status) status.style.color = '#22c55e';
                    if (status) status.textContent = `✅ Hoş geldin, ${discordUser.username}!`;
                    setTimeout(() => hideLoginScreen(), 800);
                } else {
                    if (btn) {
                        btn.disabled = false;
                        btn.style.opacity = '1';
                        btn.innerHTML = '<svg width="24" height="24" viewBox="0 0 127.14 96.36" fill="white"><path d="M107.7,8.07A105.15,105.15,0,0,0,81.47,0a72.06,72.06,0,0,0-3.36,6.83A97.68,97.68,0,0,0,49,6.83,72.37,72.37,0,0,0,45.64,0,105.89,105.89,0,0,0,19.39,8.09C2.79,32.65-1.71,56.6.54,80.21A105.73,105.73,0,0,0,32.71,96.36,77.7,77.7,0,0,0,39.6,85.25a68.42,68.42,0,0,1-10.85-5.18c.91-.66,1.8-1.34,2.66-2a75.57,75.57,0,0,0,64.32,0c.87.71,1.76,1.39,2.66,2a68.68,68.68,0,0,1-10.87,5.19,77,77,0,0,0,6.89,11.1,105.25,105.25,0,0,0,32.19-16.14c2.64-27.38-4.51-51.11-18.91-72.15ZM42.45,65.69C36.18,65.69,31,60,31,53s5-12.74,11.43-12.74S54,45.91,53.87,53,48.8,65.69,42.45,65.69Zm42.24,0C78.41,65.69,73.25,60,73.25,53s5-12.74,11.44-12.74S96.23,45.91,96.1,53,91,65.69,84.69,65.69Z"/></svg> Discord ile Giriş Yap';
                    }
                    if (status) {
                        status.style.color = '#ef4444';
                        status.textContent = '❌ ' + (result.error || 'Giriş başarısız');
                    }
                }
            } catch (err) {
                if (btn) {
                    btn.disabled = false;
                    btn.style.opacity = '1';
                    btn.innerHTML = '<svg width="24" height="24" viewBox="0 0 127.14 96.36" fill="white"><path d="M107.7,8.07A105.15,105.15,0,0,0,81.47,0a72.06,72.06,0,0,0-3.36,6.83A97.68,97.68,0,0,0,49,6.83,72.37,72.37,0,0,0,45.64,0,105.89,105.89,0,0,0,19.39,8.09C2.79,32.65-1.71,56.6.54,80.21A105.73,105.73,0,0,0,32.71,96.36,77.7,77.7,0,0,0,39.6,85.25a68.42,68.42,0,0,1-10.85-5.18c.91-.66,1.8-1.34,2.66-2a75.57,75.57,0,0,0,64.32,0c.87.71,1.76,1.39,2.66,2a68.68,68.68,0,0,1-10.87,5.19,77,77,0,0,0,6.89,11.1,105.25,105.25,0,0,0,32.19-16.14c2.64-27.38-4.51-51.11-18.91-72.15ZM42.45,65.69C36.18,65.69,31,60,31,53s5-12.74,11.43-12.74S54,45.91,53.87,53,48.8,65.69,42.45,65.69Zm42.24,0C78.41,65.69,73.25,60,73.25,53s5-12.74,11.44-12.74S96.23,45.91,96.1,53,91,65.69,84.69,65.69Z"/></svg> Discord ile Giriş Yap';
                }
                if (status) {
                    status.style.color = '#ef4444';
                    status.textContent = '❌ Hata: ' + err.message;
                }
            }
        }
        function showLoginScreen() {
            const ls = document.getElementById('loginScreen');
            if (ls) ls.style.display = 'flex';
        }
        function hideLoginScreen() {
            const ls = document.getElementById('loginScreen');
            if (ls) {
                ls.style.opacity = '0';
                ls.style.transition = 'opacity 0.5s ease';
                setTimeout(() => ls.style.display = 'none', 500);
            }
            const user = getCurrentUser();
            if (user) {
                const displayName = user.globalName || user.username;
                localStorage.setItem('profileName', displayName);
                if (user.avatar) localStorage.setItem('profileAvatar', user.avatar);
                const navName = document.getElementById('navProfileName');
                if (navName) navName.textContent = displayName;
                // Ayarlar'daki rol badge'ini güncelle
                const roleBadge = document.getElementById('userRoleBadge');
                if (roleBadge) roleBadge.textContent = user.isAdmin ? '👑 Herobrine (Admin)' : '⚔️ Skynix Kullanıcısı';
                updateProfileUI();
            }
        }
        function doLogout() {
            localStorage.removeItem('skynix_current_user');
            localStorage.setItem('isAdminMode', 'false');
            location.reload();
        }
        function activateAdminMode() {
            const code = prompt('Admin aktivasyon kodunu girin:');
            if (code === ADMIN_SECRET_KEY) {
                const users = getUsers();
                const uid = localStorage.getItem('skynix_current_user');
                const user = users.find(u => u.id === uid);
                if (user) {
                    user.isAdmin = true;
                    saveUsers(users);
                }
                localStorage.setItem('isAdminMode', 'true');
                showToast('✅ Admin modu aktifleştirildi!');
                updateProfileUI();
                renderStoreMods(currentStoreFilter);
            } else if (code !== null) {
                showToast('❌ Hatalı kod!');
            }
        }
        // ========== END AUTH SYSTEM ==========

        window.addEventListener('DOMContentLoaded', async () => {
            // Oturum Kontrolü
            const currentUserCheck = localStorage.getItem('skynix_current_user');
            const ls = document.getElementById('loginScreen');
            if (!currentUserCheck || !getUsers().find(u => u.id === currentUserCheck)) {
                if (ls) ls.style.display = 'flex';
            } else {
                if (ls) ls.style.display = 'none';
                const user = getCurrentUser();
                if (user) {
                    localStorage.setItem('profileName', user.username);
                }
            }
            applyLanguage(currentLang);
            renderThemeGrid();
            await loadSavedSettings();
            initDragAndDrop();

            // Özel Skinler listesini ilk render et
            renderCustomSkins();

            const savedNavPos = localStorage.getItem('navPos') || 'side';
            document.getElementById('navPosSelect').value = savedNavPos;
            changeNavPosition(savedNavPos);

            const savedSpotify = localStorage.getItem('spotifyUrl');
            if (savedSpotify) document.getElementById('spotifyIframe').src = savedSpotify;

            const sBtnScale = localStorage.getItem('startBtnScale');
            if (sBtnScale) {
                document.getElementById('btnScaleRange').value = sBtnScale;
                updateStartBtnScale(sBtnScale);
            }
            const sWidgetScale = localStorage.getItem('widgetScale');
            if (sWidgetScale) {
                document.getElementById('widgetScaleRange').value = sWidgetScale;
                updateWidgetScale(sWidgetScale);
            }

            setInterval(() => {
                appUsageSeconds++;
                localStorage.setItem('appUsageSeconds', appUsageSeconds.toString());
            }, 1000);

            // Gerçek LoL Süreci Durum Değişikliklerini Dinle
            if (window.electronAPI && window.electronAPI.onLolStatusChange) {
                window.electronAPI.onLolStatusChange((isRunning) => {
                    const badge = document.querySelector('.client-status-badge');
                    const statusText = document.getElementById('txt-client-status');
                    if (isRunning) {
                        badge.classList.remove('disconnected');
                        if (statusText) statusText.innerText = currentLang === 'tr' ? 'LOL BAĞLI' : 'LOL CONNECTED';
                    } else {
                        badge.classList.add('disconnected');
                        if (statusText) statusText.innerText = currentLang === 'tr' ? 'LOL KAPALI' : 'LOL OFFLINE';
                    }
                });
            }

            let progress = 0;
            const bar = document.getElementById('progressBar');
            const interval = setInterval(() => {
                progress += 20;
                if (bar) bar.style.width = progress + '%';
                if (progress >= 100) {
                    clearInterval(interval);
                    const loader = document.getElementById('loadingScreen');
                    if (loader) {
                        loader.style.opacity = '0';
                        setTimeout(() => loader.style.display = 'none', 600);
                    }
                }
            }, 150);

            await fetchChampions();
            await fetchOnlineStoreMods();
        });

        async function fetchOnlineStoreMods() {
            try {
                const res = await fetch('https://raw.githubusercontent.com/Herobrine-2/skynix-database/main/store.json');
                if (res.ok) {
                    const data = await res.json();
                    if (Array.isArray(data) && data.length > 0) {
                        storeModsList = data;
                        localStorage.setItem('storeModsList', JSON.stringify(storeModsList));
                        renderStoreMods(currentStoreFilter);
                        console.log('[Store] GitHub veritabanından ' + data.length + ' mod başarıyla yüklendi.');
                    }
                }
            } catch (err) {
                console.warn('[Store] Online mağaza çekilemedi, yerel veri kullanılıyor:', err.message);
            }
        }
    </script>
</body>
</html>
