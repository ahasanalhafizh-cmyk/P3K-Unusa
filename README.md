<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>P3K Digital | Dashboard Navigasi Modern</title>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;600;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            --danger: #e11d48;
            --danger-gradient: linear-gradient(135deg, #e11d48 0%, #fb7185 100%);
            --dark: #0f172a;
            --secondary: #64748b;
            --light: #f8fafc;
            --white: #ffffff;
            --shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Plus Jakarta Sans', sans-serif;
        }

        body {
            background-color: var(--light);
            display: flex;
            min-height: 100vh;
            color: var(--dark);
        }

        /* Sidebar Glassmorphism */
        nav {
            width: 280px;
            background: var(--dark);
            padding: 30px 20px;
            display: flex;
            flex-direction: column;
            color: white;
            position: fixed;
            height: 100vh;
        }

        .nav-logo {
            font-size: 1.5rem;
            font-weight: 800;
            margin-bottom: 40px;
            display: flex;
            align-items: center;
            gap: 10px;
            color: #fb7185;
        }

        .nav-info-box {
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            padding: 20px;
            margin-top: auto;
            cursor: pointer;
            transition: 0.3s;
        }

        .nav-info-box:hover {
            background: rgba(255, 255, 255, 0.1);
            transform: translateY(-5px);
        }

        /* Main Content */
        main {
            flex: 1;
            margin-left: 280px;
            padding: 50px;
        }

        .header-section {
            margin-bottom: 40px;
        }

        .header-section h1 {
            font-size: 2.5rem;
            font-weight: 800;
            background: var(--danger-gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        /* Card Grid */
        .grid-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
        }

        .card {
            background: var(--white);
            border-radius: 24px;
            padding: 35px 25px;
            text-align: center;
            text-decoration: none;
            color: var(--dark);
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            box-shadow: var(--shadow);
            border: 1px solid #f1f5f9;
            cursor: pointer;
        }

        .card:hover {
            transform: translateY(-15px);
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1);
            border-color: #fb7185;
        }

        .card-icon {
            width: 80px;
            height: 80px;
            margin: 0 auto 20px;
            background: #fff1f2;
            color: var(--danger);
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            transition: 0.3s;
        }

        .card:hover .card-icon {
            background: var(--danger-gradient);
            color: white;
            transform: rotate(10deg);
        }

        .card h3 {
            font-size: 1.3rem;
            margin-bottom: 10px;
            font-weight: 700;
        }

        .card p {
            color: var(--secondary);
            font-size: 0.9rem;
            line-height: 1.5;
        }

        /* Detail Area */
        #detail-area {
            display: none;
            margin-top: 40px;
            animation: slideUp 0.5s ease;
        }

        @keyframes slideUp {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body>

    <nav>
        <div class="nav-logo">
            <i class="fas fa-hand-holding-medical"></i>
            <span>P3K DIGITAL</span>
        </div>
             <p style="font-size: 0.85rem; color: #94a3b8; line-height: 1.6;">
               Aplikasi panduan darurat untuk memberikan pertolongan pertama secara cepat, tepat, dan aman.
                </p>

        <div class="nav-info-box" onclick="tampilkan('definisi')">
            <h4 style="font-size: 0.9rem; margin-bottom: 8px; color: #fb7185;">
                <i class="fas fa-info-circle"></i> DEFINISI P3K
            </h4>
            <p style="font-size: 0.75rem; color: #cbd5e1; text-align: justify;">
                Upaya pertolongan dan perawatan sementara terhadap korban kecelakaan sebelum bantuan medis tiba.
            </p>
        </div>
    </nav>

    <main>
        <div class="header-section">
             <p style="animation: var(--danger-gradient); text-align: text-transform uppercase; letter-spacing: 2px; margin-bottom: 10px;">Universitas Nahdlatul Ulama Surabaya</p>
            <p style="font-weight: 600; color: var(--danger); text-transform: uppercase; letter-spacing: 2px; margin-bottom: 10px;">Menu Utama</p>
            <h1>Dashboard Panduan P3K Digital</h1>
        </div>

        <div class="grid-container">
            <div class="card" onclick="navigasi('perdarahan')">
                <div class="card-icon"><i class="fas fa-droplet"></i></div>
                <h3>Perdarahan</h3>
                <p>Teknik menekan luka, posisi tubuh, dan penggunaan torniket yang benar.</p>
            </div>

             <div class="card" onclick="navigasi('Luka')">
               <div class="card-icon"><i class="fas fa-hospital"></i></div>
                <h3>luka</h3>
                <p>Cara stabilisasi luka, dan penanganan.</p>
            </div>

            <div class="card" onclick="navigasi('balut')">
                <div class="card-icon"><i class="fas fa-bandage"></i></div>
                <h3>Pembalutan</h3>
                <p>Mengenal jenis pembalut, isi kotak P3K, dan teknik membalut luka.</p>
            </div>
            
            <div class="card" onclick="navigasi('patah')">
                <div class="card-icon"><i class="fas fa-bone"></i></div>
                <h3>Patah Tulang</h3>
                <p>Cara stabilisasi tulang, penggunaan bidai, dan penanganan dislokasi.</p>
            </div>

            <div class="card" onclick="navigasi('bakar')">
                <div class="card-icon"><i class="fas fa-fire-flame-curved" style="color: #f97316;"></i></div>
                <h3>lukabakar</h3>
                <p>Cara stabilisasi tulang, penggunaan bidai, dan penanganan dislokasi.</p>
            </div>
        </div>

        <div id="detail-area">
            <div id="isi-detail"></div>
            <button onclick="tutupDetail()" style="margin-top:20px; padding: 10px 25px; border-radius: 10px; border: none; background: var(--dark); color: white; cursor: pointer;">
                <i class="fas fa-arrow-left"></i> Kembali ke Atas
            </button>
        </div>
    </main>

    <script>
        function navigasi(kategori) {
            if (kategori === 'perdarahan') {
                window.location.href = "perdarahan.html";
            } else if (kategori === 'balut') {
                window.location.href = "pembalutan.html";
            } else if (kategori === 'bakar') {
                window.location.href = "lukabakar.html";
             } else if (kategori === 'Luka') {
                window.location.href = "luka.html";
            } else if (kategori === 'patah') {
                window.location.href = "Patahtulang.html";
            }
        }

        function tampilkan(kategori) {
            const detailArea = document.getElementById("detail-area");
            const isiDetail = document.getElementById("isi-detail");
            
            if (kategori === 'definisi') {
                detailArea.style.display = "block";
                isiDetail.innerHTML = `
                    <div style="background: white; padding: 40px; border-radius: 30px; border-left: 10px solid var(--danger); box-shadow: var(--shadow);">
                        <h2 style="margin-bottom: 20px;"><i class="fas fa-book-medical" style="color: var(--danger)"></i> Apa itu P3K?</h2>
                        <p style="font-size: 1.1rem; line-height: 1.8; color: #475569;">
                            <strong>Pertolongan Pertama Pada Kecelakaan (P3K)</strong> adalah upaya pertolongan dan perawatan sementara terhadap korban kecelakaan sebelum mendapat pertolongan yang lebih sempurna dari dokter atau paramedik.
                        </p>
                        <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin-top: 30px;">
                            <div style="background: #f8fafc; padding: 20px; border-radius: 15px;">
                                <h4 style="color: var(--danger)">Tujuan Utama:</h4>
                                <ul style="margin-top: 10px; padding-left: 20px; font-size: 0.9rem;">
                                    <li>Menyelamatkan jiwa korban</li>
                                    <li>Mencegah cacat permanen</li>
                                    <li>Mencegah infeksi</li>
                                    <li>Mengurangi rasa sakit dan rasa takut</li>
                                    <li>Menunjang proses penyembuhan</li>
                                </ul>
                            </div>
                        </div>
                    </div>
                `;
                detailArea.scrollIntoView({ behavior: 'smooth' });
            }
        }

        function tutupDetail() {
            document.getElementById("detail-area").style.display = "none";
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }
    </script>
</body>
</html>
