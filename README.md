<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sandile Nkambule - IT Technician & Developer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        .hero {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 40px;
            margin-bottom: 30px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(45deg, transparent, rgba(255, 255, 255, 0.1), transparent);
            transform: rotate(45deg);
            animation: shimmer 3s infinite;
        }

        @keyframes shimmer {
            0% { transform: translateX(-100%) translateY(-100%) rotate(45deg); }
            100% { transform: translateX(100%) translateY(100%) rotate(45deg); }
        }

        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            margin: 0 auto 20px;
            background: linear-gradient(45deg, #667eea, #764ba2);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 60px;
            color: white;
            position: relative;
            z-index: 1;
            transition: transform 0.3s ease;
        }

        .profile-img:hover {
            transform: scale(1.05);
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 10px;
            background: linear-gradient(45deg, #667eea, #764ba2);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            position: relative;
            z-index: 1;
        }

        .hero .subtitle {
            font-size: 1.2rem;
            color: #666;
            margin-bottom: 20px;
            position: relative;
            z-index: 1;
        }

        .hero .description {
            font-size: 1.1rem;
            color: #555;
            max-width: 600px;
            margin: 0 auto;
            position: relative;
            z-index: 1;
        }

        .sections {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
        }

        .section {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 30px;
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .section:hover {
            transform: translateY(-5px);
            box-shadow: 0 25px 50px rgba(0, 0, 0, 0.15);
        }

        .section h2 {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: #333;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .section-icon {
            font-size: 1.5rem;
            background: linear-gradient(45deg, #667eea, #764ba2);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
            gap: 15px;
            margin-top: 20px;
        }

        .skill-tag {
            background: linear-gradient(45deg, #667eea, #764ba2);
            color: white;
            padding: 8px 15px;
            border-radius: 25px;
            text-align: center;
            font-size: 0.9rem;
            font-weight: 500;
            transition: transform 0.2s ease;
        }

        .skill-tag:hover {
            transform: scale(1.05);
        }

        .contact-links {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
            margin-top: 20px;
        }

        .contact-link {
            display: flex;
            align-items: center;
            gap: 8px;
            padding: 12px 20px;
            background: linear-gradient(45deg, #667eea, #764ba2);
            color: white;
            text-decoration: none;
            border-radius: 25px;
            transition: transform 0.2s ease, box-shadow 0.2s ease;
            font-weight: 500;
        }

        .contact-link:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 20px rgba(102, 126, 234, 0.3);
        }

        .projects {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 30px;
            margin-top: 30px;
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }

        .project-card {
            background: #f8f9fa;
            border-radius: 15px;
            padding: 20px;
            margin-bottom: 20px;
            border-left: 4px solid;
            border-image: linear-gradient(45deg, #667eea, #764ba2) 1;
            transition: transform 0.2s ease;
        }

        .project-card:hover {
            transform: translateX(5px);
        }

        .project-card h3 {
            color: #333;
            margin-bottom: 10px;
        }

        .project-card p {
            color: #666;
            margin-bottom: 10px;
        }

        .project-tech {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
        }

        .tech-tag {
            background: #e9ecef;
            padding: 4px 10px;
            border-radius: 15px;
            font-size: 0.8rem;
            color: #495057;
        }

        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2rem;
            }
            
            .container {
                padding: 15px;
            }
            
            .hero, .section {
                padding: 20px;
            }
            
            .contact-links {
                flex-direction: column;
                align-items: center;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="hero">
            <div class="profile-img">👨‍💻</div>
            <h1>Sandile Ncaba Nkambule</h1>
            <p class="subtitle">Problem-solving IT Technician & Full Stack Developer</p>
            <p class="description">
                Passionate about building efficient web solutions and optimizing IT infrastructures. 
                Recently earned AWS Educate Machine Learning badge, expanding expertise into cloud-based AI solutions and data-driven technologies.
            </p>
        </div>

        <div class="sections">
            <div class="section">
                <h2><span class="section-icon">🚀</span>Technical Skills</h2>
                <div class="skills-grid">
                    <div class="skill-tag">ASP.NET</div>
                    <div class="skill-tag">React.js</div>
                    <div class="skill-tag">Node.js</div>
                    <div class="skill-tag">Android</div>
                    <div class="skill-tag">TCP/IP</div>
                    <div class="skill-tag">DNS</div>
                    <div class="skill-tag">Windows</div>
                    <div class="skill-tag">Linux</div>
                    <div class="skill-tag">Machine Learning</div>
                    <div class="skill-tag">AWS</div>
                    <div class="skill-tag">Data Analysis</div>
                    <div class="skill-tag">Web Design</div>
                </div>
            </div>

            <div class="section">
                <h2><span class="section-icon">💡</span>Expertise</h2>
                <ul style="list-style: none; padding: 0;">
                    <li style="margin-bottom: 15px; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #667eea;">✅</span>
                        Web Application Development & Deployment
                    </li>
                    <li style="margin-bottom: 15px; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #667eea;">✅</span>
                        IT Infrastructure Optimization
                    </li>
                    <li style="margin-bottom: 15px; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #667eea;">✅</span>
                        Complex Application Troubleshooting
                    </li>
                    <li style="margin-bottom: 15px; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #667eea;">✅</span>
                        Biometric Systems (ZK Systems)
                    </li>
                    <li style="margin-bottom: 15px; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #667eea;">✅</span>
                        Data Representation & Analysis
                    </li>
                    <li style="margin-bottom: 15px; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #667eea;">✅</span>
                        Cloud-based AI Solutions
                    </li>
                </ul>
            </div>

            <div class="section">
                <h2><span class="section-icon">🎯</span>Leadership & Soft Skills</h2>
                <ul style="list-style: none; padding: 0;">
                    <li style="margin-bottom: 15px; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #764ba2;">🏆</span>
                        Strong Leadership Abilities
                    </li>
                    <li style="margin-bottom: 15px; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #764ba2;">🤝</span>
                        Excellent Customer Service
                    </li>
                    <li style="margin-bottom: 15px; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #764ba2;">📋</span>
                        Project Management
                    </li>
                    <li style="margin-bottom: 15px; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #764ba2;">💡</span>
                        Innovation Driver
                    </li>
                    <li style="margin-bottom: 15px; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #764ba2;">🔧</span>
                        Problem-solving Mindset
                    </li>
                </ul>
            </div>

            <div class="section">
                <h2><span class="section-icon">📞</span>Connect With Me</h2>
                <div class="contact-links">
                    <a href="mailto:your.email@example.com" class="contact-link">
                        📧 Email
                    </a>
                    <a href="https://linkedin.com/in/yourprofile" class="contact-link">
                        💼 LinkedIn
                    </a>
                    <a href="https://github.com/yourusername" class="contact-link">
                        💻 GitHub
                    </a>
                    <a href="tel:+1234567890" class="contact-link">
                        📱 Phone
                    </a>
                </div>
            </div>
        </div>

        <div class="projects">
            <h2 style="text-align: center; margin-bottom: 30px; color: #333;">
                <span class="section-icon">🛠️</span> Featured Projects
            </h2>
            
            <div class="project-card">
                <h3>Web Application Suite</h3>
                <p>Developed and deployed comprehensive web applications using modern full-stack technologies, focusing on performance and user experience.</p>
                <div class="project-tech">
                    <span class="tech-tag">ASP.NET</span>
                    <span class="tech-tag">React.js</span>
                    <span class="tech-tag">Node.js</span>
                    <span class="tech-tag">Database Design</span>
                </div>
            </div>

            <div class="project-card">
                <h3>Biometric System Integration</h3>
                <p>Successfully troubleshot and optimized ZK biometric systems, improving reliability and integration with existing IT infrastructure.</p>
                <div class="project-tech">
                    <span class="tech-tag">ZK Systems</span>
                    <span class="tech-tag">Network Integration</span>
                    <span class="tech-tag">System Optimization</span>
                </div>
            </div>

            <div class="project-card">
                <h3>AWS Machine Learning Implementation</h3>
                <p>Applied machine learning techniques using AWS services to create data-driven solutions that transform raw data into actionable insights.</p>
                <div class="project-tech">
                    <span class="tech-tag">AWS ML</span>
                    <span class="tech-tag">Data Analysis</span>
                    <span class="tech-tag">Cloud Computing</span>
                    <span class="tech-tag">Data Visualization</span>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Add smooth scrolling for any anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Add parallax effect to background
        window.addEventListener('scroll', () => {
            const scrolled = window.pageYOffset;
            const parallax = document.body;
            const speed = scrolled * 0.5;
            parallax.style.backgroundPosition = `center ${speed}px`;
        });

        // Add typing effect to subtitle
        const subtitle = document.querySelector('.subtitle');
        const text = subtitle.textContent;
        subtitle.textContent = '';
        
        let i = 0;
        const typeWriter = () => {
            if (i < text.length) {
                subtitle.textContent += text.charAt(i);
                i++;
                setTimeout(typeWriter, 100);
            }
        };
        
        // Start typing effect after page loads
        window.addEventListener('load', () => {
            setTimeout(typeWriter, 1000);
        });
    </script>
</body>
</html>
