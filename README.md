# Cole-Landing-Page
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>How 6-7 Figure Entrepreneurs Scale to 8-Figures Without Hiring Another Bad Sales Rep</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html, body {
            overflow-x: hidden;
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #0f0f23 0%, #1a1a2e 50%, #16213e 100%);
        }

        .container {
            width: 100%;
            max-width: 800px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, #0f0f23 0%, #1a1a2e 50%, #16213e 100%);
            color: white;
            padding: 60px 0;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><radialGradient id="grad1" cx="50%" cy="50%" r="50%"><stop offset="0%" style="stop-color:rgba(255,255,255,0.1);stop-opacity:1" /><stop offset="100%" style="stop-color:rgba(255,255,255,0);stop-opacity:0" /></radialGradient></defs><circle cx="20" cy="20" r="2" fill="rgba(255,255,255,0.3)"/><circle cx="80" cy="40" r="1" fill="rgba(255,255,255,0.2)"/><circle cx="40" cy="80" r="1.5" fill="rgba(255,255,255,0.25)"/></svg>') repeat;
            animation: float 20s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(180deg); }
        }

        .preheader {
            font-size: 14px;
            color: #ff6b35;
            font-weight: bold;
            letter-spacing: 1px;
            text-transform: uppercase;
            margin-bottom: 20px;
            animation: slideDown 0.8s ease-out;
        }

        @keyframes slideDown {
            from { opacity: 0; transform: translateY(-30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .hero h1 {
            font-size: clamp(28px, 5vw, 48px);
            font-weight: bold;
            margin-bottom: 20px;
            line-height: 1.2;
            animation: slideUp 0.8s ease-out 0.2s both;
        }

        @keyframes slideUp {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .hero .subheader {
            font-size: clamp(16px, 3vw, 24px);
            margin-bottom: 40px;
            color: #e0e0e0;
            animation: fadeIn 0.8s ease-out 0.4s both;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        .vsl-container {
            margin: 40px 0;
            animation: scaleIn 0.8s ease-out 0.6s both;
            position: relative;
            z-index: 2;
        }

        @keyframes scaleIn {
            from { opacity: 0; transform: scale(0.8); }
            to { opacity: 1; transform: scale(1); }
        }

        .vsl-icon {
            display: inline-block;
            width: 200px;
            height: 120px;
            background: linear-gradient(135deg, #ff6b35, #f7931e);
            border-radius: 15px;
            position: relative;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 10px 30px rgba(255, 107, 53, 0.3);
            text-decoration: none;
            color: white;
        }

        .vsl-icon:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 40px rgba(255, 107, 53, 0.4);
        }

        .play-button {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 0;
            height: 0;
            border-left: 20px solid white;
            border-top: 12px solid transparent;
            border-bottom: 12px solid transparent;
            margin-left: 3px;
        }

        .vsl-text {
            display: block;
            margin-top: 15px;
            font-size: 16px;
            font-weight: bold;
            color: white;
        }

        .cta-primary {
            background: linear-gradient(135deg, #ff6b35, #f7931e);
            color: white;
            padding: 18px 40px;
            font-size: 20px;
            font-weight: bold;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
            text-transform: uppercase;
            letter-spacing: 1px;
            box-shadow: 0 10px 30px rgba(255, 107, 53, 0.3);
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% { box-shadow: 0 10px 30px rgba(255, 107, 53, 0.3); }
            50% { box-shadow: 0 10px 40px rgba(255, 107, 53, 0.5); }
            100% { box-shadow: 0 10px 30px rgba(255, 107, 53, 0.3); }
        }

        .cta-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 35px rgba(255, 107, 53, 0.5);
        }

        /* Section Styles */
        .section {
            padding: 80px 0;
            position: relative;
        }

        .section:nth-child(even) {
            background: #f8f9fa;
        }

        .section:nth-child(odd) {
            background: white;
        }

        .section h2 {
            font-size: clamp(24px, 4vw, 36px);
            margin-bottom: 30px;
            color: #1a1a2e;
            text-align: center;
            position: relative;
        }

        .section h2::after {
            content: '';
            display: block;
            width: 60px;
            height: 4px;
            background: linear-gradient(90deg, #ff6b35, #f7931e);
            margin: 20px auto;
            border-radius: 2px;
        }

        .section p {
            font-size: clamp(16px, 2.5vw, 20px);
            margin-bottom: 20px;
            line-height: 1.8;
        }

        .highlight {
            background: linear-gradient(120deg, #ff6b35 0%, #f7931e 100%);
            background-clip: text;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-weight: bold;
        }

        .bold {
            font-weight: bold;
            color: #1a1a2e;
        }

        .italic {
            font-style: italic;
        }

        /* Bullets */
        .bullets {
            list-style: none;
            margin: 30px 0;
        }

        .bullets li {
            padding: 15px 0;
            border-bottom: 1px solid #eee;
            font-size: 18px;
            line-height: 1.6;
            position: relative;
            padding-left: 30px;
        }

        .bullets li::before {
            content: '✓';
            position: absolute;
            left: 0;
            color: #ff6b35;
            font-weight: bold;
            font-size: 20px;
        }

        /* FAQ Section */
        .faq-item {
            background: white;
            margin-bottom: 20px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            overflow: hidden;
            transition: all 0.3s ease;
        }

        .faq-item:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.15);
        }

        .faq-question {
            padding: 25px;
            background: linear-gradient(135deg, #1a1a2e, #16213e);
            color: white;
            cursor: pointer;
            font-weight: bold;
            font-size: 18px;
        }

        .faq-answer {
            padding: 25px;
            font-size: 16px;
            line-height: 1.6;
        }

        /* Responsive Design */
        @media (max-width: 1024px) {
            .container {
                padding: 0 15px;
            }
            .section {
                padding: 60px 0;
            }
        }

        @media (max-width: 768px) {
            .hero {
                padding: 40px 0;
            }
            
            .section {
                padding: 40px 0;
            }
            
            .vsl-icon {
                width: 160px;
                height: 100px;
            }
            
            .cta-primary {
                padding: 15px 30px;
                font-size: 18px;
            }
            
            .section p {
                margin-bottom: 15px;
            }
        }

        /* Smooth scroll behavior */
        html {
            scroll-behavior: smooth;
        }

        /* Entrance animations */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.8s ease;
        }

        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>
    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <div class="preheader">For 6-7 Figure Entrepreneurs Ready to Scale</div>
            
            <h1>How to Scale from 7 to 8-Figures in 24 Months Without Wasting Another Dollar on Bad Sales Reps</h1>
            
            <div class="subheader">
                Finally... a proven system that installs predictable lead-gen, recruits high-performing sales teams, and provides 8-figure boardroom consulting — so you can scale without the hiring nightmare.
            </div>
            
            <div class="vsl-container">
                <a href="https://docs.google.com/document/d/1ARqL6E54Aa3g2Au_XkBj9v3bY_t3q5OeH978D9TUq8g/edit?usp=sharing" class="vsl-icon">
                    <div class="play-button"></div>
                </a>
                <span class="vsl-text">Click Here To See The: VSL I WROTE FOR YOU</span>
            </div>
            
            <button class="cta-primary" onclick="window.open('https://docs.google.com/document/d/1ARqL6E54Aa3g2Au_XkBj9v3bY_t3q5OeH978D9TUq8g/edit?usp=sharing', '_blank')">
                Book Your Strategy Call Now
            </button>
        </div>
    </section>

    <!-- Problem Identification -->
    <section class="section fade-in">
        <div class="container">
            <h2>Why 97% of 7-Figure Entrepreneurs Never Break the 8-Figure Ceiling</h2>
            
            <p>You're already successful...</p>
            
            <p>You've built a <span class="bold">6 or 7-figure business</span> that most people only dream about.</p>
            
            <p>But here's what keeps you up at night...</p>
            
            <p>Your revenue is a <span class="highlight">rollercoaster</span>. One month you're celebrating record numbers. The next month, you're wondering where all your leads went.</p>
            
            <p>You've tried hiring salespeople...</p>
            
            <p>You've wasted <span class="bold">months</span> recruiting. Spent <span class="bold">thousands</span> on training. Only to watch them burn through your leads without closing deals.</p>
            
            <p>You've bought into marketing "gurus" promising endless leads...</p>
            
            <p>But leads without a system to convert them are just <span class="italic">expensive names in your CRM</span>.</p>
            
            <p>Meanwhile, your competitors with <span class="bold">inferior products</span> are scaling past you because they figured out something you haven't...</p>
            
            <p>The <span class="highlight">8-figure entrepreneurs</span> don't just have better products. They have <span class="bold">better systems</span>.</p>
            
            <p>And if you keep doing what you're doing now...</p>
            
            <p>Six months from now, you'll still be stuck in the same place, watching others pass you by while you're trapped in the <span class="bold">"7-figure ceiling."</span></p>
            
            <p>But what if I told you there's a way to break through that ceiling...</p>
            
            <p>What if you could <span class="bold">predictably scale to 8-figures</span> using the same systems that work for Tony Robbins and Dean Graziosi?</p>
        </div>
    </section>

    <!-- Origin Story -->
    <section class="section fade-in">
        <div class="container">
            <h2>How We Went from "Sales Training Experts" to the Secret Weapon Behind Multiple 8-Figure Companies</h2>
            
            <p>Three years ago, we were just another sales training company...</p>
            
            <p>We'd teach entrepreneurs how to "close better." How to "handle objections." How to "follow up with prospects."</p>
            
            <p>And our clients would get <span class="italic">temporary</span> bumps in revenue.</p>
            
            <p>But then something would always happen...</p>
            
            <p>Their lead flow would dry up. Their sales reps would quit. Their systems would fall apart.</p>
            
            <p>They'd come back to us, frustrated: <span class="bold">"Your training worked... but now what?"</span></p>
            
            <p>That's when we realized the problem...</p>
            
            <p>Everyone was treating sales like an <span class="bold">isolated skill</span> instead of part of a <span class="bold">complete business system</span>.</p>
            
            <p>So we did something different...</p>
            
            <p>We started studying the entrepreneurs who <span class="highlight">consistently</span> scaled from 7 to 8 figures. Not the ones who got lucky. The ones who did it <span class="bold">repeatedly</span>.</p>
            
            <p>Here's what we found:</p>
            
            <p>They didn't just focus on sales. They built <span class="bold">three interconnected systems</span>:</p>
            
            <p><span class="bold">1. Predictable Lead Generation</span> — Internal systems that generate qualified prospects on demand</p>
            
            <p><span class="bold">2. High-Performing Sales Teams</span> — Recruiting, training, and managing reps who actually hit KPIs</p>
            
            <p><span class="bold">3. Strategic Business Consulting</span> — Boardroom-level guidance to optimize the entire operation</p>
            
            <p>When we started installing all three systems for our clients...</p>
            
            <p>Magic happened.</p>
            
            <p>No... not magic. <span class="bold">Predictable results</span>.</p>
        </div>
    </section>

    <!-- Solution Revelation -->
    <section class="section fade-in">
        <div class="container">
            <h2>The 3-Pillar Scale System That Consistently Breaks 7-Figure Entrepreneurs Into 8-Figures</h2>
            
            <p>Here's exactly how it works:</p>
            
            <p><span class="bold">PILLAR 1: Internal Lead Generation Systems</span></p>
            
            <p>Instead of depending on expensive ads that stop working overnight...</p>
            
            <p>We install <span class="highlight">internal lead-gen systems</span> that generate qualified prospects from your existing network, referrals, and strategic partnerships.</p>
            
            <p>This means <span class="bold">predictable pipeline</span> that doesn't disappear when Facebook changes their algorithm.</p>
            
            <p><span class="bold">PILLAR 2: Sales Team Recruiting & Ramping</span></p>
            
            <p>Instead of hoping your next hire will be "the one..."</p>
            
            <p>We use our proven recruiting system to find sales reps who already have the skills and mindset to succeed in <span class="bold">your specific business model</span>.</p>
            
            <p>Then we ramp them to KPIs using the same training frameworks that work for <span class="bold">2,000+ brands</span>.</p>
            
            <p><span class="bold">PILLAR 3: 8-Figure Boardroom Consulting</span></p>
            
            <p>Instead of getting generic advice from masterminds full of 6-figure entrepreneurs...</p>
            
            <p>You get direct access to strategies being used by companies doing <span class="highlight">$30M+ per year</span>.</p>
            
            <p>Operations. Systems. Team management. Financial optimization.</p>
            
            <p>The kind of insight you can only get when you're in the room with people who've already built what you're trying to build.</p>
            
            <p>Here's what happens when all three pillars work together:</p>
            
            <p>Month 1-3: Your lead flow stabilizes. No more feast or famine.</p>
            
            <p>Month 4-8: Your new sales reps start hitting KPIs. Revenue becomes predictable.</p>
            
            <p>Month 9-18: You implement advanced systems. Operations run without you.</p>
            
            <p>Month 12-24: You break through 8-figures with a business that scales itself.</p>
            
            <p>This isn't theory. It's the exact system we've used with <span class="bold">multiple companies</span> to scale to <span class="highlight">$30M+ in under two years</span>.</p>
        </div>
    </section>

    <!-- Product Introduction -->
    <section class="section fade-in">
        <div class="container">
            <h2>Introducing Closers.io: The Complete Scale-to-8-Figures System</h2>
            
            <p>This isn't just another course or coaching program...</p>
            
            <p>Closers.io is the <span class="bold">complete business scaling system</span> used by the entrepreneurs you see on stage at major events.</p>
            
            <p>Here's what you get:</p>
            
            <ul class="bullets">
                <li><span class="bold">Lead Generation System Installation:</span> We build and install internal lead-gen systems so you never depend on paid ads again → You wake up to qualified prospects in your pipeline → You become the entrepreneur who never worries about "where the next client will come from"</li>
                
                <li><span class="bold">Sales Rep Recruiting & Training:</span> We find, vet, and train sales reps specifically for your business model → Your team consistently hits KPIs without constant micromanaging → You become the leader of a high-performing sales organization</li>
                
                <li><span class="bold">8-Figure Boardroom Mastermind:</span> Direct access to strategies used by $30M+ companies → You implement systems that work at scale → You become the entrepreneur operating at the highest level of business</li>
                
                <li><span class="bold">Sales Process & Script Consulting:</span> Proven frameworks that convert prospects into high-value clients → Your close rates increase dramatically → You become known for having the best sales process in your industry</li>
                
                <li><span class="bold">KPI Tracking & Management Systems:</span> Clear metrics that show exactly what's working and what isn't → You make data-driven decisions that compound your growth → You become the entrepreneur who scales through systems, not guesswork</li>
            </ul>
            
            <p>Compare this to what you've tried before:</p>
            
            <p><span class="bold">Generic sales training:</span> Teaches you to close better, but doesn't fix your lead problem or help you hire good reps.</p>
            
            <p><span class="bold">Marketing agencies:</span> Generate leads, but can't help you convert them or scale your team.</p>
            
            <p><span class="bold">Business coaches:</span> Give you theory and motivation, but don't have the systems to scale sales operations.</p>
            
            <p>Closers.io is the <span class="highlight">only system</span> that handles all three: lead generation, sales team building, AND strategic scaling consulting.</p>
            
            <p>It's why entrepreneurs who've worked with us call it <span class="bold">"the missing piece"</span> they needed to break through 8-figures.</p>
        </div>
    </section>

    <!-- Offer Structure -->
    <section class="section fade-in">
        <div class="container">
            <h2>How to Get Started (And Why You Need to Act This Week)</h2>
            
            <p>Here's how this works:</p>
            
            <p>Step 1: Book a strategy call using the link below this video</p>
            
            <p>Step 2: We audit your current business and identify your biggest scaling bottlenecks</p>
            
            <p>Step 3: We determine if you're a fit for our lead-gen system, recruiting program, or 8-figure mastermind</p>
            
            <p>Step 4: If we're a match, we create a custom scaling plan and get started immediately</p>
            
            <p><span class="bold">Our Promise:</span></p>
            
            <p>If we take you on as a client and you don't see measurable improvement in your sales systems within the first 90 days, we'll refund every penny and give you $1,000 for wasting your time.</p>
            
            <p>We can make this guarantee because we've done this <span class="bold">2,000+ times</span> with entrepreneurs just like you.</p>
            
            <p><span class="bold">Why you need to book your call this week:</span></p>
            
            <p>We only work with a limited number of clients at a time because our system requires hands-on implementation.</p>
            
            <p>Right now, we have <span class="bold">3 spots available</span> for new clients starting in the next 30 days.</p>
            
            <p>After that, there's a waiting list until Q3.</p>
            
            <p>If you're serious about scaling to 8-figures...</p>
            
            <p>If you're tired of the revenue rollercoaster...</p>
            
            <p>If you're ready to build a business that runs without you...</p>
            
            <button class="cta-primary" onclick="window.open('https://docs.google.com/document/d/1ARqL6E54Aa3g2Au_XkBj9v3bY_t3q5OeH978D9TUq8g/edit?usp=sharing', '_blank')">
                Book Your Strategy Call Now
            </button>
        </div>
    </section>

    <!-- FAQ Section -->
    <section class="section fade-in">
        <div class="container">
            <h2>Questions Successful Entrepreneurs Ask Before Making Million-Dollar Decisions</h2>
            
            <div class="faq-item">
                <div class="faq-question">
                    "This sounds expensive. What if I can't afford it right now?"
                </div>
                <div class="faq-answer">
                    Here's the real question: Can you afford to stay where you are? If you're doing $1M-$5M annually and stay stuck at that level for another 2 years while your competitors scale to $10M+, what does that cost you? The entrepreneurs who work with us see ROI within 90 days because we're not selling you a course — we're installing systems that generate revenue immediately.
                </div>
            </div>
            
            <div class="faq-item">
                <div class="faq-question">
                    "Will this work for MY specific industry?"
                </div>
                <div class="faq-answer">
                    We've worked with 2,000+ brands across every industry you can imagine. Coaching, consulting, e-commerce, SaaS, agencies, real estate, fitness, finance... The principles of lead generation, sales team management, and business scaling are universal. What changes is the execution, and that's exactly what we customize for your business model during our strategy call.
                </div>
            </div>
            
            <div class="faq-item">
                <div class="faq-question">
                    "What if my current sales team doesn't adapt to your system?"
                </div>
                <div class="faq-answer">
                    That's exactly why we don't just train your existing team — we help you recruit and ramp NEW high-performers who are already aligned with proven systems. Your current team can stay and learn alongside the new reps, or they can find opportunities that better fit their skillset. Either way, you end up with a sales organization that actually hits KPIs.
                </div>
            </div>
            
            <div class="faq-item">
                <div class="faq-question">
                    "I'm already busy running my business. How much time will this take?"
                </div>
                <div class="faq-answer">
                    This is designed for entrepreneurs who DON'T have time to micromanage every detail. We handle the heavy lifting — recruiting, training, system installation — while you focus on the strategic decisions that only you can make. Most clients find they have MORE time after 90 days because their business starts running without constant intervention.
                </div>
            </div>
            
            <p style="text-align: center; margin-top: 50px; font-size: 18px;">
                Ready to join the entrepreneurs who've cracked the code on predictable 8-figure scaling?
            </p>
            
            <div style="text-align: center; margin-top: 30px;">
                <button class="cta-primary" onclick="window.open('https://docs.google.com/document/d/1ARqL6E54Aa3g2Au_XkBj9v3bY_t3q5OeH978D9TUq8g/edit?usp=sharing', '_blank')">
                    Book Your Strategy Call Now
                </button>
            </div>
        </div>
    </section>

    <script>
        // Smooth scrolling and entrance animations
        function isElementInViewport(el) {
            const rect = el.getBoundingClientRect();
            return (
                rect.top >= 0 &&
                rect.left >= 0 &&
                rect.bottom <= (window.innerHeight || document.documentElement.clientHeight) &&
                rect.right <= (window.innerWidth || document.documentElement.clientWidth)
            );
        }

        function handleScroll() {
            const elements = document.querySelectorAll('.fade-in');
            elements.forEach(el => {
                if (isElementInViewport(el) || window.scrollY + window.innerHeight >= el.offsetTop) {
                    el.classList.add('visible');
                }
            });
        }

        // Run on scroll and page load
        window.addEventListener('scroll', handleScroll);
        window.addEventListener('load', handleScroll);
        handleScroll(); // Run immediately

        // Add click tracking for CTAs
        document.querySelectorAll('.cta-primary, .vsl-icon').forEach(button => {
            button.addEventListener('click', function() {
                // Add any tracking code here if needed
                console.log('CTA clicked');
            });
        });
    </script>
</body>
</html>
