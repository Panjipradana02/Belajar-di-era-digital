<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Digital Citizen vs Citizen Journalism</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        .slide {
            background: rgba(255, 255, 255, 0.95);
            margin: 20px 0;
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
            animation: slideIn 0.8s ease-out;
        }
        
        @keyframes slideIn {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        h1 {
            color: #2c3e50;
            text-align: center;
            font-size: 2.5em;
            margin-bottom: 30px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
        }
        
        h2 {
            color: #3498db;
            font-size: 2em;
            margin-bottom: 20px;
            border-bottom: 3px solid #3498db;
            padding-bottom: 10px;
        }
        
        h3 {
            color: #e74c3c;
            font-size: 1.5em;
            margin: 20px 0 15px 0;
        }
        
        p {
            color: #34495e;
            margin-bottom: 15px;
            font-size: 1.1em;
        }
        
        .comparison-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
            margin: 30px 0;
        }
        
        .card {
            background: linear-gradient(135deg, #74b9ff, #0984e3);
            padding: 25px;
            border-radius: 10px;
            color: white;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }
        
        .card:hover {
            transform: translateY(-5px);
        }
        
        .card h3 {
            color: white;
            margin-bottom: 15px;
        }
        
        .card2 {
            background: linear-gradient(135deg, #fd79a8, #e84393);
        }
        
        .characteristics {
            background: #f8f9fa;
            padding: 20px;
            border-radius: 10px;
            margin: 20px 0;
            border-left: 5px solid #3498db;
        }
        
        .characteristics ul {
            list-style: none;
            padding-left: 0;
        }
        
        .characteristics li {
            background: white;
            margin: 10px 0;
            padding: 15px;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            position: relative;
            padding-left: 50px;
        }
        
        .characteristics li::before {
            content: "✓";
            position: absolute;
            left: 15px;
            top: 15px;
            color: #27ae60;
            font-weight: bold;
            font-size: 1.2em;
        }
        
        .table-container {
            overflow-x: auto;
            margin: 30px 0;
        }
        
        table {
            width: 100%;
            border-collapse: collapse;
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        th, td {
            padding: 15px;
            text-align: left;
            border-bottom: 1px solid #ddd;
        }
        
        th {
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            font-weight: bold;
        }
        
        tr:hover {
            background-color: #f5f5f5;
        }
        
        .highlight {
            background: linear-gradient(120deg, #a8edea 0%, #fed6e3 100%);
            padding: 20px;
            border-radius: 10px;
            margin: 20px 0;
            border-left: 5px solid #ff6b6b;
        }
        
        .navigation {
            position: fixed;
            top: 20px;
            right: 20px;
            background: rgba(255, 255, 255, 0.9);
            padding: 15px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .nav-btn {
            background: #3498db;
            color: white;
            border: none;
            padding: 10px 15px;
            margin: 5px;
            border-radius: 5px;
            cursor: pointer;
            transition: background 0.3s ease;
        }
        
        .nav-btn:hover {
            background: #2980b9;
        }
        
        @media (max-width: 768px) {
            .comparison-grid {
                grid-template-columns: 1fr;
            }
            
            .slide {
                padding: 20px;
                margin: 10px 0;
            }
            
            h1 {
                font-size: 2em;
            }
            
            .navigation {
                position: static;
                margin: 20px 0;
            }
        }
        
        .quiz-section {
            background: linear-gradient(135deg, #ffecd2 0%, #fcb69f 100%);
            padding: 25px;
            border-radius: 15px;
            margin: 30px 0;
        }
        
        .quiz-btn {
            background: #e74c3c;
            color: white;
            border: none;
            padding: 12px 25px;
            border-radius: 25px;
            cursor: pointer;
            font-size: 1.1em;
            transition: all 0.3s ease;
        }
        
        .quiz-btn:hover {
            background: #c0392b;
            transform: scale(1.05);
        }
    </style>
</head>
<body>
    <div class="navigation">
        <button class="nav-btn" onclick="scrollToSlide(0)">Judul</button>
        <button class="nav-btn" onclick="scrollToSlide(1)">Definisi</button>
        <button class="nav-btn" onclick="scrollToSlide(2)">Perbandingan</button>
        <button class="nav-btn" onclick="scrollToSlide(3)">Kesimpulan</button>
    </div>

    <div class="container">
        <!-- Slide 1: Judul -->
        <div class="slide" id="slide-0">
            <h1>🌐 Digital Citizen vs Citizen Journalism</h1>
            <p style="text-align: center; font-size: 1.3em; color: #7f8c8d;">
                Media Pembelajaran Digital<br>
                <strong>Memahami Perbedaan dan Karakteristik</strong>
            </p>
            <div style="text-align: center; margin-top: 30px;">
                <div style="display: inline-block; background: linear-gradient(135deg, #74b9ff, #0984e3); color: white; padding: 15px 30px; border-radius: 25px; font-size: 1.2em;">
                    📚 Pembelajaran Interaktif
                </div>
            </div>
        </div>

        <!-- Slide 2: Definisi -->
        <div class="slide" id="slide-1">
            <h2>📖 Definisi dan Konsep Dasar</h2>
            
            <div class="comparison-grid">
                <div class="card">
                    <h3>🧑‍💻 Digital Citizen</h3>
                    <p>Individu yang menggunakan teknologi digital dan internet secara bertanggung jawab, etis, dan produktif dalam kehidupan sehari-hari.</p>
                </div>
                
                <div class="card card2">
                    <h3>📰 Citizen Journalism</h3>
                    <p>Praktik individu biasa (bukan jurnalis profesional) yang mengumpulkan, melaporkan, dan menyebarkan berita menggunakan platform digital.</p>
                </div>
            </div>
        </div>

        <!-- Slide 3: Karakteristik Digital Citizen -->
        <div class="slide" id="slide-2">
            <h2>🌟 Karakteristik Digital Citizen</h2>
            
            <div class="characteristics">
                <ul>
                    <li><strong>Literasi Digital:</strong> Kemampuan menggunakan teknologi dengan baik dan memahami cara kerja platform digital</li>
                    <li><strong>Etika Digital:</strong> Berperilaku sopan dan menghormati orang lain di ruang digital</li>
                    <li><strong>Keamanan Digital:</strong> Memahami cara melindungi data pribadi dan privasi online</li>
                    <li><strong>Hukum Digital:</strong> Mengetahui dan mematuhi aturan hukum yang berlaku di dunia digital</li>
                    <li><strong>Komunikasi Digital:</strong> Berkomunikasi secara efektif dan bertanggung jawab di platform digital</li>
                    <li><strong>Akses Digital:</strong> Memiliki kesempatan yang sama untuk mengakses teknologi digital</li>
                    <li><strong>Perdagangan Digital:</strong> Memahami hak dan kewajiban sebagai konsumen atau penjual online</li>
                    <li><strong>Kesehatan Digital:</strong> Menjaga keseimbangan antara kehidupan digital dan fisik</li>
                </ul>
            </div>
        </div>

        <!-- Slide 4: Karakteristik Citizen Journalism -->
        <div class="slide">
            <h2>📱 Karakteristik Citizen Journalism</h2>
            
            <div class="characteristics">
                <ul>
                    <li><strong>Pelaporan Langsung:</strong> Melaporkan peristiwa yang disaksikan atau dialami secara langsung</li>
                    <li><strong>Penggunaan Media Sosial:</strong> Memanfaatkan platform seperti Twitter, Facebook, Instagram, blog</li>
                    <li><strong>Dokumentasi Real-time:</strong> Memberikan laporan atau dokumentasi kejadian secara langsung</li>
                    <li><strong>Perspektif Lokal:</strong> Memberikan sudut pandang dari tingkat grassroot atau komunitas lokal</li>
                    <li><strong>Interaktif:</strong> Memungkinkan dialog dan diskusi dengan pembaca/penonton</li>
                    <li><strong>Akses Mudah:</strong> Dapat dilakukan oleh siapa saja yang memiliki perangkat digital</li>
                    <li><strong>Kecepatan:</strong> Sering kali lebih cepat dari media mainstream</li>
                    <li><strong>Subjektivitas:</strong> Cenderung lebih subjektif dibanding jurnalisme profesional</li>
                </ul>
            </div>
        </div>

        <!-- Slide 5: Tabel Perbandingan -->
        <div class="slide" id="slide-3">
            <h2>⚖️ Perbandingan Lengkap</h2>
            
            <div class="table-container">
                <table>
                    <thead>
                        <tr>
                            <th>Aspek</th>
                            <th>Digital Citizen</th>
                            <th>Citizen Journalism</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td><strong>Ruang Lingkup</strong></td>
                            <td>Mencakup seluruh aspek kehidupan digital</td>
                            <td>Fokus pada kegiatan jurnalistik/pelaporan</td>
                        </tr>
                        <tr>
                            <td><strong>Tujuan Utama</strong></td>
                            <td>Menjadi warga yang bertanggung jawab di dunia digital</td>
                            <td>Menyampaikan informasi/berita kepada publik</td>
                        </tr>
                        <tr>
                            <td><strong>Aktivitas</strong></td>
                            <td>Konsumsi dan partisipasi digital secara umum</td>
                            <td>Produksi dan distribusi konten berita</td>
                        </tr>
                        <tr>
                            <td><strong>Keterampilan</strong></td>
                            <td>Literasi digital umum</td>
                            <td>Keterampilan jurnalistik dasar</td>
                        </tr>
                        <tr>
                            <td><strong>Tanggung Jawab</strong></td>
                            <td>Etika dan keamanan personal</td>
                            <td>Akurasi informasi dan dampak sosial</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </div>

        <!-- Slide 6: Keterkaitan -->
        <div class="slide">
            <h2>🔗 Keterkaitan dan Hubungan</h2>
            
            <div class="highlight">
                <h3>💡 Insight Penting:</h3>
                <p><strong>Citizen journalism</strong> sebenarnya merupakan <strong>bagian dari</strong> praktik digital citizenship. Seorang citizen journalist yang baik harus terlebih dahulu menjadi digital citizen yang bertanggung jawab.</p>
            </div>
            
            <div style="background: white; padding: 25px; border-radius: 10px; margin: 20px 0;">
                <h3>🎯 Mengapa Keterkaitan Ini Penting?</h3>
                <p>Citizen journalist perlu memahami:</p>
                <ul style="margin-left: 20px; color: #34495e;">
                    <li>Etika digital dalam menyebarkan informasi</li>
                    <li>Verifikasi informasi sebelum dipublikasikan</li>
                    <li>Dampak dari konten yang mereka sebarkan</li>
                    <li>Tanggung jawab sosial sebagai pembuat konten</li>
                </ul>
            </div>
        </div>

        <!-- Slide 7: Kesimpulan -->
        <div class="slide">
            <h2>🎓 Kesimpulan</h2>
            
            <div style="background: linear-gradient(135deg, #a8edea 0%, #fed6e3 100%); padding: 25px; border-radius: 15px;">
                <h3>🔑 Poin Kunci:</h3>
                <ol style="font-size: 1.1em; line-height: 1.8;">
                    <li><strong>Digital Citizen</strong> = Konsep yang lebih luas tentang warga digital yang bertanggung jawab</li>
                    <li><strong>Citizen Journalism</strong> = Aktivitas spesifik dalam melaporkan berita secara mandiri</li>
                    <li>Keduanya membutuhkan <strong>literasi digital</strong> dan <strong>tanggung jawab</strong></li>
                    <li>Citizen journalism adalah <strong>bagian dari</strong> digital citizenship</li>
                    <li>Partisipasi aktif dan bertanggung jawab adalah kunci utama keduanya</li>
                </ol>
            </div>
            
            <div class="quiz-section">
                <h3>🧠 Uji Pemahaman Anda!</h3>
                <p>Klik tombol di bawah untuk memulai kuis interaktif:</p>
                <button class="quiz-btn" onclick="startQuiz()">Mulai Kuis 🚀</button>
            </div>
        </div>
    </div>

    <script>
        let currentQuiz = 0;
        let score = 0;
        let userName = '';
        let userId = '';
        
        // KONFIGURASI TELEGRAM BOT
        const TELEGRAM_BOT_TOKEN = '7621118144:AAHGfdKRStE5-0MBQm-Nsgz0ilfX3rsC1C8';
        const TELEGRAM_CHAT_ID = '5336726671';
        
        const quizQuestions = [
            {
                question: "Apa yang dimaksud dengan Digital Citizen?",
                options: [
                    "Orang yang hanya menggunakan internet",
                    "Individu yang menggunakan teknologi digital secara bertanggung jawab",
                    "Jurnalis yang bekerja online",
                    "Pembuat konten media sosial"
                ],
                correct: 1
            },
            {
                question: "Karakteristik utama Citizen Journalism adalah:",
                options: [
                    "Hanya melaporkan berita politik",
                    "Bekerja untuk media besar",
                    "Melaporkan peristiwa secara real-time oleh individu biasa",
                    "Menggunakan peralatan profesional"
                ],
                correct: 2
            },
            {
                question: "Hubungan antara Digital Citizen dan Citizen Journalism adalah:",
                options: [
                    "Keduanya tidak berhubungan",
                    "Citizen Journalism bagian dari Digital Citizenship",
                    "Digital Citizen bagian dari Citizen Journalism",
                    "Keduanya sama persis"
                ],
                correct: 1
            }
        ];

        function scrollToSlide(slideNumber) {
            const slide = document.getElementById(`slide-${slideNumber}`);
            if (slide) {
                slide.scrollIntoView({ behavior: 'smooth' });
            }
        }

        function startQuiz() {
            // Reset quiz data
            currentQuiz = 0;
            score = 0;
            
            // Minta input nama dan ID siswa
            const userDataHTML = `
                <div style="background: white; padding: 25px; border-radius: 15px; margin: 20px 0;">
                    <h3>📝 Data Siswa</h3>
                    <p>Masukkan data Anda sebelum memulai kuis:</p>
                    <input type="text" id="userName" placeholder="Nama Lengkap" style="width: 100%; padding: 10px; margin: 10px 0; border: 2px solid #ddd; border-radius: 5px; font-size: 1em;">
                    <input type="text" id="userId" placeholder="NIM/NIS/ID Siswa" style="width: 100%; padding: 10px; margin: 10px 0; border: 2px solid #ddd; border-radius: 5px; font-size: 1em;">
                    <button class="quiz-btn" onclick="validateAndStartQuiz()" style="margin-top: 15px;">Mulai Kuis 🚀</button>
                </div>
            `;
            
            document.querySelector('.quiz-section').innerHTML = userDataHTML;
        }

        function validateAndStartQuiz() {
            userName = document.getElementById('userName').value.trim();
            userId = document.getElementById('userId').value.trim();
            
            if (!userName || !userId) {
                alert('Mohon lengkapi nama dan ID siswa!');
                return;
            }
            
            showQuiz();
        }

        function showQuiz() {
            if (currentQuiz < quizQuestions.length) {
                const quiz = quizQuestions[currentQuiz];
                let optionsHTML = quiz.options.map((option, index) => 
                    `<button class="quiz-btn" style="display: block; margin: 10px 0; width: 100%;" onclick="checkAnswer(${index})">${option}</button>`
                ).join('');
                
                const quizHTML = `
                    <div style="background: white; padding: 25px; border-radius: 15px; margin: 20px 0;">
                        <h3>Pertanyaan ${currentQuiz + 1} dari ${quizQuestions.length}:</h3>
                        <p style="font-size: 1.2em; margin: 20px 0;">${quiz.question}</p>
                        ${optionsHTML}
                        <p style="margin-top: 20px; color: #666;"><strong>Skor: ${score}/${currentQuiz}</strong></p>
                    </div>
                `;
                
                document.querySelector('.quiz-section').innerHTML = quizHTML;
            } else {
                sendScoreToTelegram();
            }
        }

        async function sendScoreToTelegram() {
            const finalScore = score;
            const totalQuestions = quizQuestions.length;
            const percentage = Math.round((finalScore / totalQuestions) * 100);
            const grade = getGrade(percentage);
            const timestamp = new Date().toLocaleString('id-ID');
            
            const message = `
🎓 HASIL KUIS PEMBELAJARAN
📚 Materi: Digital Citizen vs Citizen Journalism

👤 Nama: ${userName}
🆔 ID: ${userId}
📅 Waktu: ${timestamp}

📊 HASIL:
✅ Benar: ${finalScore}
❌ Salah: ${totalQuestions - finalScore}
📈 Nilai: ${percentage}%
🏆 Grade: ${grade}

${getMotivationalMessage(percentage)}
            `.trim();
            
            // Tampilkan hasil di halaman
            displayFinalResult(finalScore, totalQuestions, percentage, grade);
            
            // Kirim ke Telegram
            try {
                const response = await fetch(`https://api.telegram.org/bot${TELEGRAM_BOT_TOKEN}/sendMessage`, {
                    method: 'POST',
                    headers: {
                        'Content-Type': 'application/json',
                    },
                    body: JSON.stringify({
                        chat_id: TELEGRAM_CHAT_ID,
                        text: message,
                        parse_mode: 'Markdown'
                    })
                });
                
                if (response.ok) {
                    console.log('✅ Hasil berhasil dikirim ke Telegram!');
                    showTelegramStatus('✅ Nilai berhasil dikirim ke Telegram!', 'success');
                } else {
                    console.error('❌ Gagal mengirim ke Telegram:', response.statusText);
                    showTelegramStatus('⚠️ Gagal mengirim ke Telegram', 'error');
                }
            } catch (error) {
                console.error('❌ Error mengirim ke Telegram:', error);
                showTelegramStatus('⚠️ Error koneksi ke Telegram', 'error');
            }
        }

        function displayFinalResult(finalScore, totalQuestions, percentage, grade) {
            const resultColor = percentage >= 80 ? '#2ecc71' : percentage >= 60 ? '#f39c12' : '#e74c3c';
            
            document.querySelector('.quiz-section').innerHTML = `
                <div style="background: ${resultColor}; color: white; padding: 25px; border-radius: 15px; text-align: center;">
                    <h3>🎉 Kuis Selesai!</h3>
                    <div style="background: rgba(255,255,255,0.2); padding: 20px; border-radius: 10px; margin: 20px 0;">
                        <h2>${userName}</h2>
                        <p><strong>ID: ${userId}</strong></p>
                        <div style="font-size: 2em; margin: 10px 0;">${percentage}%</div>
                        <div style="font-size: 1.5em; margin: 10px 0;">Grade: ${grade}</div>
                        <p>Benar: ${finalScore}/${totalQuestions}</p>
                    </div>
                    <p>${getMotivationalMessage(percentage)}</p>
                    <button class="quiz-btn" onclick="startQuiz()" style="background: white; color: ${resultColor}; margin: 10px;">Ulangi Kuis</button>
                    <button class="quiz-btn" onclick="downloadCertificate()" style="background: rgba(255,255,255,0.2); border: 2px solid white; margin: 10px;">📜 Download Sertifikat</button>
                </div>
            `;
        }

        function getGrade(percentage) {
            if (percentage >= 90) return 'A+';
            if (percentage >= 85) return 'A';
            if (percentage >= 80) return 'A-';
            if (percentage >= 75) return 'B+';
            if (percentage >= 70) return 'B';
            if (percentage >= 65) return 'B-';
            if (percentage >= 60) return 'C+';
            if (percentage >= 55) return 'C';
            if (percentage >= 50) return 'C-';
            return 'D';
        }

        function getMotivationalMessage(percentage) {
            if (percentage >= 90) return '🌟 Luar biasa! Anda menguasai materi dengan sangat baik!';
            if (percentage >= 80) return '👏 Bagus sekali! Pemahaman Anda sangat baik!';
            if (percentage >= 70) return '👍 Baik! Anda memahami sebagian besar materi!';
            if (percentage >= 60) return '📚 Cukup baik, tapi masih bisa ditingkatkan!';
            return '💪 Jangan menyerah! Coba pelajari lagi materinya!';
        }

        function showTelegramStatus(message, type) {
            const statusColor = type === 'success' ? '#2ecc71' : '#e74c3c';
            const statusDiv = document.createElement('div');
            statusDiv.innerHTML = `
                <div style="background: ${statusColor}; color: white; padding: 10px; border-radius: 5px; margin: 10px 0; text-align: center; animation: fadeInOut 3s ease-in-out;">
                    ${message}
                </div>
            `;
            document.querySelector('.quiz-section').appendChild(statusDiv);
            
            // Hapus status setelah 3 detik
            setTimeout(() => {
                if (statusDiv.parentNode) {
                    statusDiv.parentNode.removeChild(statusDiv);
                }
            }, 3000);
        }

        function downloadCertificate() {
            const percentage = Math.round((score / quizQuestions.length) * 100);
            const grade = getGrade(percentage);
            const date = new Date().toLocaleDateString('id-ID');
            
            // Buat canvas untuk sertifikat
            const canvas = document.createElement('canvas');
            canvas.width = 800;
            canvas.height = 600;
            const ctx = canvas.getContext('2d');
            
            // Background gradient
            const gradient = ctx.createLinearGradient(0, 0, 800, 600);
            gradient.addColorStop(0, '#667eea');
            gradient.addColorStop(1, '#764ba2');
            ctx.fillStyle = gradient;
            ctx.fillRect(0, 0, 800, 600);
            
            // Border
            ctx.strokeStyle = 'white';
            ctx.lineWidth = 10;
            ctx.strokeRect(20, 20, 760, 560);
            
            // Title
            ctx.fillStyle = 'white';
            ctx.font = 'bold 36px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('SERTIFIKAT PEMBELAJARAN', 400, 100);
            
            // Content
            ctx.font = '24px Arial';
            ctx.fillText('Diberikan kepada:', 400, 180);
            
            ctx.font = 'bold 32px Arial';
            ctx.fillText(userName, 400, 230);
            
            ctx.font = '20px Arial';
            ctx.fillText(`ID: ${userId}`, 400, 270);
            
            ctx.font = '22px Arial';
            ctx.fillText('Telah menyelesaikan kuis', 400, 320);
            ctx.fillText('Digital Citizen vs Citizen Journalism', 400, 350);
            
            ctx.font = 'bold 28px Arial';
            ctx.fillText(`Nilai: ${percentage}% (Grade ${grade})`, 400, 420);
            
            ctx.font = '18px Arial';
            ctx.fillText(`Tanggal: ${date}`, 400, 480);
            
            // Download
            const link = document.createElement('a');
            link.download = `Sertifikat_${userName.replace(/\s+/g, '_')}_${userId}.png`;
            link.href = canvas.toDataURL();
            link.click();
        }

        function checkAnswer(selectedIndex) {
            const quiz = quizQuestions[currentQuiz];
            const isCorrect = selectedIndex === quiz.correct;
            
            if (isCorrect) {
                score++;
            }
            
            const resultHTML = `
                <div style="background: ${isCorrect ? '#2ecc71' : '#e74c3c'}; color: white; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h3>${isCorrect ? '✅ Benar!' : '❌ Salah!'}</h3>
                    <p>Jawaban yang benar: ${quiz.options[quiz.correct]}</p>
                    <p><strong>Skor saat ini: ${score}/${currentQuiz + 1}</strong></p>
                    <button class="quiz-btn" onclick="nextQuestion()" style="background: white; color: ${isCorrect ? '#2ecc71' : '#e74c3c'};">Lanjut</button>
                </div>
            `;
            
            document.querySelector('.quiz-section').innerHTML = resultHTML;
        }

        function nextQuestion() {
            currentQuiz++;
            showQuiz();
        }

        // Smooth scrolling untuk navigasi
        document.addEventListener('DOMContentLoaded', function() {
            const slides = document.querySelectorAll('.slide');
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.opacity = '1';
                        entry.target.style.transform = 'translateY(0)';
                    }
                });
            }, { threshold: 0.1 });

            slides.forEach(slide => {
                observer.observe(slide);
            });
        });
    </script>
</body>
</html>
