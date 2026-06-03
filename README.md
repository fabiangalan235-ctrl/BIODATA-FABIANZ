<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>Biodata | Fabian Galan</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', 'Poppins', 'Inter', system-ui, -apple-system, BlinkMacSystemFont, 'Roboto', sans-serif;
            background: linear-gradient(145deg, #e0eafc 0%, #cfdef3 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 2rem 1rem;
        }

        /* Kartu biodata utama */
        .biodata-card {
            max-width: 700px;
            width: 100%;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(0px);
            border-radius: 2.5rem;
            box-shadow: 0 25px 45px -12px rgba(0, 0, 0, 0.35), 0 8px 18px rgba(0, 0, 0, 0.1);
            overflow: hidden;
            transition: transform 0.25s ease, box-shadow 0.3s;
        }

        .biodata-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 30px 50px -15px rgba(0, 0, 0, 0.4);
        }

        /* Header / banner */
        .header-banner {
            background: linear-gradient(135deg, #1a2a6c, #b21f1f, #fdbb4d);
            background-size: 200% 200%;
            padding: 2rem 1.8rem;
            text-align: center;
            color: white;
            border-bottom-left-radius: 1.2rem;
            border-bottom-right-radius: 1.2rem;
        }

        .header-banner h1 {
            font-size: 2.2rem;
            letter-spacing: -0.5px;
            font-weight: 700;
            margin-bottom: 0.3rem;
            text-shadow: 2px 2px 6px rgba(0,0,0,0.2);
            word-break: break-word;
        }

        .header-banner .badge {
            background: rgba(255,255,255,0.2);
            backdrop-filter: blur(6px);
            display: inline-block;
            padding: 0.3rem 1rem;
            border-radius: 40px;
            font-size: 0.85rem;
            font-weight: 500;
            margin-top: 0.5rem;
        }

        /* konten biodata */
        .bio-content {
            padding: 2rem 2rem 1.5rem;
        }

        /* grid informasi */
        .info-grid {
            display: flex;
            flex-direction: column;
            gap: 1.2rem;
            margin-bottom: 2rem;
        }

        .info-item {
            display: flex;
            align-items: baseline;
            flex-wrap: wrap;
            border-bottom: 1px dashed #cbd5e1;
            padding-bottom: 0.7rem;
        }

        .info-label {
            font-weight: 700;
            width: 130px;
            font-size: 1.05rem;
            color: #1e293b;
            letter-spacing: -0.2px;
        }

        .info-value {
            flex: 1;
            font-size: 1.05rem;
            color: #0f172a;
            font-weight: 500;
            background: #f8fafc;
            padding: 0.2rem 0.8rem;
            border-radius: 20px;
            display: inline-block;
            width: fit-content;
            min-width: 180px;
        }

        /* kotak motivasi / motto */
        .motivation-box {
            background: #fef9e3;
            border-left: 8px solid #f59e0b;
            border-radius: 1.2rem;
            padding: 1rem 1.4rem;
            margin: 1rem 0 1.8rem 0;
            box-shadow: 0 6px 12px -8px rgba(0,0,0,0.1);
            transition: all 0.2s;
        }

        .motivation-box p:first-child {
            font-weight: 700;
            font-size: 1rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            color: #b45309;
            margin-bottom: 0.5rem;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .motivation-box p:first-child span {
            font-size: 1.3rem;
        }

        .motivation-quote {
            font-size: 1.3rem;
            font-weight: 600;
            color: #2c3e2f;
            line-height: 1.4;
            word-break: break-word;
            font-style: italic;
        }

        /* tombol link */
        .btn-link-container {
            text-align: center;
            margin: 0.5rem 0 0.8rem;
        }

        .custom-link-btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 12px;
            background: linear-gradient(95deg, #0f172a, #1e293b);
            color: white;
            text-decoration: none;
            font-weight: 600;
            font-size: 1rem;
            padding: 0.9rem 2rem;
            border-radius: 60px;
            transition: all 0.25s ease;
            border: none;
            cursor: pointer;
            box-shadow: 0 8px 14px -6px rgba(0, 0, 0, 0.2);
            letter-spacing: 0.3px;
            width: auto;
            min-width: 220px;
        }

        .custom-link-btn:hover {
            background: linear-gradient(95deg, #2d3a5e, #0f172a);
            transform: scale(1.02);
            box-shadow: 0 12px 20px -8px rgba(0, 0, 0, 0.3);
            text-decoration: none;
            color: #facc15;
        }

        .custom-link-btn:active {
            transform: scale(0.98);
        }

        /* ikon eksternal kecil */
        .external-icon {
            font-size: 1.2rem;
            transition: transform 0.2s;
        }

        /* footer kecil */
        .footer-note {
            text-align: center;
            font-size: 0.7rem;
            color: #475569;
            border-top: 1px solid #e2e8f0;
            padding: 1rem;
            background: #f9fafb;
        }

        /* Responsif */
        @media (max-width: 550px) {
            .bio-content {
                padding: 1.5rem;
            }
            .info-label {
                width: 100%;
                margin-bottom: 6px;
            }
            .info-item {
                flex-direction: column;
                gap: 5px;
            }
            .info-value {
                width: 100%;
                padding: 0.3rem 0.8rem;
            }
            .motivation-quote {
                font-size: 1.1rem;
            }
            .header-banner h1 {
                font-size: 1.6rem;
            }
            .custom-link-btn {
                padding: 0.7rem 1.2rem;
                font-size: 0.9rem;
                width: 100%;
            }
        }

        /* aksen tambahan */
        .highlight {
            background: linear-gradient(120deg, #f1f5f9, #ffffff);
        }
    </style>
</head>
<body>

<div class="biodata-card">
    <div class="header-banner">
        <h1>✨ Fabian Galan ✨</h1>
        <div class="badge">#PantangMenyerah #GenerasiHebat</div>
    </div>
    
    <div class="bio-content">
        <div class="info-grid">
            <!-- NAMA -->
            <div class="info-item">
                <div class="info-label">📛 Nama Lengkap</div>
                <div class="info-value">FABIAN GALAN</div>
            </div>
            <!-- UMUR -->
            <div class="info-item">
                <div class="info-label">🎂 Umur</div>
                <div class="info-value">16 tahun</div>
            </div>
            <!-- ASAL SEKOLAH -->
            <div class="info-item">
                <div class="info-label">🏫 Asal Sekolah</div>
                <div class="info-value">SMAN 15 JAKARTA</div>
            </div>
            <!-- KELAS -->
            <div class="info-item">
                <div class="info-label">📚 Kelas</div>
                <div class="info-value">X-5</div>
            </div>
        </div>
        
        <!-- KATA-KATA MOTIVASI / MOTO HIDUP -->
        <div class="motivation-box">
            <p>
                <span>🌟</span> MOTTO HIDUP / KATA MOTIVASI
            </p>
            <div class="motivation-quote">
                “ SEHAT SELALU DAN SUKSES ”
            </div>
            <div style="margin-top: 8px; font-size: 0.75rem; color: #a16207; text-align: right;">
                — Fabian Galan, tetap semangat!
            </div>
        </div>
        
        <!-- TOMBOL LINK sesuai permintaan (https://fabiangalan235-ctrl.github.io/gem-balap-balap/) -->
        <div class="btn-link-container">
            <a href="https://fabiangalan235-ctrl.github.io/gem-balap-balap/" 
               target="_blank" 
               rel="noopener noreferrer"
               class="custom-link-btn">
                <span>🚀 Kunjungi Link Gem Balap Balap</span>
                <span class="external-icon">🔗</span>
            </a>
            <p style="font-size: 0.7rem; margin-top: 12px; color: #334155;">
                ⚡ Tekan tombol di atas untuk melihat proyek keren Fabian!
            </p>
        </div>
    </div>
    
    <div class="footer-note">
        <span>© 2025 • Fabian Galan • Tetap Sehat & Sukses</span>
    </div>
</div>

</body>
</html>
