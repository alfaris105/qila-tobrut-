<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Apk Unban WhatsApp</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f5f5f5;
            color: #333;
            line-height: 1.6;
            padding: 20px;
            max-width: 500px;
            margin: 0 auto;
        }
        
        header {
            text-align: center;
            margin-bottom: 30px;
        }
        
        h1 {
            font-size: 24px;
            color: #075e54;
            margin-bottom: 5px;
        }
        
        .author {
            font-size: 14px;
            color: #666;
            margin-bottom: 20px;
        }
        
        .section {
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            margin-bottom: 20px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        
        h2 {
            font-size: 18px;
            color: #075e54;
            margin-bottom: 15px;
        }
        
        .input-group {
            margin: 15px 0;
        }
        
        .input-label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
            color: #333;
        }
        
        .phone-input {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 16px;
            transition: border-color 0.3s;
        }
        
        .phone-input:focus {
            border-color: #128c7e;
            outline: none;
        }
        
        hr {
            border: none;
            border-top: 1px solid #ddd;
            margin: 20px 0;
        }
        
        .option-group {
            margin: 20px 0;
        }
        
        .option-label {
            display: block;
            margin-bottom: 10px;
            font-weight: bold;
            color: #333;
        }
        
        .radio-option {
            display: flex;
            align-items: center;
            margin-bottom: 10px;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .radio-option:hover {
            background-color: #f9f9f9;
        }
        
        .radio-option input {
            margin-right: 10px;
        }
        
        .btn {
            display: block;
            width: 100%;
            padding: 15px;
            background-color: #25d366;
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 16px;
            font-weight: bold;
            cursor: pointer;
            transition: background-color 0.3s;
            text-align: center;
            text-decoration: none;
        }
        
        .btn:hover {
            background-color: #128c7e;
        }
        
        .btn:disabled {
            background-color: #cccccc;
            cursor: not-allowed;
        }
        
        .info-box {
            background-color: #e8f4fd;
            border-left: 4px solid #128c7e;
            padding: 15px;
            margin-top: 20px;
            border-radius: 0 5px 5px 0;
            font-size: 14px;
        }
        
        footer {
            text-align: center;
            margin-top: 30px;
            color: #666;
            font-size: 12px;
        }
        
        .error-message {
            color: #e74c3c;
            font-size: 14px;
            margin-top: 5px;
            display: none;
        }
    </style>
</head>
<body>
    <header>
        <h1>Apk Unban WhatsApp</h1>
        <div class="author">by @hamzmiw</div>
    </header>
    
    <main>
        <section class="section">
            <h2>Apk Unban WhatsApp</h2>
            
            <div class="input-group">
                <label class="input-label" for="phoneNumber">Nomor WhatsApp yang diblokir</label>
                <input type="text" id="phoneNumber" class="phone-input" placeholder="+62xxxxxxxxxxx">
                <div class="error-message" id="phoneError">Nomor Lu Salah Masukan Sesuai Format : +62xxxxxxxxxxx</div>
            </div>
            
            <hr>
            
            <div class="option-group">
                <span class="option-label">Pillin Opsi Band</span>
                
                <label class="radio-option">
                    <input type="radio" name="banType" value="permanent-fresh">
                    <span>Permanent Fresh</span>
                </label>
                
                <label class="radio-option">
                    <input type="radio" name="banType" value="permanent-hard">
                    <span>Permanent Hard</span>
                </label>
            </div>
            
            <button id="submitBtn" class="btn" disabled>Gas Unban</button>
            
            <div class="info-box">
                Jika sudah menekan tombol tersebut diem in selama 1-7 jam jika fresh gak jebol banding ulang di hari ke tujuh,work chat @hamzmiw
            </div>
        </section>
    </main>
    
    <footer>
        &copy; Apk Unban WhatsApp
    </footer>

    <script>
        const phoneInput = document.getElementById('phoneNumber');
        const phoneError = document.getElementById('phoneError');
        const submitBtn = document.getElementById('submitBtn');
        
        // Validasi nomor telepon
        function validatePhoneNumber(phone) {
            const phoneRegex = /^\+62\d{9,12}$/;
            return phoneRegex.test(phone);
        }
        
        // Update status tombol berdasarkan input
        function updateSubmitButton() {
            const phone = phoneInput.value.trim();
            const selectedOption = document.querySelector('input[name="banType"]:checked');
            
            const isPhoneValid = validatePhoneNumber(phone);
            const isOptionSelected = selectedOption !== null;
            
            if (isPhoneValid && isOptionSelected) {
                submitBtn.disabled = false;
            } else {
                submitBtn.disabled = true;
            }
            
            // Tampilkan/sembunyikan pesan error
            if (phone && !isPhoneValid) {
                phoneError.style.display = 'block';
            } else {
                phoneError.style.display = 'none';
            }
        }
        
        // Event listeners
        phoneInput.addEventListener('input', updateSubmitButton);
        
        const radioOptions = document.querySelectorAll('input[name="banType"]');
        radioOptions.forEach(option => {
            option.addEventListener('change', updateSubmitButton);
        });
        
        // Submit handler
        submitBtn.addEventListener('click', function() {
            const selectedOption = document.querySelector('input[name="banType"]:checked');
            const phoneNumber = phoneInput.value.trim();
            
            if (!validatePhoneNumber(phoneNumber)) {
                alert('Nomor Lu Salah Masukan Sesuai Format : +62xxxxxxxxxxx');
                return;
            }
            
            if (!selectedOption) {
                alert('Silakan pilih opsi band terlebih dahulu!');
                return;
            }
            
            // Template pesan berdasarkan opsi yang dipilih
            let subject = "WhatsApp Account Unban Request";
            let messageBody = "";
            
            if (selectedOption.value === "permanent-fresh") {
                messageBody = `Здравствуйте, службы поддержки WhatsApp и Meta WhatsApp!

Я пользуюсь официальным аккаунтом WhatsApp уже два года. Час назад мой аккаунт заблокировали. Я в панике, потому что потеряю все свои личные данные. Прошу вас восстановить мой аккаунт.

Мой аккаунт WhatsApp заблокирован навсегда [https://wa.me/${phoneNumber}].

Написав это сообщение, я обжалую блокировку моего аккаунта WhatsApp. Я уверен, что не нарушил никаких условий WhatsApp, но почему мой аккаунт всё ещё заблокирован?

Мой аккаунт WhatsApp используется для общения с коллегами, семьёй, бабушкой и дедушкой. Моя бабушка сейчас больна, поэтому я не знаю, чего ожидать, если вы заблокируете мой аккаунт WhatsApp.

Надеюсь, вы пересмотрите решение о блокировке моего аккаунта WhatsApp. Умоляю вас восстановить мой аккаунт WhatsApp, чтобы я мог снова им пользоваться. Он мне очень нужен. Написав это сообщение, я прошу вас помочь мне восстановить мой аккаунт WhatsApp. Выражаю своё почтение Марку и командам WhatsApp и Meta AI.

С уважением,
Hamz`;
            } else if (selectedOption.value === "permanent-hard") {
                messageBody = `안녕하세요, WhatsApp 고객 지원팀과 Meta AI입니다.

WhatsApp 계정 영구 차단에 대한 이의를 제기하고자 합니다. 새 전화번호를 등록했습니다. WhatsApp 계정 복구를 위해 이의를 제기하고 싶습니다.

제 WhatsApp 번호는 [https://wa.me/${phoneNumber}]입니다.

WhatsApp 계정을 복구하여 다시 사용할 수 있도록 요청드립니다. 2019년에 인도의 누군가에게 WhatsApp 계정이 해킹당했습니다. 제 계정은 즉시 영구적으로 차단되었고, 현재까지도 차단되지 않고 있습니다. WhatsApp 고객 지원팀과 Meta AI 지원팀의 도움을 부탁드립니다. 감사합니다.

감사합니다.
Hamz`;
            }
            
            // Encode untuk URL
            const encodedSubject = encodeURIComponent(subject);
            const encodedBody = encodeURIComponent(messageBody);
            
            // Buat URL Gmail
            const gmailUrl = `https://mail.google.com/mail/?view=cm&fs=1&to=support@support.whatsapp.com&su=${encodedSubject}&body=${encodedBody}`;
            
            // Buka Gmail di tab baru
            window.open(gmailUrl, '_blank');
            
            // Tampilkan pesan konfirmasi
            alert('Gmail sedang dibuka. Silakan kirim pesan banding Anda dan tunggu balasan dari WhatsApp.');
        });
    </script>
</body>
</html>
