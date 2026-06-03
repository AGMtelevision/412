<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AGM Limited-Time Invitation Event - South Africa</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #FF8C00 0%, #FFA500 100%);
            color: #333;
            line-height: 1.6;
        }

        /* Header */
        header {
            background: linear-gradient(135deg, #FF6600 0%, #FF8C00 100%);
            color: white;
            padding: 20px;
            text-align: center;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        header h1 {
            font-size: 28px;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }

        header p {
            font-size: 14px;
            opacity: 0.95;
        }

        /* Countdown Timer */
        .countdown-section {
            background: white;
            margin: 20px;
            padding: 25px;
            border-radius: 15px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
            text-align: center;
        }

        .countdown-section h2 {
            color: #FF6600;
            margin-bottom: 20px;
            font-size: 22px;
        }

        .countdown-timer {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 15px;
            margin-bottom: 20px;
        }

        .countdown-item {
            background: linear-gradient(135deg, #FF8C00 0%, #FFA500 100%);
            color: white;
            padding: 15px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }

        .countdown-item .number {
            font-size: 32px;
            font-weight: bold;
            display: block;
        }

        .countdown-item .label {
            font-size: 12px;
            margin-top: 5px;
            opacity: 0.9;
        }

        .countdown-status {
            font-size: 16px;
            color: #FF6600;
            font-weight: bold;
        }

        /* Lucky Draw Wheel */
        .wheel-section {
            background: white;
            margin: 20px;
            padding: 25px;
            border-radius: 15px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
            text-align: center;
        }

        .wheel-section h2 {
            color: #FF6600;
            margin-bottom: 20px;
            font-size: 22px;
        }

        .wheel-container {
            display: flex;
            justify-content: center;
            align-items: center;
            margin: 20px 0;
            position: relative;
        }

        .lucky-wheel {
            width: 300px;
            height: 300px;
            border-radius: 50%;
            background: conic-gradient(
                from 0deg,
                #FF6600 0deg 45deg,
                #FFB347 45deg 90deg,
                #FF8C00 90deg 135deg,
                #FFA500 135deg 180deg,
                #FF7700 180deg 225deg,
                #FF9500 225deg 270deg,
                #FF6600 270deg 315deg,
                #FFB347 315deg 360deg
            );
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
            position: relative;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .wheel-center {
            width: 80px;
            height: 80px;
            background: radial-gradient(circle, #FF6600, #FF3300);
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            color: white;
            font-weight: bold;
            font-size: 18px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
            z-index: 2;
        }

        .wheel-pointer {
            position: absolute;
            top: -15px;
            width: 0;
            height: 0;
            border-left: 15px solid transparent;
            border-right: 15px solid transparent;
            border-top: 25px solid #FF3300;
            z-index: 3;
        }

        .wheel-labels {
            position: absolute;
            width: 100%;
            height: 100%;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .wheel-label {
            position: absolute;
            width: 90%;
            height: 90%;
            display: flex;
            justify-content: center;
            align-items: flex-start;
            padding-top: 10px;
            font-weight: bold;
            color: white;
            font-size: 14px;
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);
        }

        .wheel-label:nth-child(1) { transform: rotate(22.5deg); }
        .wheel-label:nth-child(2) { transform: rotate(67.5deg); }
        .wheel-label:nth-child(3) { transform: rotate(112.5deg); }
        .wheel-label:nth-child(4) { transform: rotate(157.5deg); }
        .wheel-label:nth-child(5) { transform: rotate(202.5deg); }
        .wheel-label:nth-child(6) { transform: rotate(247.5deg); }
        .wheel-label:nth-child(7) { transform: rotate(292.5deg); }
        .wheel-label:nth-child(8) { transform: rotate(337.5deg); }

        .wheel-note {
            margin-top: 15px;
            font-size: 14px;
            color: #FF6600;
            font-weight: bold;
        }

        /* Content Section */
        .content-section {
            background: white;
            margin: 20px;
            padding: 25px;
            border-radius: 15px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
        }

        .content-section h2 {
            color: #FF6600;
            margin-bottom: 20px;
            font-size: 22px;
            border-bottom: 3px solid #FFA500;
            padding-bottom: 10px;
        }

        .content-subsection {
            margin-bottom: 25px;
        }

        .content-subsection h3 {
            color: #FF8C00;
            margin-bottom: 15px;
            font-size: 18px;
        }

        .reward-item {
            background: #FFF8F0;
            padding: 15px;
            margin-bottom: 12px;
            border-radius: 8px;
            border-left: 4px solid #FF6600;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .reward-item-text {
            flex: 1;
            font-size: 15px;
        }

        .reward-badge {
            background: linear-gradient(135deg, #FF6600, #FF8C00);
            color: white;
            padding: 8px 15px;
            border-radius: 20px;
            font-weight: bold;
            white-space: nowrap;
            margin-left: 10px;
            font-size: 14px;
        }

        .highlight-text {
            color: #FF6600;
            font-weight: bold;
        }

        /* Event Details */
        .event-details {
            background: linear-gradient(135deg, #FF8C00, #FFA500);
            color: white;
            padding: 20px;
            border-radius: 10px;
            margin-top: 20px;
            text-align: center;
        }

        .event-details p {
            margin: 8px 0;
            font-size: 15px;
        }

        .event-details strong {
            font-size: 18px;
        }

        /* Footer */
        footer {
            background: linear-gradient(135deg, #333 0%, #555 100%);
            color: white;
            padding: 25px;
            text-align: center;
            margin-top: 20px;
        }

        .phone-number-section {
            margin-bottom: 20px;
        }

        .phone-number-section p {
            margin-bottom: 8px;
            font-size: 14px;
        }

        .virtual-phone {
            background: linear-gradient(135deg, #FF6600, #FF8C00);
            color: white;
            padding: 12px 20px;
            border-radius: 8px;
            font-weight: bold;
            font-size: 20px;
            display: inline-block;
            margin: 10px 0;
            letter-spacing: 2px;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0%, 100% {
                opacity: 1;
            }
            50% {
                opacity: 0.7;
            }
        }

        .prize-ticker {
            background: white;
            color: #FF6600;
            padding: 12px 20px;
            border-radius: 8px;
            font-weight: bold;
            font-size: 16px;
            margin-top: 15px;
            overflow: hidden;
            position: relative;
        }

        .prize-ticker-content {
            display: flex;
            gap: 30px;
            animation: scroll 10s linear infinite;
        }

        @keyframes scroll {
            0% {
                transform: translateX(100%);
            }
            100% {
                transform: translateX(-100%);
            }
        }

        .prize-item {
            white-space: nowrap;
            padding: 0 20px;
        }

        footer p {
            margin: 8px 0;
            font-size: 13px;
            opacity: 0.9;
        }

        footer a {
            color: #FFA500;
            text-decoration: none;
        }

        footer a:hover {
            text-decoration: underline;
        }

        /* Responsive */
        @media (max-width: 768px) {
            header h1 {
                font-size: 22px;
            }

            .countdown-timer {
                grid-template-columns: repeat(2, 1fr);
                gap: 10px;
            }

            .countdown-item .number {
                font-size: 24px;
            }

            .lucky-wheel {
                width: 250px;
                height: 250px;
            }

            .wheel-center {
                width: 65px;
                height: 65px;
                font-size: 14px;
            }

            .wheel-label {
                font-size: 12px;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <h1>🎉 Limited-Time Invitation Event 🎉</h1>
        <p>AGM APP - South Africa Expansion Celebration</p>
    </header>

    <!-- Countdown Timer -->
    <div class="countdown-section">
        <h2>⏰ Event Countdown</h2>
        <div class="countdown-timer">
            <div class="countdown-item">
                <span class="number" id="days">0</span>
                <span class="label">Days</span>
            </div>
            <div class="countdown-item">
                <span class="number" id="hours">0</span>
                <span class="label">Hours</span>
            </div>
            <div class="countdown-item">
                <span class="number" id="minutes">0</span>
                <span class="label">Minutes</span>
            </div>
            <div class="countdown-item">
                <span class="number" id="seconds">0</span>
                <span class="label">Seconds</span>
            </div>
        </div>
        <div class="countdown-status" id="eventStatus">Event is Active!</div>
    </div>

    <!-- Lucky Draw Wheel (Display Only) -->
    <div class="wheel-section">
        <h2>💰 Lucky Draw Wheel - View Only</h2>
        <div class="wheel-container">
            <div class="lucky-wheel">
                <div class="wheel-pointer"></div>
                <div class="wheel-labels">
                    <div class="wheel-label">R1000</div>
                    <div class="wheel-label">R800</div>
                    <div class="wheel-label">R500</div>
                    <div class="wheel-label">R1500</div>
                    <div class="wheel-label">R2000</div>
                    <div class="wheel-label">R10000</div>
                    <div class="wheel-label">R5000</div>
                    <div class="wheel-label">R3000</div>
                </div>
                <div class="wheel-center">AGM</div>
            </div>
        </div>
        <div class="wheel-note">🔒 Display Only - Lucky Draw Wheel (Non-Interactive)</div>
    </div>

    <!-- Event Content -->
    <div class="content-section">
        <h2>📢 Event Overview</h2>
        <p style="font-size: 16px; line-height: 1.8; color: #555;">
            To expand AGM APP's business in South Africa, AGM will be hosting an incentive event to recognize the hard work and contributions of all employees. We encourage everyone to participate and share this opportunity with family and friends, contributing to the company's growth, generating more income, and creating a better life for their families.
        </p>
    </div>

    <!-- Rewards Section -->
    <div class="content-section">
        <h2>🎁 Rewards Program</h2>

        <!-- Invitation Rewards -->
        <div class="content-subsection">
            <h3>1️⃣ Invitation Rewards</h3>
            <div class="reward-item">
                <div class="reward-item-text">
                    <span class="highlight-text">→ Invite an intern to join G1</span>
                </div>
                <div class="reward-badge">R54 + 1 Draw</div>
            </div>
            <div class="reward-item">
                <div class="reward-item-text">
                    <span class="highlight-text">→ Invite an intern to join G2</span>
                </div>
                <div class="reward-badge">R216 + 2 Draws</div>
            </div>
        </div>

        <!-- Intern Rewards -->
        <div class="content-subsection">
            <h3>2️⃣ Intern Rewards</h3>
            <div class="reward-item">
                <div class="reward-item-text">
                    <span class="highlight-text">→ Upgrade to G1</span>
                </div>
                <div class="reward-badge">1 Draw</div>
            </div>
            <div class="reward-item">
                <div class="reward-item-text">
                    <span class="highlight-text">→ Upgrade to G2</span>
                </div>
                <div class="reward-badge">2 Draws</div>
            </div>
        </div>

        <!-- Lucky Draw Prizes -->
        <div class="content-subsection">
            <h3>3️⃣ Lucky Draw Prizes</h3>
            <div class="event-details">
                <p><strong>Maximum Reward: R10,000</strong></p>
                <p>💎 Grand Prize Pool Available for Lucky Winners!</p>
            </div>
        </div>

        <!-- Event Details -->
        <div class="event-details" style="margin-top: 25px;">
            <p>📅 Event Period: <strong>June 1-4, 2026</strong></p>
            <p>📝 Note: If you meet the requirements for the holiday event, please contact the hiring manager to apply for the reward.</p>
        </div>
    </div>

    <!-- Footer -->
    <footer>
        <div class="phone-number-section">
            <p>🔒 Protected Privacy Virtual Contact Number:</p>
            <div class="virtual-phone" id="virtualPhone">+27 (***) ***-****</div>
            <div class="prize-ticker">
                <div class="prize-ticker-content" id="prizeTicker">
                    <div class="prize-item">🎉 R10,000 Prize Available</div>
                    <div class="prize-item">🎁 Limited Slots - Join Now</div>
                    <div class="prize-item">💰 Max Rewards Awaiting Winners</div>
                    <div class="prize-item">🌟 Your Future Starts Here</div>
                    <div class="prize-item">🎯 South Africa Opportunity</div>
                </div>
            </div>
        </div>
        <hr style="margin: 20px 0; opacity: 0.3;">
        <p>&copy; 2026 AGM APP - South Africa Expansion Event. All Rights Reserved.</p>
        <p>For inquiries: <a href="mailto:support@agmapp.com">support@agmapp.com</a></p>
        <p style="font-size: 12px; margin-top: 15px; opacity: 0.7;">This is a limited-time promotional event. Terms and conditions apply.</p>
    </footer>

    <script>
        // Countdown Timer Function
        function updateCountdown() {
            const eventStart = new Date('2026-06-01T00:00:00').getTime();
            const eventEnd = new Date('2026-06-04T23:59:59').getTime();
            const now = new Date().getTime();

            // For demonstration, we'll use a target date approach
            const targetDate = new Date('2026-06-04T23:59:59').getTime();
            const distance = targetDate - now;

            if (distance < 0) {
                document.getElementById('eventStatus').textContent = 'Event Has Ended!';
                document.getElementById('eventStatus').style.color = '#999';
                return;
            }

            const days = Math.floor(distance / (1000 * 60 * 60 * 24));
            const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((distance % (1000 * 60)) / 1000);

            document.getElementById('days').textContent = String(days).padStart(2, '0');
            document.getElementById('hours').textContent = String(hours).padStart(2, '0');
            document.getElementById('minutes').textContent = String(minutes).padStart(2, '0');
            document.getElementById('seconds').textContent = String(seconds).padStart(2, '0');

            if (distance > 0) {
                document.getElementById('eventStatus').textContent = '⏳ Event is Active - Time to Join!';
            }
        }

        // Generate Virtual Phone Number
        function generateVirtualPhone() {
            const baseNumber = '+27 (';
            const area = String(Math.floor(Math.random() * 900) + 100);
            const first = String(Math.floor(Math.random() * 9000) + 1000);
            const last = String(Math.floor(Math.random() * 9000) + 1000);
            
            document.getElementById('virtualPhone').textContent = `+27 (${area}) ${first}-${last}`;
        }

        // Initialize
        updateCountdown();
        generateVirtualPhone();

        // Update countdown every second
        setInterval(updateCountdown, 1000);

        // Regenerate phone number every 5 seconds for privacy effect
        setInterval(generateVirtualPhone, 5000);

        // Duplicate prize ticker content for seamless scrolling
        const tickerContent = document.getElementById('prizeTicker');
        const originalHTML = tickerContent.innerHTML;
        tickerContent.innerHTML = originalHTML + originalHTML;
    </script>
</body>
</html>
