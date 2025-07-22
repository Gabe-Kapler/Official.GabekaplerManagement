# Official.GabekaplerManagement
Official Gabe Kapler Management Pipeline For Change Foundation 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>KapConnect - Gabe Kapler Official</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700;800&display=swap" rel="stylesheet">
    <style>
        :root {
            --marlins-blue: #00A3E0;
            --marlins-orange: #EF4A81;
            --marlins-black: #000000;
            --marlins-gray: #D0D3D4;
            --marlins-red: #C41E3A;
            --light: #f8f9fa;
            --dark: #212529;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Montserrat', sans-serif;
        }

        body {
            background-color: #f0f2f5;
            color: var(--dark);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Header Styles */
        header {
            background: linear-gradient(rgba(0,0,0,0.8), rgba(0,0,0,0.8)), url('https://images.unsplash.com/photo-1549633030-83d2d4a6b90e?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1920&q=80') center/cover;
            color: white;
            padding: 1rem 0;
            position: relative;
            border-bottom: 5px solid var(--marlins-orange);
        }

        .header-content {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        .top-bar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 0;
        }

        .logo-container {
            display: flex;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
        }

        .logo-circle {
            width: 70px;
            height: 70px;
            border-radius: 50%;
            background: var(--marlins-black);
            position: relative;
            overflow: hidden;
            box-shadow: 0 2px 10px rgba(0,0,0,0.2);
        }

        .baseball-seams {
            position: absolute;
            width: 100%;
            height: 100%;
            background: 
                linear-gradient(to bottom, transparent 49%, var(--light) 49%, var(--light) 51%, transparent 51%),
                linear-gradient(to right, transparent 49%, var(--light) 49%, var(--light) 51%, transparent 51%);
            opacity: 0.2;
        }

        .letter-k {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            font-size: 40px;
            font-weight: 900;
            color: var(--light);
            text-shadow: 0 0 5px rgba(0,0,0,0.5);
        }

        .marlins-teal {
            position: absolute;
            top: 0;
            right: 0;
            width: 40%;
            height: 40%;
            background: var(--marlins-blue);
            clip-path: polygon(0 0, 100% 0, 100% 100%);
        }

        .marlins-orange {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 40%;
            height: 40%;
            background: var(--marlins-orange);
            clip-path: polygon(0 100%, 100% 100%, 0 0);
        }

        .marlins-black {
            position: absolute;
            top: 15%;
            left: 15%;
            width: 70%;
            height: 70%;
            border: 3px solid var(--marlins-black);
            border-radius: 50%;
        }

        .logo-text {
            margin-left: 15px;
            display: flex;
            flex-direction: column;
            line-height: 1;
        }

        .text-main {
            font-size: 28px;
            color: var(--light);
            letter-spacing: -1px;
            font-weight: 800;
        }

        .text-sub {
            font-size: 16px;
            color: var(--marlins-blue);
            font-weight: 600;
            letter-spacing: 2px;
            margin-top: 3px;
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav ul li {
            margin-left: 2rem;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
            text-transform: uppercase;
            font-size: 14px;
            letter-spacing: 1px;
        }

        nav ul li a:hover {
            color: var(--marlins-orange);
        }

        .hero {
            text-align: center;
            padding: 6rem 1rem;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            text-transform: uppercase;
            letter-spacing: 2px;
            background: linear-gradient(to right, var(--marlins-blue), var(--marlins-orange));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero p {
            font-size: 1.5rem;
            max-width: 800px;
            margin: 0 auto;
            color: var(--marlins-gray);
        }

        .cta-buttons {
            margin-top: 2rem;
        }

        .btn {
            display: inline-block;
            padding: 1rem 2rem;
            margin: 0 1rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            text-transform: uppercase;
            letter-spacing: 1px;
            font-size: 14px;
        }

        .btn-primary {
            background: var(--marlins-blue);
            color: white;
            border: 2px solid var(--marlins-blue);
        }

        .btn-primary:hover {
            background: transparent;
            color: var(--marlins-blue);
        }

        .btn-secondary {
            background: transparent;
            color: var(--marlins-orange);
            border: 2px solid var(--marlins-orange);
        }

        .btn-secondary:hover {
            background: var(--marlins-orange);
            color: white;
        }

        /* Main Content */
        .section {
            padding: 5rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section h2 {
            text-align: center;
            margin-bottom: 3rem;
            font-size: 2.5rem;
            color: var(--marlins-black);
            text-transform: uppercase;
            position: relative;
        }

        .section h2:after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: var(--marlins-orange);
            border-radius: 2px;
        }

        .dark {
            background: linear-gradient(rgba(0,0,0,0.9), rgba(0,0,0,0.9)), url('https://images.unsplash.com/photo-1593079831268-3381b0db4a77?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1920&q=80') center/cover;
            color: white;
        }

        .dark h2 {
            color: white;
        }

        /* Donation Styles */
        .donation-options {
            display: flex;
            gap: 2rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .donation-card {
            background: white;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            padding: 2rem;
            width: 100%;
            max-width: 400px;
            text-align: center;
            transition: transform 0.3s ease;
            border-top: 5px solid var(--marlins-blue);
        }

        .donation-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0,0,0,0.15);
        }

        .donate-btn {
            background: var(--marlins-blue);
            color: white;
            border: none;
            padding: 0.8rem 1.5rem;
            margin: 0.5rem;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
            transition: background 0.3s;
            width: 100px;
        }

        .donate-btn:hover {
            background: #0080a8;
        }

        .custom-donate {
            margin-top: 1.5rem;
        }

        .custom-donate input {
            padding: 0.8rem;
            width: 150px;
            border: 1px solid #ddd;
            border-radius: 5px;
            margin-right: 0.5rem;
            text-align: center;
            font-weight: bold;
        }

        /* Membership Styles */
        .tiers {
            display: flex;
            justify-content: center;
            gap: 2rem;
            flex-wrap: wrap;
        }

        .tier {
            background: white;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            padding: 2rem;
            width: 100%;
            max-width: 350px;
            text-align: center;
            position: relative;
            transition: transform 0.3s ease;
            border-top: 5px solid var(--marlins-gray);
        }

        .tier.featured {
            border-top: 5px solid var(--marlins-orange);
            transform: scale(1.05);
            box-shadow: 0 15px 40px rgba(0,0,0,0.2);
        }

        .tier:hover {
            transform: translateY(-10px);
        }

        .tier.featured:hover {
            transform: scale(1.05) translateY(-10px);
        }

        .tier h3 {
            font-size: 1.8rem;
            margin-bottom: 1rem;
            color: var(--marlins-black);
        }

        .price {
            font-size: 2.5rem;
            color: var(--marlins-blue);
            margin: 1rem 0;
            font-weight: 800;
        }

        .price span {
            font-size: 1rem;
            color: var(--marlins-gray);
            font-weight: normal;
        }

        .tier ul {
            list-style: none;
            margin: 2rem 0;
            text-align: left;
        }

        .tier ul li {
            margin-bottom: 0.8rem;
            display: flex;
            align-items: center;
            padding: 0.5rem 0;
            border-bottom: 1px dashed #eee;
        }

        .tier ul li i {
            color: var(--marlins-orange);
            margin-right: 0.5rem;
            font-size: 1.2rem;
        }

        .join-btn {
            background: var(--marlins-blue);
            color: white;
            border: none;
            padding: 1rem 2rem;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
            width: 100%;
            transition: background 0.3s;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .join-btn:hover {
            background: #0080a8;
        }

        .tier.featured .join-btn {
            background: var(--marlins-orange);
        }

        .tier.featured .join-btn:hover {
            background: #d1386e;
        }

        /* Live Matches */
        .match-container {
            display: flex;
            gap: 2rem;
            flex-wrap: wrap;
        }

        .upcoming, .live-now {
            flex: 1;
            min-width: 300px;
        }

        .match-card {
            background: rgba(255,255,255,0.1);
            padding: 1.5rem;
            border-radius: 10px;
            margin-bottom: 1rem;
            text-align: center;
            border: 1px solid rgba(255,255,255,0.2);
        }

        .match-card h4 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: var(--marlins-orange);
        }

        .match-card p {
            margin: 0.5rem 0;
        }

        .video-placeholder {
            background: rgba(0,0,0,0.2);
            height: 300px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            border-radius: 10px;
            position: relative;
            overflow: hidden;
            border: 2px solid var(--marlins-blue);
        }

        .video-placeholder i {
            font-size: 5rem;
            margin-bottom: 1rem;
            opacity: 0.3;
            color: var(--marlins-blue);
        }

        .members-only {
            background: rgba(0,0,0,0.7);
            padding: 1rem;
            border-radius: 5px;
            text-align: center;
            margin-top: 1rem;
        }

        .upgrade-btn {
            background: var(--marlins-orange);
            color: white;
            border: none;
            padding: 0.5rem 1rem;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 0.5rem;
            font-weight: bold;
        }

        .team-badge {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 2rem;
            margin: 1.5rem 0;
        }

        .team {
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .team-logo {
            width: 80px;
            height: 80px;
            background: var(--light);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            font-weight: bold;
            margin-bottom: 0.5rem;
            border: 3px solid var(--marlins-blue);
        }

        /* Meet & Greet */
        .booking-system {
            display: flex;
            gap: 3rem;
            flex-wrap: wrap;
        }

        .calendar, .booking-details {
            flex: 1;
            min-width: 300px;
        }

        #date-picker {
            height: 300px;
            background: white;
            border-radius: 10px;
            padding: 1rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
        }

        #date-picker i {
            font-size: 4rem;
            color: var(--marlins-gray);
            margin-bottom: 1rem;
        }

        .booking-details {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .booking-details p {
            margin: 1rem 0;
        }

        #booking-form input, 
        #booking-form textarea {
            width: 100%;
            padding: 0.8rem;
            margin-bottom: 1rem;
            border: 1px solid #ddd;
            border-radius: 5px;
        }

        #booking-form button {
            background: var(--marlins-orange);
            color: white;
            border: none;
            padding: 1rem;
            width: 100%;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: background 0.3s;
        }

        #booking-form button:hover {
            background: #d1386e;
        }

        .price-tag {
            font-size: 2rem;
            color: var(--marlins-blue);
            font-weight: 800;
            margin: 1rem 0;
        }

        /* Footer */
        footer {
            background: var(--marlins-black);
            color: white;
            text-align: center;
            padding: 3rem 2rem 2rem;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            gap: 2rem;
            text-align: left;
        }

        .footer-section {
            flex: 1;
            min-width: 250px;
        }

        .footer-section h3 {
            color: var(--marlins-blue);
            margin-bottom: 1.5rem;
            position: relative;
            padding-bottom: 0.5rem;
        }

        .footer-section h3:after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 50px;
            height: 3px;
            background: var(--marlins-orange);
        }

        .footer-section p {
            margin: 1rem 0;
            color: var(--marlins-gray);
        }

        .social {
            display: flex;
            gap: 1rem;
            margin-top: 1rem;
        }

        .social a {
            display: inline-block;
            width: 40px;
            height: 40px;
            background: rgba(255,255,255,0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--marlins-blue);
            transition: all 0.3s;
        }

        .social a:hover {
            background: var(--marlins-blue);
            color: white;
            transform: translateY(-5px);
        }

        .copyright {
            margin-top: 3rem;
            padding-top: 2rem;
            border-top: 1px solid rgba(255,255,255,0.1);
            color: var(--marlins-gray);
            font-size: 0.9rem;
        }

        @media (max-width: 768px) {
            .top-bar {
                flex-direction: column;
                padding: 1rem;
            }
            
            nav ul {
                margin-top: 1rem;
                flex-wrap: wrap;
                justify-content: center;
            }
            
            nav ul li {
                margin: 0.5rem;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .btn {
                display: block;
                margin: 1rem auto;
                max-width: 250px;
            }
            
            .section {
                padding: 3rem 1rem;
            }
            
            .section h2 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="header-content">
            <div class="top-bar">
                <div class="logo-container">
                    <div class="logo">
                        <div class="logo-circle">
                            <div class="baseball-seams"></div>
                            <div class="letter-k">K</div>
                            <div class="marlins-teal"></div>
                            <div class="marlins-orange"></div>
                            <div class="marlins-black"></div>
                        </div>
                        <div class="logo-text">
                            <span class="text-main">KAPLER</span>
                            <span class="text-sub">CONNECT</span>
                        </div>
                    </div>
                </div>
                <nav>
                    <ul>
                        <li><a href="#donate">Donate</a></li>
                        <li><a href="#membership">Membership</a></li>
                        <li><a href="#live">Live Matches</a></li>
                        <li><a href="#meet">Meet & Greet</a></li>
                        <li><a href="#"><i class="fas fa-user"></i> Login</a></li>
                    </ul>
                </nav>
            </div>
            <div class="hero">
                <h1>Gabe Kapler Official Hub</h1>
                <p>Former MLB Manager • Miami Marlins • Baseball Leadership</p>
                <div class="cta-buttons">
                    <a href="#membership" class="btn btn-primary">Join VIP Club</a>
                    <a href="#meet" class="btn btn-secondary">Book Meet & Greet</a>
                </div>
            </div>
        </div>
    </header>

    <!-- Donation Section -->
    <section id="donate" class="section">
        <h2>Support Our Mission</h2>
        <div class="donation-options">
            <div class="donation-card">
                <h3>One-Time Donation</h3>
                <p>Support youth baseball programs</p>
                <div class="donation-buttons">
                    <button class="donate-btn" data-amount="25">$25</button>
                    <button class="donate-btn" data-amount="50">$50</button>
                    <button class="donate-btn" data-amount="100">$100</button>
                </div>
                <div class="custom-donate">
                    <input type="number" placeholder="Other amount" id="custom-amount">
                    <button class="donate-btn">Donate</button>
                </div>
            </div>
            <div class="donation-card">
                <h3>Recurring Support</h3>
                <p>Become a monthly supporter</p>
                <select id="recurring-options" style="width: 100%; padding: 0.8rem; margin: 1.5rem 0; border-radius: 5px; border: 1px solid #ddd;">
                    <option value="10">$10/month</option>
                    <option value="25">$25/month</option>
                    <option value="50">$50/month</option>
                </select>
                <button class="join-btn" id="recurring-donate">Subscribe</button>
            </div>
        </div>
    </section>

    <!-- Membership Section -->
    <section id="membership" class="section">
        <h2>Premium Membership</h2>
        <div class="tiers">
            <div class="tier">
                <h3>Fan Club</h3>
                <p class="price">$9.99<span>/month</span></p>
                <ul>
                    <li><i class="fas fa-check"></i> Exclusive Content & Articles</li>
                    <li><i class="fas fa-check"></i> Monthly Newsletter</li>
                    <li><i class="fas fa-check"></i> Access to Fan Community</li>
                    <li><i class="fas fa-check"></i> 10% Discount on Merch</li>
                    <li><i class="fas fa-check"></i> Early Event Notifications</li>
                </ul>
                <button class="join-btn">Join Now</button>
            </div>
            <div class="tier featured">
                <h3>VIP Access</h3>
                <p class="price">$29.99<span>/month</span></p>
                <ul>
                    <li><i class="fas fa-check"></i> All Fan Club Benefits</li>
                    <li><i class="fas fa-check"></i> Live Match Streaming Access</li>
                    <li><i class="fas fa-check"></i> Priority Meet & Greet Booking</li>
                    <li><i class="fas fa-check"></i> Exclusive Merch Package</li>
                    <li><i class="fas fa-check"></i> Signed Memorabilia Opportunity</li>
                    <li><i class="fas fa-check"></i> Monthly Q&A Sessions</li>
                </ul>
                <button class="join-btn">Join VIP</button>
            </div>
        </div>
    </section>

    <!-- Live Matches -->
    <section id="live" class="section dark">
        <h2>Live Match Center</h2>
        <div class="match-container">
            <div class="upcoming">
                <h3>Upcoming Games</h3>
                <div class="match-card">
                    <h4>Marlins vs Phillies</h4>
                    <p>August 15 • 7:10 PM EST</p>
                    <p>LoanDepot Park, Miami</p>
                    <div class="team-badge">
                        <div class="team">
                            <div class="team-logo" style="background: #00A3E0; color: white;">M</div>
                            <span>Marlins</span>
                        </div>
                        <span>VS</span>
                        <div class="team">
                            <div class="team-logo" style="background: #E81828; color: white;">P</div>
                            <span>Phillies</span>
                        </div>
                    </div>
                    <button class="upgrade-btn">Set Reminder</button>
                </div>
                <div class="match-card">
                    <h4>Marlins vs Braves</h4>
                    <p>August 17 • 6:40 PM EST</p>
                    <p>LoanDepot Park, Miami</p>
                    <div class="team-badge">
                        <div class="team">
                            <div class="team-logo" style="background: #00A3E0; color: white;">M</div>
                            <span>Marlins</span>
                        </div>
                        <span>VS</span>
                        <div class="team">
                            <div class="team-logo" style="background: #CE1141; color: white;">B</div>
                            <span>Braves</span>
                        </div>
                    </div>
                    <button class="upgrade-btn">Set Reminder</button>
                </div>
            </div>
            <div class="live-now">
                <h3>Live Now</h3>
                <div class="video-placeholder">
                    <i class="fas fa-baseball-ball"></i>
                    <p>LIVE STREAM WILL APPEAR HERE</p>
                    <div class="members-only">
                        <p>VIP Members Only</p>
                        <button class="upgrade-btn">Upgrade to Watch</button>
                    </div>
                </div>
                <div class="email-signup" style="margin-top: 2rem; text-align: center;">
                    <h4>Get Game Reminders</h4>
                    <div style="display: flex; margin-top: 1rem;">
                        <input type="email" id="reminder-email" placeholder="Your email" style="flex: 1; padding: 0.8rem; border-radius: 5px 0 0 5px; border: 1px solid #ddd; border-right: none;">
                        <button id="reminder-submit" style="background: var(--marlins-orange); color: white; border: none; padding: 0 1.5rem; border-radius: 0 5px 5px 0; cursor: pointer;">Notify Me</button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Meet & Greet -->
    <section id="meet" class="section">
        <h2>Meet Gabe Kapler</h2>
        <div class="booking-system">
            <div class="calendar">
                <div id="date-picker">
                    <i class="far fa-calendar-alt"></i>
                    <h3>Schedule Your Session</h3>
                    <p>Select an available date from the calendar</p>
                    <p>30-minute virtual meet & greet</p>
                </div>
            </div>
            <div class="booking-details">
                <h3>Booking Details</h3>
                <p>Personal 30-minute virtual session with Gabe Kapler</p>
                <p>Ask questions, get advice, or just chat baseball!</p>
                <div class="price-tag">$249</div>
                <form id="booking-form">
                    <input type="text" placeholder="Your Full Name" required>
                    <input type="email" placeholder="Email Address" required>
                    <input type="tel" placeholder="Phone Number">
                    <textarea placeholder="Special requests or questions..." rows="3"></textarea>
                    <button type="submit">Book Now</button>
                </form>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-content">
            <div class="footer-section">
                <h3>About KapConnect</h3>
                <p>Official platform for fans of Gabe Kapler, former MLB manager and baseball analyst. Join our community for exclusive content, live events, and more.</p>
                <div class="social">
                    <a href="#"><i class="fab fa-twitter"></i></a>
                    <a href="#"><i class="fab fa-instagram"></i></a>
                    <a href="#"><i class="fab fa-facebook-f"></i></a>
                    <a href="#"><i class="fab fa-youtube"></i></a>
                </div>
            </div>
            <div class="footer-section">
                <h3>Quick Links</h3>
                <p><a href="#donate" style="color: var(--marlins-gray); text-decoration: none;">Donations</a></p>
                <p><a href="#membership" style="color: var(--marlins-gray); text-decoration: none;">Membership</a></p>
                <p><a href="#live" style="color: var(--marlins-gray); text-decoration: none;">Live Matches</a></p>
                <p><a href="#meet" style="color: var(--marlins-gray); text-decoration: none;">Meet & Greet</a></p>
                <p><a href="#" style="color: var(--marlins-gray); text-decoration: none;">FAQ</a></p>
            </div>
            <div class="footer-section">
                <h3>Contact Us</h3>
                <p><i class="fas fa-envelope"></i> contact@kapconnect.com</p>
                <p><i class="fas fa-phone"></i> (305) 555-7890</p>
                <p><i class="fas fa-map-marker-alt"></i> Miami, Florida</p>
            </div>
        </div>
        <div class="copyright">
            <p>&copy; 2023 KapConnect. All rights reserved. This site is not affiliated with the Miami Marlins or MLB.</p>
        </div>
    </footer>

    <script>
        // Simple functionality for demo purposes
        document.addEventListener('DOMContentLoaded', () => {
            // Donation buttons
            const donateBtns = document.querySelectorAll('.donate-btn');
            donateBtns.forEach(btn => {
                btn.addEventListener('click', () => {
                    let amount = btn.getAttribute('data-amount');
                    if(!amount) {
                        amount = document.getElementById('custom-amount').value || '25';
                    }
                    alert(`Thank you for your $${amount} donation! You will be redirected to our secure payment page.`);
                });
            });

            // Membership join buttons
            const joinBtns = document.querySelectorAll('.join-btn');
            joinBtns.forEach(btn => {
                btn.addEventListener('click', () => {
                    const tier = btn.closest('.tier').querySelector('h3').textContent;
                    alert(`Redirecting to ${tier} signup page`);
                });
            });

            // Booking form
            const bookingForm = document.getElementById('booking-form');
            bookingForm.addEventListener('submit', (e) => {
                e.preventDefault();
                alert('Meet & Greet request submitted! You will receive confirmation shortly.');
                bookingForm.reset();
            });

            // Email reminder
            document.getElementById('reminder-submit').addEventListener('click', () => {
                const email = document.getElementById('reminder-email').value;
                if(email) {
                    alert(`Thank you! We'll send game reminders to ${email}`);
                } else {
                    alert('Please enter a valid email address');
                }
            });
        });
    </script>
</body>
</html>