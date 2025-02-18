<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Website Kelas X-8</title>
    <style>
        :root {
            --primary: #2563eb;
            --secondary: #1e40af;
            --accent: #f97316;
            --background: #f8fafc;
            --text: #1e293b;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Inter', sans-serif;
        }

        body {
            background-color: var(--background);
            color: var(--text);
            line-height: 1.6;
        }

        /* Header Styles */
        .header {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            padding: 1rem;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 100;
        }

        .navbar {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0.5rem;
        }

        .logo {
            color: white;
            font-size: 1.5rem;
            font-weight: bold;
            text-decoration: none;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
        }

        .nav-link {
            color: white;
            text-decoration: none;
            padding: 0.5rem 1rem;
            border-radius: 0.5rem;
            transition: all 0.3s ease;
        }

        .nav-link:hover {
            background-color: rgba(255, 255, 255, 0.1);
        }

        .menu-toggle {
            display: none;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
            background: none;
            border: none;
        }

        /* Hero Section */
        .hero {
            margin-top: 5rem;
            padding: 4rem 1rem;
            text-align: center;
            background: white;
        }

        .hero h1 {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 1rem;
        }

        .hero p {
            color: var(--text);
            max-width: 600px;
            margin: 0 auto;
        }

        /* Card Grid */
        .card-grid {
            max-width: 1200px;
            margin: 2rem auto;
            padding: 0 1rem;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .card {
            background: white;
            border-radius: 1rem;
            padding: 2rem;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }

        .card:hover {
            transform: translateY(-5px);
        }

        .card h3 {
            color: var(--primary);
            margin-bottom: 1rem;
        }

        .card-icon {
            font-size: 2rem;
            margin-bottom: 1rem;
            color: var(--accent);
        }

        /* Schedule Section */
        .schedule {
            max-width: 1200px;
            margin: 2rem auto;
            padding: 2rem 1rem;
            background: white;
            border-radius: 1rem;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        .schedule h2 {
            color: var(--primary);
            margin-bottom: 1.5rem;
        }

        .schedule-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1rem;
        }

        .schedule-item {
            padding: 1rem;
            background: var(--background);
            border-radius: 0.5rem;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .schedule-item:hover {
            background: var(--primary);
            color: white;
        }

        /* Announcement Section */
        .announcements {
            max-width: 1200px;
            margin: 2rem auto;
            padding: 2rem 1rem;
        }

        .announcement-card {
            background: white;
            border-radius: 1rem;
            padding: 1.5rem;
            margin-bottom: 1rem;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
            cursor: pointer;
            transition: transform 0.3s ease;
        }

        .announcement-card:hover {
            transform: translateX(10px);
        }

        .announcement-date {
            color: var(--accent);
            font-size: 0.875rem;
        }

        /* Modal */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5);
            align-items: center;
            justify-content: center;
            z-index: 1000;
        }

        .modal-content {
            background: white;
            padding: 2rem;
            border-radius: 1rem;
            max-width: 500px;
            width: 90%;
            position: relative;
        }

        .close-modal {
            position: absolute;
            top: 1rem;
            right: 1rem;
            font-size: 1.5rem;
            cursor: pointer;
            background: none;
            border: none;
            color: var(--text);
        }

        /* Footer */
        .footer {
            background: var(--secondary);
            color: white;
            padding: 3rem 1rem;
            margin-top: 4rem;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }

        .footer-section h3 {
            margin-bottom: 1rem;
        }

        .footer-links {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 0.5rem;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
                position: absolute;
                top: 100%;
                left: 0;
                right: 0;
                background: var(--primary);
                flex-direction: column;
                padding: 1rem;
            }

            .nav-links.active {
                display: flex;
            }

            .menu-toggle {
                display: block;
            }

            .hero h1 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <header class="header">
        <nav class="navbar">
            <a href="#" class="logo">Class X-8</a>
            <button class="menu-toggle">☰</button>
            <div class="nav-links">
                <a href="Jadwal Pelajran.html" class="nav-link">Jadwal</a>
                <a href="materi.html" class="nav-link">Materi</a>
                <a href="galeri.html" class="nav-link">Galeri</a>
            </div>
        </nav>
    </header>

    <section class="hero">
        <h1>Selamat Datang di X-8</h1>
        <p>Mari belajar dan berkembang bersama untuk mencapai prestasi terbaik!</p>
    </section>

    <div class="card-grid">
        <div class="card">
            <div class="card-icon">📚 </div>
            <h3>Materi Pembelajaran</h3>
            <p>Akses semua materi pelajaran dengan mudah dan terorganisir</p>
            <button><a href="materi.html">klik disini</a></button>
        </div>
        <div class="card">
            <div class="card-icon" >📅</div>
            <h3>Jadwal Pelajaran</h3>
            <p>Lihat jadwal pelajaran harian dan mingguan kelas</p>
            <button><a href="Jadwal Pelajran.html">klik disini</a></button>
        </div>
    </div>

    <section class="schedule" id="jadwal">
        <h2>Jam Pelajaran</h2>
        <div class="schedule-grid">
            <div class="schedule-item">
                <h4>06:45 - 07:30</h4>
                <p>JP I</p>
            </div>
            <div class="schedule-item">
                <h4>07:30 - 08:15</h4>
                <p>JP II</p>
            </div>
            <div class="schedule-item">
                <h4>08:15 - 09:45</h4>
                <p>JP IV</p>
            </div>
            <div class="schedule-item">
                <h4>09:45 - 10:00</h4>
                <p>ISTIRAHAT I</p>
            </div>
            <div class="schedule-item">
                <h4>10:00 - 10:45</h4>
                <p>JP V</p>
            </div>
            <div class="schedule-item">
                <h4>10:45 - 11:30</h4>
                <p>JP VI</p>
            </div>
            <div class="schedule-item">
                <h4>11:30 - 12:15</h4>
                <p>JP VII</p>
            </div>
            <div class="schedule-item">
                <h4>12:15 - 13:00</h4>
                <p>ISTIRAHAT II</p>
            </div>
            <div class="schedule-item">
                <h4>13:00 - 13:45</h4>
                <p>jp VIII</p>
            </div>
            <div class="schedule-item">
                <h4>13:45 - 14:30</h4>
                <p>JP IX</p>
            </div>
            <div class="schedule-item">
                <h4>14:30 - 15:15</h4>
                <p>JP X</p>
            </div>
        </div>
    </section>

    <section class="announcements">
        <div class="announcement-card">
            <h3>Ujian Tengah Semester</h3>
            <p>Selesai</p>
            <div class="announcement-date">30 September 2024</div>
        </div>
        <div class="announcement-card">
            <h3>Ujian Akhir Semester</h3>
            <p></p>
            <div class="announcement-date">Menunggu Info lebih lanjut dari pihak sekolah</div>
        </div>
    </section>

    <div class="modal" id="modal">
        <div class="modal-content">
            <button class="close-modal">&times;</button>
            <h2 id="modal-title"></h2>
            <p id="modal-content"></p>
        </div>
    </div>

    <footer class="footer">
        <div class="footer-content">
            <div class="footer-section">
                <h3>Tentang Kami</h3>
                <p>Website resmi kelas X-8 SMA Negeri 1 Mojosari.</p>
            </div>
        </div>
    </footer>

    <script>
        // Menu Toggle
        const menuToggle = document.querySelector('.menu-toggle');
        const navLinks = document.querySelector('.nav-links');

        menuToggle.addEventListener('click', () => {
            navLinks.classList.toggle('active');
        });

        // Modal Functionality
        const modal = document.getElementById('modal');
        const modalTitle = document.getElementById('modal-title');
        const modalContent = document.getElementById('modal-content');
        const closeModal = document.querySelector('.close-modal');

        function showModal(title, content) {
            modalTitle.textContent = title;
            modalContent.textContent = content;
            modal.style.display = 'flex';
        }

        closeModal.addEventListener('click', () => {
            modal.style.display = 'none';
        });

        window.addEventListener('click', (e) => {
            if (e.target === modal) {
                modal.style.display = 'none';
            }
        });

        // Schedule Items Click Handler
        const scheduleItems = document.querySelectorAll('.schedule-item');
        scheduleItems.forEach(item => {
            item.addEventListener('click', () => {
                const time = item.querySelector('h4').textContent;
                const subject = item.querySelector('p').textContent;
                showModal('Detail Jadwal', `Jam Pelajaran: ${subject}\nWaktu: ${time}`);
            });
        });

        // Announcement Cards Click Handler
        const announcementCards = document.querySelectorAll('.announcement-card');
        announcementCards.forEach(card => {
            card.addEventListener('click', () => {
                const title = card.querySelector('h3').textContent;
                const content = card.querySelector('p').textContent;
                showModal(title, content);
            });
        });

        // Smooth Scroll for Navigation
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
