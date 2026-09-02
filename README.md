<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dhruv • Designer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Helvetica Neue', sans-serif;
            background: #ffffff;
            color: #1a1a1a;
            line-height: 1.6;
            letter-spacing: -0.3px;
        }

        @media (prefers-reduced-motion: reduce) {
            * {
                animation-duration: 0.01ms !important;
                animation-iteration-count: 1 !important;
                transition-duration: 0.01ms !important;
            }
        }

        /* Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }

        @keyframes subtleGlow {
            0%, 100% {
                text-shadow: 0 0 0 rgba(26, 26, 26, 0);
            }
            50% {
                text-shadow: 0 0 8px rgba(26, 26, 26, 0.08);
            }
        }

        /* Container */
        .container {
            max-width: 700px;
            margin: 0 auto;
            padding: 60px 40px;
        }

        @media (max-width: 640px) {
            .container {
                padding: 40px 24px;
            }
        }

        /* Hero Section */
        .hero {
            margin-bottom: 80px;
            animation: fadeInUp 0.8s ease-out;
        }

        .name {
            font-size: 3.5rem;
            font-weight: 700;
            line-height: 1.1;
            margin-bottom: 12px;
            letter-spacing: -1.5px;
        }

        @media (max-width: 640px) {
            .name {
                font-size: 2.5rem;
            }
        }

        .location {
            font-size: 0.95rem;
            color: #666;
            margin-bottom: 32px;
            letter-spacing: 0.5px;
        }

        .tagline {
            font-size: 1.1rem;
            color: #2a2a2a;
            font-weight: 500;
            margin-bottom: 20px;
            letter-spacing: -0.2px;
        }

        .intro-text {
            font-size: 0.95rem;
            color: #555;
            line-height: 1.8;
            margin-bottom: 12px;
        }

        .intro-text:last-child {
            margin-bottom: 0;
        }

        /* Divider */
        .divider {
            width: 32px;
            height: 1px;
            background: #ddd;
            margin: 60px 0;
            animation: fadeIn 1s ease-out 0.3s both;
        }

        /* Section */
        .section {
            margin-bottom: 60px;
            animation: fadeInUp 0.8s ease-out both;
        }

        .section:nth-child(4) {
            animation-delay: 0.2s;
        }

        .section:nth-child(5) {
            animation-delay: 0.4s;
        }

        .section-title {
            font-size: 0.85rem;
            font-weight: 700;
            color: #1a1a1a;
            text-transform: uppercase;
            letter-spacing: 1.2px;
            margin-bottom: 20px;
            display: block;
        }

        /* Focus Areas */
        .focus-list {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 16px;
        }

        @media (max-width: 640px) {
            .focus-list {
                grid-template-columns: 1fr;
            }
        }

        .focus-item {
            padding: 16px 20px;
            background: #fafafa;
            border: 1px solid #efefef;
            border-radius: 4px;
            font-size: 0.9rem;
            color: #333;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .focus-item:hover {
            background: #f5f5f5;
            border-color: #ddd;
            transform: translateY(-2px);
        }

        /* Approach */
        .approach-item {
            padding-bottom: 24px;
            margin-bottom: 24px;
            border-bottom: 1px solid #efefef;
        }

        .approach-item:last-child {
            border-bottom: none;
            margin-bottom: 0;
            padding-bottom: 0;
        }

        .approach-label {
            font-size: 0.8rem;
            color: #999;
            text-transform: uppercase;
            letter-spacing: 0.8px;
            margin-bottom: 8px;
            display: block;
        }

        .approach-text {
            font-size: 0.95rem;
            color: #2a2a2a;
            line-height: 1.7;
        }

        /* Links */
        .links {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            align-items: center;
        }

        .link-item {
            display: inline-flex;
            align-items: center;
            gap: 6px;
            padding: 10px 16px;
            background: #f5f5f5;
            border: 1px solid #e0e0e0;
            border-radius: 4px;
            text-decoration: none;
            color: #1a1a1a;
            font-size: 0.9rem;
            font-weight: 500;
            transition: all 0.3s ease;
        }

        .link-item:hover {
            background: #efefef;
            border-color: #ccc;
            transform: translateY(-2px);
        }

        .link-item::after {
            content: '→';
            font-size: 0.8em;
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .link-item:hover::after {
            opacity: 1;
        }

        /* Footer */
        .footer {
            margin-top: 80px;
            padding-top: 40px;
            border-top: 1px solid #efefef;
            font-size: 0.8rem;
            color: #999;
            text-align: center;
            animation: fadeIn 1s ease-out 0.6s both;
        }

        /* Accent hover effect */
        .accent-word {
            position: relative;
            color: #1a1a1a;
            transition: color 0.3s ease;
        }

        .accent-word:hover {
            color: #666;
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Hero -->
        <section class="hero">
            <h1 class="name">Dhruv</h1>
            <p class="location">Jaipur, India</p>
            <p class="tagline">Designer · Thinker · Vibe Coder</p>
            <p class="intro-text">I design things, break things, and occasionally make them work.</p>
            <p class="intro-text">I explore the space between design, technology, and interaction—where an idea meets the possibility of real experience.</p>
        </section>

        <div class="divider"></div>

        <!-- What I Do -->
        <section class="section">
            <span class="section-title">Focus Areas</span>
            <div class="focus-list">
                <div class="focus-item">UI/UX Design</div>
                <div class="focus-item">Visual Design</div>
                <div class="focus-item">Creative Coding</div>
                <div class="focus-item">Spatial Experiences</div>
                <div class="focus-item">Interaction Design</div>
                <div class="focus-item">Prototyping</div>
            </div>
        </section>

        <!-- Approach -->
        <section class="section">
            <span class="section-title">My Approach</span>
            
            <div class="approach-item">
                <span class="approach-label">Philosophy</span>
                <p class="approach-text">I don't think of myself as a developer. I think of myself as someone who builds enough to turn an idea into something people can actually experience.</p>
            </div>

            <div class="approach-item">
                <span class="approach-label">Process</span>
                <p class="approach-text">I work intuitively, exploring and iterating. I let ideas evolve as I build them. There's something powerful about discovering the shape of a thing by making it.</p>
            </div>

            <div class="approach-item">
                <span class="approach-label">What Excites Me</span>
                <p class="approach-text">Problems that sit at the intersection of aesthetics, function, and human behavior. Any project interesting enough to become briefly obsessed with.</p>
            </div>
        </section>

        <!-- Connect -->
        <section class="section">
            <span class="section-title">Let's Connect</span>
            <div class="links">
                <a href="https://twitter.com" class="link-item">Twitter</a>
                <a href="https://dribbble.com" class="link-item">Dribbble</a>
                <a href="mailto:your-email@example.com" class="link-item">Email</a>
            </div>
        </section>

        <!-- Footer -->
        <footer class="footer">
            <p>Currently exploring design systems and interactive experiences</p>
        </footer>
    </div>
</body>
</html>
