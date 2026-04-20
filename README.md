<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PZ Furniture | Premium Furniture & Interior Design</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;600;700&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #1a1a1a;
            --primary-gold: #D4AF37;
            --gold-light: #F4E4BC;
            --gold-dark: #B8941F;
            --accent: #C9B037;
            --dark: #0f0f0f;
            --light: #fafafa;
            --gray: #f0f0f0;
            --text: #2c2c2c;
            --text-light: #666;
            --success: #22c55e;
            --danger: #ef4444;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            color: var(--text);
            line-height: 1.6;
            overflow-x: hidden;
            background: var(--light);
        }

        h1, h2, h3, .brand, .logo-text {
            font-family: 'Cinzel', serif;
            letter-spacing: 0.5px;
        }

        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(255,255,255,0.98);
            backdrop-filter: blur(20px);
            z-index: 1000;
            padding: 0.8rem 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 4px 30px rgba(0,0,0,0.08);
        }

        .nav-brand {
            display: flex;
            align-items: center;
            gap: 1rem;
            text-decoration: none;
        }

        .logo-container {
            width: 60px;
            height: 60px;
            position: relative;
        }

        .logo-container img {
            width: 100%;
            height: 100%;
            object-fit: contain;
        }

        .brand-text {
            display: flex;
            flex-direction: column;
        }

        .brand-name {
            font-family: 'Cinzel', serif;
            font-size: 1.4rem;
            font-weight: 700;
            color: var(--primary);
            line-height: 1;
        }

        .brand-tagline {
            font-size: 0.7rem;
            color: var(--primary-gold);
            letter-spacing: 2px;
            text-transform: uppercase;
            margin-top: 2px;
        }

        .nav-links {
            display: flex;
            gap: 2.5rem;
            list-style: none;
            align-items: center;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--text);
            font-weight: 500;
            font-size: 0.95rem;
            position: relative;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: var(--primary-gold);
        }

        .admin-btn {
            background: linear-gradient(135deg, var(--primary-gold), var(--gold-dark));
            color: white;
            border: none;
            padding: 0.7rem 1.5rem;
            border-radius: 30px;
            cursor: pointer;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 0.5rem;
            transition: all 0.3s;
        }

        .admin-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 25px rgba(212,175,55,0.4);
        }

        /* Hero Section */
        .hero {
            margin-top: 76px;
            min-height: 95vh;
            background: linear-gradient(135deg, rgba(26,26,26,0.85), rgba(0,0,0,0.7)),
                        url('https://images.unsplash.com/photo-1618221195710-dd6b41faaea6?w=1920&h=1080&fit=crop');
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            position: relative;
        }

        .hero-content {
            position: relative;
            z-index: 2;
            max-width: 900px;
            padding: 0 2rem;
        }

        .hero-badge {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            background: rgba(212,175,55,0.2);
            border: 1px solid var(--primary-gold);
            padding: 0.5rem 1.2rem;
            border-radius: 50px;
            font-size: 0.9rem;
            margin-bottom: 2rem;
            backdrop-filter: blur(10px);
        }

        .hero h1 {
            font-size: clamp(3rem, 6vw, 5rem);
            margin-bottom: 1.5rem;
            line-height: 1.1;
            text-shadow: 2px 2px 20px rgba(0,0,0,0.5);
            font-weight: 600;
        }

        .hero h1 span {
            color: var(--primary-gold);
            display: block;
            font-size: 0.5em;
            letter-spacing: 8px;
            text-transform: uppercase;
            margin-top: 1rem;
            font-weight: 400;
        }

        .hero p {
            font-size: 1.4rem;
            margin-bottom: 2.5rem;
            opacity: 0.95;
            font-weight: 300;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        .cta-group {
            display: flex;
            gap: 1.5rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            padding: 1.1rem 2.5rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.4s;
            display: inline-flex;
            align-items: center;
            gap: 0.8rem;
            font-size: 1rem;
            border: none;
            cursor: pointer;
        }

        .btn-primary {
            background: linear-gradient(135deg, var(--primary-gold), var(--gold-dark));
            color: white;
            box-shadow: 0 10px 30px rgba(212,175,55,0.3);
        }

        .btn-secondary {
            background: transparent;
            color: white;
            border: 2px solid rgba(255,255,255,0.3);
        }

        .btn-secondary:hover {
            background: white;
            color: var(--dark);
        }

        /* Section Styles */
        section {
            padding: 6rem 5%;
            max-width: 1400px;
            margin: 0 auto;
        }

        .section-header {
            text-align: center;
            margin-bottom: 4rem;
        }

        .section-header h2 {
            font-size: 2.8rem;
            color: var(--primary);
            margin-bottom: 1rem;
            position: relative;
            display: inline-block;
        }

        .section-header h2::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 60px;
            height: 3px;
            background: linear-gradient(90deg, var(--primary-gold), var(--gold-dark));
        }

        .section-header p {
            color: var(--text-light);
            font-size: 1.2rem;
            max-width: 600px;
            margin: 1.5rem auto 0;
        }

        /* About Section */
        .about {
            background: linear-gradient(135deg, #f8f8f8 0%, #fff 100%);
        }

        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 5rem;
            align-items: center;
        }

        .about-visual {
            position: relative;
        }

        .about-frame {
            position: relative;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 30px 60px rgba(0,0,0,0.15);
        }

        .about-frame img {
            width: 100%;
            height: 550px;
            object-fit: cover;
            display: block;
        }

        .experience-badge {
            position: absolute;
            bottom: -30px;
            right: -30px;
            background: linear-gradient(135deg, var(--primary-gold), var(--gold-dark));
            color: white;
            padding: 2rem;
            border-radius: 20px;
            text-align: center;
            box-shadow: 0 10px 30px rgba(212,175,55,0.3);
            z-index: 10;
        }

        .experience-badge .years {
            font-size: 3rem;
            font-weight: 700;
            display: block;
            line-height: 1;
        }

        .about-content h2 {
            font-size: 2.8rem;
            margin-bottom: 1.5rem;
            color: var(--primary);
        }

        .about-content .lead {
            font-size: 1.2rem;
            color: var(--primary-gold);
            margin-bottom: 1.5rem;
            font-weight: 500;
        }

        .about-content p {
            margin-bottom: 1.5rem;
            color: var(--text-light);
            line-height: 1.9;
            font-size: 1.05rem;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 1.5rem;
            margin-top: 2.5rem;
        }

        .feature-box {
            display: flex;
            align-items: flex-start;
            gap: 1rem;
            padding: 1.2rem;
            background: white;
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
        }

        .feature-icon {
            width: 45px;
            height: 45px;
            background: linear-gradient(135deg, var(--gold-light), var(--primary-gold));
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.3rem;
            flex-shrink: 0;
        }

        /* Gallery Section */
        .gallery-section {
            background: white;
        }

        .gallery-controls {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 3rem;
            flex-wrap: wrap;
            gap: 1.5rem;
        }

        .filter-tabs {
            display: flex;
            gap: 0.8rem;
            flex-wrap: wrap;
        }

        .filter-btn {
            padding: 0.7rem 1.8rem;
            border: 2px solid var(--gray);
            background: white;
            border-radius: 30px;
            cursor: pointer;
            transition: all 0.3s;
            font-weight: 500;
            font-size: 0.95rem;
        }

        .filter-btn.active, .filter-btn:hover {
            background: var(--primary);
            color: white;
            border-color: var(--primary);
        }

        .search-box {
            position: relative;
            width: 300px;
        }

        .search-box input {
            width: 100%;
            padding: 0.9rem 1rem 0.9rem 3rem;
            border: 2px solid var(--gray);
            border-radius: 30px;
            font-family: inherit;
            font-size: 0.95rem;
        }

        .search-box::before {
            content: "🔍";
            position: absolute;
            left: 1rem;
            top: 50%;
            transform: translateY(-50%);
            opacity: 0.5;
        }

        .gallery-stats {
            display: flex;
            gap: 2rem;
            margin-bottom: 2rem;
            padding: 1.5rem;
            background: linear-gradient(135deg, var(--gray), white);
            border-radius: 15px;
            border-left: 4px solid var(--primary-gold);
        }

        .stat-item {
            text-align: center;
        }

        .stat-value {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--primary);
            display: block;
        }

        .stat-label {
            font-size: 0.85rem;
            color: var(--text-light);
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
            gap: 2.5rem;
        }

        .gallery-item {
            position: relative;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 10px 40px rgba(0,0,0,0.08);
            transition: all 0.4s;
            background: white;
            cursor: pointer;
        }

        .gallery-item:hover {
            transform: translateY(-10px) scale(1.02);
            box-shadow: 0 20px 60px rgba(0,0,0,0.15);
        }

        .gallery-media {
            position: relative;
            height: 320px;
            overflow: hidden;
        }

        .gallery-media img, .gallery-media video {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.6s;
        }

        .gallery-item:hover .gallery-media img,
        .gallery-item:hover .gallery-media video {
            transform: scale(1.1);
        }

        .media-type {
            position: absolute;
            top: 1rem;
            right: 1rem;
            background: rgba(0,0,0,0.6);
            color: white;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
            backdrop-filter: blur(10px);
            z-index: 5;
        }

        .price-tag {
            position: absolute;
            top: 1rem;
            left: 1rem;
            background: linear-gradient(135deg, var(--primary-gold), var(--gold-dark));
            color: white;
            padding: 0.6rem 1.2rem;
            border-radius: 30px;
            font-weight: 700;
            font-size: 1rem;
            box-shadow: 0 4px 15px rgba(212,175,55,0.3);
            z-index: 5;
        }

        .gallery-info {
            padding: 1.5rem;
        }

        .gallery-meta {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 0.5rem;
        }

        .gallery-category {
            font-size: 0.8rem;
            text-transform: uppercase;
            letter-spacing: 2px;
            color: var(--primary-gold);
            font-weight: 600;
        }

        .gallery-info h3 {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
            color: var(--primary);
        }

        .gallery-info p {
            color: var(--text-light);
            font-size: 0.95rem;
        }

        .gallery-actions {
            position: absolute;
            bottom: 1.5rem;
            right: 1.5rem;
            display: flex;
            gap: 0.5rem;
            opacity: 0;
            transform: translateY(10px);
            transition: all 0.3s;
            z-index: 10;
        }

        .gallery-item:hover .gallery-actions {
            opacity: 1;
            transform: translateY(0);
        }

        .action-btn {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            border: none;
            background: white;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        .action-btn:hover {
            transform: scale(1.1);
            background: var(--primary-gold);
            color: white;
        }

        /* Services Section */
        .services {
            background: linear-gradient(135deg, var(--primary) 0%, #2a2a2a 100%);
            color: white;
        }

        .services .section-header h2 {
            color: white;
        }

        .services .section-header p {
            color: rgba(255,255,255,0.7);
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2.5rem;
        }

        .service-card {
            background: rgba(255,255,255,0.03);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(212,175,55,0.2);
            border-radius: 24px;
            padding: 3rem 2rem;
            text-align: center;
            transition: all 0.4s;
        }

        .service-card:hover {
            transform: translateY(-8px);
            background: rgba(255,255,255,0.08);
            border-color: var(--primary-gold);
        }

        .service-icon {
            width: 80px;
            height: 80px;
            background: linear-gradient(135deg, rgba(212,175,55,0.2), rgba(212,175,55,0.05));
            border-radius: 24px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2.5rem;
            margin: 0 auto 1.5rem;
            border: 1px solid rgba(212,175,55,0.3);
        }

        .service-card h3 {
            font-size: 1.4rem;
            margin-bottom: 1rem;
            color: var(--primary-gold);
        }

        .service-card p {
            color: rgba(255,255,255,0.7);
            font-size: 1rem;
            line-height: 1.7;
        }

        /* Contact Section */
        .contact {
            background: linear-gradient(135deg, #f8f8f8 0%, #fff 100%);
        }

        .contact-wrapper {
            display: grid;
            grid-template-columns: 1.2fr 1fr;
            gap: 4rem;
            align-items: start;
        }

        .contact-form-wrapper {
            background: white;
            padding: 3rem;
            border-radius: 24px;
            box-shadow: 0 20px 60px rgba(0,0,0,0.08);
        }

        .contact-form-wrapper h3 {
            font-size: 1.8rem;
            margin-bottom: 2rem;
            color: var(--primary);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
            color: var(--text);
            font-size: 0.95rem;
        }

        .form-group input,
        .form-group textarea,
        .form-group select {
            width: 100%;
            padding: 1rem;
            border: 2px solid var(--gray);
            border-radius: 12px;
            font-family: inherit;
            font-size: 1rem;
            transition: all 0.3s;
        }

        .form-group input:focus,
        .form-group textarea:focus,
        .form-group select:focus {
            outline: none;
            border-color: var(--primary-gold);
            box-shadow: 0 0 0 4px rgba(212,175,55,0.1);
        }

        .form-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1.5rem;
        }

        .submit-btn {
            width: 100%;
            padding: 1.2rem;
            background: linear-gradient(135deg, var(--primary-gold), var(--gold-dark));
            color: white;
            border: none;
            border-radius: 12px;
            font-size: 1.1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.5rem;
        }

        .submit-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 30px rgba(212,175,55,0.3);
        }

        .contact-info-panel {
            display: flex;
            flex-direction: column;
            gap: 1.5rem;
        }

        .info-card {
            background: white;
            padding: 2rem;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.05);
            display: flex;
            align-items: flex-start;
            gap: 1.5rem;
            transition: all 0.3s;
            border-left: 4px solid transparent;
        }

        .info-card:hover {
            transform: translateX(5px);
            border-left-color: var(--primary-gold);
        }

        .info-icon-wrap {
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, var(--gold-light), var(--primary-gold));
            border-radius: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
            flex-shrink: 0;
        }

        .info-details h4 {
            font-size: 1.2rem;
            margin-bottom: 0.5rem;
            color: var(--primary);
        }

        .info-details p {
            color: var(--text-light);
            line-height: 1.6;
            font-size: 1rem;
        }

        .map-embed {
            width: 100%;
            height: 300px;
            border-radius: 20px;
            overflow: hidden;
            margin-top: 1rem;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            background: var(--gray);
            display: flex;
            align-items: center;
            justify-content: center;
            flex-direction: column;
            color: var(--text-light);
        }

        /* Admin Panel */
        .admin-overlay {
            position: fixed;
            inset: 0;
            background: rgba(0,0,0,0.6);
            backdrop-filter: blur(5px);
            z-index: 1999;
            opacity: 0;
            visibility: hidden;
            transition: all 0.3s;
        }

        .admin-overlay.active {
            opacity: 1;
            visibility: visible;
        }

        .admin-panel {
            position: fixed;
            right: -500px;
            top: 0;
            width: 480px;
            height: 100vh;
            background: white;
            z-index: 2000;
            transition: right 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            display: flex;
            flex-direction: column;
            box-shadow: -10px 0 50px rgba(0,0,0,0.2);
        }

        .admin-panel.active {
            right: 0;
        }

        .admin-header {
            padding: 1.5rem 2rem;
            background: linear-gradient(135deg, var(--primary), #2a2a2a);
            color: white;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .admin-header h3 {
            font-size: 1.3rem;
            display: flex;
            align-items: center;
            gap: 0.8rem;
        }

        .admin-close {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            border: none;
            background: rgba(255,255,255,0.1);
            color: white;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            transition: all 0.3s;
        }

        .admin-close:hover {
            background: rgba(255,255,255,0.2);
            transform: rotate(90deg);
        }

        .admin-tabs {
            display: flex;
            border-bottom: 1px solid var(--gray);
            padding: 0 2rem;
            gap: 2rem;
        }

        .admin-tab {
            padding: 1rem 0;
            border: none;
            background: none;
            cursor: pointer;
            font-weight: 600;
            color: var(--text-light);
            position: relative;
            transition: color 0.3s;
        }

        .admin-tab.active {
            color: var(--primary-gold);
        }

        .admin-tab.active::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            height: 3px;
            background: var(--primary-gold);
        }

        .admin-content {
            flex: 1;
            overflow-y: auto;
            padding: 2rem;
        }

        .tab-content {
            display: none;
        }

        .tab-content.active {
            display: block;
            animation: fadeIn 0.3s;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .upload-zone {
            border: 3px dashed var(--gray);
            border-radius: 20px;
            padding: 3rem 2rem;
            text-align: center;
            background: linear-gradient(135deg, #fafafa, #f0f0f0);
            transition: all 0.3s;
            cursor: pointer;
            position: relative;
            overflow: hidden;
        }

        .upload-zone:hover, .upload-zone.dragover {
            border-color: var(--primary-gold);
            background: linear-gradient(135deg, var(--gold-light), #fafafa);
            transform: scale(1.02);
        }

        .upload-zone-icon {
            width: 80px;
            height: 80px;
            background: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            margin: 0 auto 1rem;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }

        .upload-zone h4 {
            font-size: 1.2rem;
            margin-bottom: 0.5rem;
            color: var(--primary);
        }

        .upload-zone p {
            color: var(--text-light);
            font-size: 0.95rem;
        }

        .file-input {
            display: none;
        }

        .upload-preview {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 1rem;
            margin-top: 1.5rem;
        }

        .preview-item {
            aspect-ratio: 1;
            border-radius: 12px;
            overflow: hidden;
            position: relative;
            border: 2px solid var(--gray);
        }

        .preview-item img, .preview-item video {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .preview-remove {
            position: absolute;
            top: 5px;
            right: 5px;
            width: 25px;
            height: 25px;
            background: var(--danger);
            color: white;
            border: none;
            border-radius: 50%;
            cursor: pointer;
            font-size: 1rem;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .form-section {
            background: var(--gray);
            padding: 1.5rem;
            border-radius: 16px;
            margin-bottom: 1.5rem;
        }

        .form-section h4 {
            margin-bottom: 1rem;
            color: var(--primary);
            font-size: 1.1rem;
        }

        .input-group {
            margin-bottom: 1rem;
        }

        .input-group label {
            display: block;
            margin-bottom: 0.4rem;
            font-size: 0.9rem;
            font-weight: 500;
            color: var(--text);
        }

        .input-group input,
        .input-group select,
        .input-group textarea {
            width: 100%;
            padding: 0.8rem;
            border: 1px solid #ddd;
            border-radius: 10px;
            font-family: inherit;
            font-size: 0.95rem;
        }

        .input-group input:focus,
        .input-group select:focus,
        .input-group textarea:focus {
            outline: none;
            border-color: var(--primary-gold);
        }

        .input-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1rem;
        }

        .btn-full {
            width: 100%;
            padding: 1rem;
            background: linear-gradient(135deg, var(--primary-gold), var(--gold-dark));
            color: white;
            border: none;
            border-radius: 12px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.5rem;
        }

        .btn-full:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 30px rgba(212,175,55,0.3);
        }

        .btn-full:disabled {
            opacity: 0.6;
            cursor: not-allowed;
            transform: none;
        }

        .items-search {
            margin-bottom: 1.5rem;
        }

        .items-search input {
            width: 100%;
            padding: 0.8rem 1rem;
            border: 1px solid var(--gray);
            border-radius: 10px;
            font-family: inherit;
        }

        .admin-item {
            display: flex;
            gap: 1rem;
            padding: 1rem;
            background: var(--gray);
            border-radius: 12px;
            margin-bottom: 1rem;
            align-items: center;
            transition: all 0.3s;
        }

        .admin-item:hover {
            background: #e8e8e8;
            transform: translateX(5px);
        }

        .admin-item-media {
            width: 70px;
            height: 70px;
            border-radius: 10px;
            overflow: hidden;
            flex-shrink: 0;
            position: relative;
        }

        .admin-item-media img, .admin-item-media video {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .admin-item-info {
            flex: 1;
            min-width: 0;
        }

        .admin-item-info h4 {
            font-size: 1rem;
            margin-bottom: 0.2rem;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

        .admin-item-info p {
            font-size: 0.85rem;
            color: var(--text-light);
        }

        .admin-item-actions {
            display: flex;
            gap: 0.5rem;
        }

        .icon-btn {
            width: 35px;
            height: 35px;
            border-radius: 8px;
            border: none;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.2s;
        }

        .icon-btn.edit {
            background: var(--primary);
            color: white;
        }

        .icon-btn.delete {
            background: var(--danger);
            color: white;
        }

        .icon-btn:hover {
            transform: scale(1.1);
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 1rem;
            margin-bottom: 2rem;
        }

        .stat-card {
            background: linear-gradient(135deg, var(--primary), #2a2a2a);
            color: white;
            padding: 1.5rem;
            border-radius: 16px;
            text-align: center;
        }

        .stat-card h5 {
            font-size: 0.9rem;
            opacity: 0.8;
            margin-bottom: 0.5rem;
        }

        .stat-card .value {
            font-size: 2rem;
            font-weight: 700;
            color: var(--primary-gold);
        }

        .category-chart {
            background: var(--gray);
            padding: 1.5rem;
            border-radius: 16px;
        }

        .category-chart h4 {
            margin-bottom: 1rem;
            color: var(--primary);
        }

        .chart-item {
            display: flex;
            align-items: center;
            gap: 1rem;
            margin-bottom: 1rem;
        }

        .chart-label {
            width: 100px;
            font-size: 0.9rem;
            color: var(--text);
        }

        .chart-bar {
            flex: 1;
            height: 8px;
            background: #ddd;
            border-radius: 4px;
            overflow: hidden;
        }

        .chart-fill {
            height: 100%;
            background: linear-gradient(90deg, var(--primary-gold), var(--gold-dark));
            border-radius: 4px;
            transition: width 0.5s;
        }

        .chart-value {
            width: 40px;
            text-align: right;
            font-weight: 600;
            font-size: 0.9rem;
        }

        /* Backup/Restore Buttons */
        .backup-section {
            margin-top: 2rem;
            padding: 1.5rem;
            background: linear-gradient(135deg, #f0f0f0, #fafafa);
            border-radius: 16px;
            border: 2px dashed var(--primary-gold);
        }

        .backup-section h4 {
            margin-bottom: 1rem;
            color: var(--primary);
        }

        .backup-btn {
            width: 100%;
            padding: 0.8rem;
            margin-bottom: 0.5rem;
            background: white;
            border: 2px solid var(--gray);
            border-radius: 10px;
            cursor: pointer;
            font-weight: 500;
            transition: all 0.3s;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.5rem;
        }

        .backup-btn:hover {
            border-color: var(--primary-gold);
            background: var(--gold-light);
        }

        /* Footer */
        footer {
            background: var(--primary);
            color: white;
            padding: 5rem 5% 2rem;
            position: relative;
        }

        footer::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, var(--primary-gold), var(--gold-dark));
        }

        .footer-grid {
            display: grid;
            grid-template-columns: 2fr 1fr 1fr 1.5fr;
            gap: 4rem;
            margin-bottom: 4rem;
        }

        .footer-brand {
            display: flex;
            flex-direction: column;
        }

        .footer-logo {
            display: flex;
            align-items: center;
            gap: 1rem;
            margin-bottom: 1.5rem;
        }

        .footer-logo img {
            width: 60px;
            height: 60px;
            object-fit: contain;
            filter: brightness(0) invert(1);
        }

        .footer-logo-text h3 {
            font-size: 1.5rem;
            color: white;
            margin-bottom: 0.2rem;
        }

        .footer-logo-text span {
            color: var(--primary-gold);
            font-size: 0.8rem;
            letter-spacing: 2px;
            text-transform: uppercase;
        }

        .footer-brand p {
            color: rgba(255,255,255,0.7);
            line-height: 1.8;
            margin-bottom: 1.5rem;
        }

        .social-grid {
            display: flex;
            gap: 1rem;
        }

        .social-btn {
            width: 45px;
            height: 45px;
            background: rgba(255,255,255,0.1);
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            text-decoration: none;
            transition: all 0.3s;
            font-size: 1.2rem;
        }

        .social-btn:hover {
            background: var(--primary-gold);
            color: var(--primary);
            transform: translateY(-3px);
        }

        .footer-section h4 {
            color: var(--primary-gold);
            margin-bottom: 1.5rem;
            font-size: 1.2rem;
        }

        .footer-section ul {
            list-style: none;
        }

        .footer-section li {
            margin-bottom: 1rem;
        }

        .footer-section a {
            color: rgba(255,255,255,0.7);
            text-decoration: none;
            transition: all 0.3s;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .footer-section a:hover {
            color: var(--primary-gold);
            padding-left: 5px;
        }

        .contact-list li {
            display: flex;
            align-items: flex-start;
            gap: 1rem;
            margin-bottom: 1.2rem;
        }

        .contact-icon {
            color: var(--primary-gold);
            font-size: 1.2rem;
        }

        .contact-text {
            color: rgba(255,255,255,0.8);
            font-size: 0.95rem;
            line-height: 1.5;
        }

        .footer-bottom {
            border-top: 1px solid rgba(255,255,255,0.1);
            padding-top: 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            color: rgba(255,255,255,0.5);
            font-size: 0.9rem;
        }

        /* Lightbox */
        .lightbox {
            position: fixed;
            inset: 0;
            background: rgba(0,0,0,0.95);
            z-index: 3000;
            display: none;
            align-items: center;
            justify-content: center;
            backdrop-filter: blur(10px);
        }

        .lightbox.active {
            display: flex;
            animation: fadeIn 0.3s;
        }

        .lightbox-container {
            max-width: 90vw;
            max-height: 90vh;
            position: relative;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .lightbox-media {
            max-width: 100%;
            max-height: 75vh;
            border-radius: 12px;
            box-shadow: 0 20px 60px rgba(0,0,0,0.5);
        }

        .lightbox-info {
            background: rgba(255,255,255,0.1);
            backdrop-filter: blur(20px);
            padding: 1.5rem 3rem;
            border-radius: 16px;
            margin-top: 1.5rem;
            text-align: center;
            color: white;
            max-width: 600px;
        }

        .lightbox-info h3 {
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
        }

        .lightbox-price {
            color: var(--primary-gold);
            font-size: 1.3rem;
            font-weight: 700;
        }

        .lightbox-close {
            position: absolute;
            top: 2rem;
            right: 2rem;
            width: 50px;
            height: 50px;
            background: rgba(255,255,255,0.1);
            border: none;
            border-radius: 50%;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
            transition: all 0.3s;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .lightbox-close:hover {
            background: var(--danger);
            transform: rotate(90deg);
        }

        .lightbox-nav {
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            width: 60px;
            height: 60px;
            background: rgba(255,255,255,0.1);
            border: none;
            border-radius: 50%;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
            transition: all 0.3s;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .lightbox-nav:hover {
            background: var(--primary-gold);
            color: var(--primary);
        }

        .lightbox-prev { left: 2rem; }
        .lightbox-next { right: 2rem; }

        /* Toast */
        .toast-container {
            position: fixed;
            bottom: 2rem;
            right: 2rem;
            z-index: 4000;
            display: flex;
            flex-direction: column;
            gap: 1rem;
        }

        .toast {
            background: white;
            padding: 1rem 1.5rem;
            border-radius: 12px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
            display: flex;
            align-items: center;
            gap: 1rem;
            min-width: 300px;
            transform: translateX(400px);
            transition: transform 0.3s;
            border-left: 4px solid var(--success);
        }

        .toast.show {
            transform: translateX(0);
        }

        .toast.error {
            border-left-color: var(--danger);
        }

        /* Animations */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.8s ease;
        }

        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }

        /* Responsive */
        @media (max-width: 1024px) {
            .about-grid, .contact-wrapper {
                grid-template-columns: 1fr;
            }
            
            .footer-grid {
                grid-template-columns: 1fr 1fr;
            }
            
            .admin-panel {
                width: 100%;
                right: -100%;
            }
            
            .gallery-controls {
                flex-direction: column;
                align-items: stretch;
            }
            
            .search-box {
                width: 100%;
            }
        }

        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .features-grid {
                grid-template-columns: 1fr;
            }
            
            .footer-grid {
                grid-template-columns: 1fr;
                gap: 2rem;
            }
            
            .footer-bottom {
                flex-direction: column;
                gap: 1rem;
                text-align: center;
            }
            
            .lightbox-nav {
                display: none;
            }
            
            .form-row, .input-row {
                grid-template-columns: 1fr;
            }
        }

        .empty-state {
            text-align: center;
            padding: 4rem 2rem;
            color: var(--text-light);
            grid-column: 1 / -1;
        }

        .empty-state-icon {
            font-size: 4rem;
            margin-bottom: 1rem;
            opacity: 0.5;
        }

        .storage-warning {
            background: #fff3cd;
            border: 1px solid #ffc107;
            color: #856404;
            padding: 1rem;
            border-radius: 10px;
            margin-bottom: 1rem;
            font-size: 0.9rem;
        }
    </style>
</head>
<body>

    <!-- Toast Container -->
    <div class="toast-container" id="toastContainer"></div>

    <!-- Admin Overlay -->
    <div class="admin-overlay" id="adminOverlay" onclick="toggleAdmin()"></div>

    <!-- Admin Panel -->
    <div class="admin-panel" id="adminPanel">
        <div class="admin-header">
            <h3>⚡ Content Manager</h3>
            <button class="admin-close" onclick="toggleAdmin()">×</button>
        </div>
        
        <div class="admin-tabs">
            <button class="admin-tab active" onclick="switchTab('upload')">📤 Upload</button>
            <button class="admin-tab" onclick="switchTab('items')">🖼️ Items</button>
            <button class="admin-tab" onclick="switchTab('stats')">📊 Stats</button>
        </div>
        
        <div class="admin-content">
            <!-- Upload Tab -->
            <div class="tab-content active" id="uploadTab">
                <div class="storage-warning" id="storageWarning" style="display: none;">
                    ⚠️ Storage is getting full. Consider exporting backup.
                </div>
                
                <div class="upload-section">
                    <div class="upload-zone" id="uploadZone">
                        <div class="upload-zone-icon">📁</div>
                        <h4>Tap to select files</h4>
                        <p>Supports: JPG, PNG, WEBP, MP4 (Max 5MB each)</p>
                        <input type="file" class="file-input" id="fileInput" multiple accept="image/*,video/*">
                    </div>
                    
                    <div class="upload-preview" id="uploadPreview"></div>
                    
                    <div class="form-section">
                        <h4>Product Details</h4>
                        <div class="input-group">
                            <label>Category</label>
                            <select id="uploadCategory">
                                <option value="sofas">Sofas</option>
                                <option value="dining">Dining Sets</option>
                                <option value="office">Office Furniture</option>
                                <option value="cabinets">Cabinets</option>
                                <option value="custom">Custom Pieces</option>
                                <option value="interior">Interior Design</option>
                                <option value="service">carpentry services</option>
                                <option value="interior">Interior Design</option>
                                <option                                                       value="tv">TVUnits</option>
                                <option>      value="general"general contractor</option>                   
                                <option>                   value="wardrobe"wardrobe closets</option>                                           
                            </select>
                        </div>
                        <div class="input-row">
                            <div class="input-group">
                                <label>Title</label>
                                <input type="text" id="uploadTitle" placeholder="e.g., Luxury Sectional">
                            </div>
                            <div class="input-group">
                                <label>Price (₦)</label>
                                <input type="text" id="uploadPrice" placeholder="e.g., 850,000">
                            </div>
                        </div>
                        <div class="input-group">
                            <label>Description</label>
                            <textarea id="uploadDesc" rows="2" placeholder="Brief description..."></textarea>
                        </div>
                        <button class="btn-full" onclick="processUpload()" id="uploadBtn">
                            <span>🚀</span> Add to Gallery
                        </button>
                    </div>
                </div>
                
                <!-- Backup Section -->
                <div class="backup-section">
                    <h4>💾 Backup & Restore</h4>
                    <p style="font-size: 0.9rem; color: var(--text-light); margin-bottom: 1rem;">
                        Save your data to a file or restore from previous backup
                    </p>
                    <button class="backup-btn" onclick="exportData()">
                        <span>💾</span> Export Data to File
                    </button>
                    <button class="backup-btn" onclick="document.getElementById('importFile').click()">
                        <span>📂</span> Import Data from File
                    </button>
                    <input type="file" id="importFile" style="display: none;" accept=".json" onchange="importData(this)">
                </div>
            </div>
            
            <!-- Items Tab -->
            <div class="tab-content" id="itemsTab">
                <div class="items-search">
                    <input type="text" placeholder="Search items..." id="adminSearch" onkeyup="filterAdminItems()">
                </div>
                <div id="adminItemsList"></div>
            </div>
            
            <!-- Stats Tab -->
            <div class="tab-content" id="statsTab">
                <div class="stats-grid">
                    <div class="stat-card">
                        <h5>Total Items</h5>
                        <div class="value" id="statTotal">0</div>
                    </div>
                    <div class="stat-card">
                        <h5>Categories</h5>
                        <div class="value" id="statCategories">0</div>
                    </div>
                    <div class="stat-card">
                        <h5>Images</h5>
                        <div class="value" id="statImages">0</div>
                    </div>
                    <div class="stat-card">
                        <h5>Videos</h5>
                        <div class="value" id="statVideos">0</div>
                    </div>
                </div>
                <div class="category-chart">
                    <h4>Items by Category</h4>
                    <div id="categoryChart"></div>
                </div>
                
                <div class="storage-warning" style="margin-top: 2rem;">
                    <strong>Storage Info:</strong><br>
                    Current usage: <span id="storageSize">0 MB</span> / ~5-10 MB limit<br>
                    <small>If uploads fail, export data, clear storage, and re-import.</small>
                </div>
            </div>
        </div>
    </div>

    <!-- Navigation -->
    <nav id="navbar">
        <a href="#" class="nav-brand">
            <div class="logo-container">
                <img src="logo.jpg" alt="PZ Furniture Logo" onerror="this.src='https://via.placeholder.com/60x60/D4AF37/FFFFFF?text=PZ'">
            </div>
            <div class="brand-text">
                <span class="brand-name">PZ Furniture</span>
                <span class="brand-tagline">Premium Interiors</span>
            </div>
        </a>
        <ul class="nav-links">
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#collection">Collection</a></li>
            <li><a href="#services">Services</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
        <button class="admin-btn" onclick="toggleAdmin()">
            <span>⚙️</span> Manage
        </button>
    </nav>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="hero-content">
            <div class="hero-badge">
                <span>✦</span> Est. Warri, Delta State
            </div>
            <h1>
                Crafting Timeless Elegance
                <span>for Your Space</span>
            </h1>
            <p>Premium furniture and interior design solutions where luxury meets functionality. Transform your house into a masterpiece.</p>
            <div class="cta-group">
                <a href="#collection" class="btn btn-primary">
                    <span>🛋️</span> Explore Collection
                </a>
                <a href="#contact" class="btn btn-secondary">
                    <span>📞</span> Get Quote
                </a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about" id="about">
        <div class="about-grid">
            <div class="about-visual fade-in">
                <div class="about-frame">
                    <img src="https://images.unsplash.com/photo-1555041469-a586c61ea9bc?w=800&h=600&fit=crop" alt="Workshop">
                </div>
                <div class="experience-badge">
                    <span class="years">15+</span>
                    <span class="text">Years of<br>Excellence</span>
                </div>
            </div>
            <div class="about-content fade-in">
                <h2>Excellence in Furniture Making</h2>
                <p class="lead">Located at 88 Effurun Sapele Road, Warri, Delta State</p>
                <p>PZ Furniture has established itself as Nigeria's premier destination for high-quality furniture and interior design. We blend modern minimalist aesthetics with luxury craftsmanship to create pieces that transform houses into homes.</p>
                <div class="features-grid">
                    <div class="feature-box">
                        <div class="feature-icon">🪵</div>
                        <div class="feature-text">
                            <h4>Premium Materials</h4>
                            <p>Imported woods & fabrics</p>
                        </div>
                    </div>
                    <div class="feature-box">
                        <div class="feature-icon">✏️</div>
                        <div class="feature-text">
                            <h4>Custom Designs</h4>
                            <p>Tailored to your space</p>
                        </div>
                    </div>
                    <div class="feature-box">
                        <div class="feature-icon">👨‍🔧</div>
                        <div class="feature-text">
                            <h4>Expert Craftsmen</h4>
                            <p>15+ years experience</p>
                        </div>
                    </div>
                    <div class="feature-box">
                        <div class="feature-icon">🚚</div>
                        <div class="feature-text">
                            <h4>Full Service</h4>
                            <p>Delivery & installation</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Gallery Section -->
    <section class="gallery-section" id="collection">
        <div class="section-header fade-in">
            <h2>Our Collection</h2>
            <p>Discover meticulously crafted furniture designed to elevate your living and working spaces</p>
        </div>
        
        <div class="gallery-controls fade-in">
            <div class="filter-tabs">
                <button class="filter-btn active" onclick="filterGallery('all')">All</button>
                <button class="filter-btn" onclick="filterGallery('sofas')">Sofas</button>
                <button class="filter-btn" onclick="filterGallery('dining')">Dining</button>
                <button class="filter-btn" onclick="filterGallery('office')">Office</button>
                <button class="filter-btn" onclick="filterGallery('cabinets')">Cabinets</button>
                <button class="filter-btn" onclick="filterGallery('custom')">Custom</button>
                <button class="filter-btn" onclick="filterGallery('tv')">TV Units</button>
                <button class="filter-btn" onclick="filterGallery(wardrobe)">wardrobe closets</button>
                <button class="filter-btn" onclick="filterGallery(contractor)">general contractor</button>
                <button class="filter-btn" onclick="filterGallery(service)">carpentry services</button>            </div>
            <div class="search-box">
                <input type="text" placeholder="Search products..." id="gallerySearch" onkeyup="searchGallery()">
            </div>
        </div>

        <div class="gallery-stats fade-in" id="galleryStats">
            <div class="stat-item">
                <span class="stat-value" id="totalItems">0</span>
                <span class="stat-label">Products</span>
            </div>
            <div class="stat-item">
                <span class="stat-value" id="totalCategories">7</span>
                <span class="stat-label">Categories</span>
            </div>
            <div class="stat-item">
                <span class="stat-value">100%</span>
                <span class="stat-label">Customizable</span>
            </div>
        </div>
        
        <div class="gallery-grid" id="galleryGrid"></div>
    </section>

    <!-- Services Section -->
    <section class="services" id="services">
        <div class="section-header fade-in">
            <h2>Our Services</h2>
            <p>Comprehensive interior solutions tailored to your unique style and requirements</p>
        </div>
        
        <div class="services-grid">
            <div class="service-card fade-in">
                <div class="service-icon">🛋️</div>
                <h3>Custom Furniture</h3>
                <p>Bespoke pieces designed and crafted to your exact specifications.</p>
            </div>
            <div class="service-card fade-in">
                <div class="service-icon">🏠</div>
                <h3>Interior Design</h3>
                <p>Full-service design from concept to completion.</p>
            </div>
            <div class="service-card fade-in">
                <div class="service-icon">🚚</div>
                <h3>Delivery & Installation</h3>
                <p>Professional white-glove service across Delta State.</p>
            </div>
            <div class="service-card fade-in">
                <div class="service-icon">🔧</div>
                <h3>Repair & Restoration</h3>
                <p>Expert furniture repair and reupholstery.</p>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
        <div class="section-header fade-in">
            <h2>Get In Touch</h2>
            <p>Visit our showroom or reach out for a consultation.</p>
        </div>
        
        <div class="contact-wrapper">
            <div class="contact-form-wrapper fade-in">
                <h3>Request a Quote</h3>
                <form id="contactForm" onsubmit="handleContact(event)">
                    <div class="form-row">
                        <div class="form-group">
                            <label>First Name</label>
                            <input type="text" required placeholder="John">
                        </div>
                        <div class="form-group">
                            <label>Last Name</label>
                            <input type="text" required placeholder="Doe">
                        </div>
                    </div>
                    <div class="form-row">
                        <div class="form-group">
                            <label>Phone</label>
                            <input type="tel" required placeholder="+234 807 625 9610">
                        </div>
                        <div class="form-group">
                            <label>Email</label>
                            <input type="email" placeholder="john@example.com">
                        </div>
                    </div>
                    <div class="form-group">
                        <label>Service Interested In</label>
                        <select required>
                            <option value="">Select a service...</option>
                            <option value="furniture">Custom Furniture</option>
                            <option value="interior">Interior Design</option>
                            <option value="office">Office Fit-out</option>
                            <option value="repair">Furniture Repair</option>
                            <option value="carpentry">carpentry</option>
                           <option value="wardrobe">wardrobe closets</option>
                           <option value="contractor">general contractor</option>                                                                                                 
                        </select>
                    </div>
                    <div class="form-group">
                        <label>Message</label>
                        <textarea rows="4" placeholder="Tell us about your project..."></textarea>
                    </div>
                    <button type="submit" class="submit-btn">
                        <span>📤</span> Send Message
                    </button>
                </form>
            </div>
            
            <div class="contact-info-panel fade-in">
                <div class="info-card">
                    <div class="info-icon-wrap">📍</div>
                    <div class="info-details">
                        <h4>Visit Our Showroom</h4>
                        <p>88 Effurun Sapele Road<br>Warri, Delta State, Nigeria</p>
                    </div>
                </div>
                
                <div class="info-card">
                    <div class="info-icon-wrap">📞</div>
                    <div class="info-details">
                        <h4>Phone</h4>
                        <p>+234 807 625 9610<br>+234 808 394 3607</p>
                    </div>
                </div>
                
                <div class="info-card">
                    <div class="info-icon-wrap">✉️</div>
                    <div class="info-details">
                        <h4>Email</h4>
                        <p>info@pzfurniture.com<br>sales@pzfurniture.com</p>
                    </div>
                </div>
                
                <div class="info-card">
                    <div class="info-icon-wrap">🕒</div>
                    <div class="info-details">
                        <h4>Business Hours</h4>
                        <p>Mon - Sat: 8:00 AM - 6:00 PM<br>Sunday: Closed</p>
                    </div>
                </div>

                <div class="map-embed">
                    <span style="font-size: 3rem; margin-bottom: 1rem;">🗺️</span>
                    <p>88 Effurun Sapele Road, Warri</p>
                    <p style="font-size: 0.9rem; margin-top: 0.5rem;">View on Google Maps</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-grid">
            <div class="footer-brand">
                <div class="footer-logo">
                    <img src="logo.jpg" alt="PZ Furniture" onerror="this.src='https://via.placeholder.com/60x60/D4AF37/FFFFFF?text=PZ'">
                    <div class="footer-logo-text">
                        <h3>PZ Furniture</h3>
                        <span>Premium Interiors</span>
                    </div>
                </div>
                <p>Premium furniture and interior design solutions in Warri, Delta State. Crafting timeless elegance for your space since 2009.</p>
                <div class="social-grid">
                    <a href="https://tiktok.com/@pzfur_niture" target="_blank" class="social-btn" title="TikTok">TT</a>
                    <a href="https://instagram.com/@pzfur_niture" target="_blank" class="social-btn" title="Instagram">IG</a>
                    <a href="https://twitter.com/@pz_Furniture" target="_blank" class="social-btn" title="Twitter">X</a>
                    <a href="https://wa.me/2348083943607" target="_blank" class="social-btn" title="WhatsApp">WA</a>
                </div>
            </div>
            
            <div class="footer-section">
                <h4>Quick Links</h4>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About Us</a></li>
                    <li><a href="#collection">Products</a></li>
                    <li><a href="#services">Services</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </div>
            
            <div class="footer-section">
                <h4>Services</h4>
                <ul>
                    <li><a href="#services">Custom Furniture</a></li>
                    <li><a href="#services">Interior Design</a></li>
                    <li><a href="#services">Office Fit-out</a></li>
                    <li><a href="#services">Furniture Repair</a></li>
                <li><a                      href="#services">bedroom section</a></li>                   
                <li><a  href="#services">general contractor</a></li> 
                <li><a                          href="#services">wardrobe/closets</a></li>         
                </ul>
            </div>
            
            <div class="footer-section">
                <h4>Contact Info</h4>
                <ul class="contact-list">
                    <li>
                        <span class="contact-icon">📍</span>
                        <span class="contact-text">88 Effurun Sapele Road,<br>Warri, Delta State</span>
                    </li>
                    <li>
                        <span class="contact-icon">📞</span>
                        <span class="contact-text">+234 807 625 9610<br>+234 808 394 3607</span>
                    </li>
                    <li>
                        <span class="contact-icon">✉️</span>
                        <span class="contact-text">info@pzfurniture.com</span>
                    </li>
                </ul>
            </div>
        </div>
        
        <div class="footer-bottom">
            <p>&copy; 2026 PZ Furniture. All rights reserved.</p>
            <div class="footer-bottom-links">
                <a href="#">Privacy Policy</a>
                <a href="#">Terms of Service</a>
            </div>
        </div>
    </footer>

    <!-- Lightbox -->
    <div class="lightbox" id="lightbox" onclick="closeLightbox(event)">
        <button class="lightbox-close" onclick="closeLightbox()">×</button>
        <button class="lightbox-nav lightbox-prev" onclick="changeImage(-1)">‹</button>
        <div class="lightbox-container" onclick="event.stopPropagation()">
            <div id="lightboxMedia"></div>
            <div class="lightbox-info" id="lightboxInfo"></div>
        </div>
        <button class="lightbox-nav lightbox-next" onclick="changeImage(1)">›</button>
    </div>

    <script>
        // Data Management with compression and backup
        const STORAGE_KEY = 'pzFurnitureGallery_v3';
        let galleryItems = [];
        let tempFiles = [];
        let currentFilter = 'all';
        let currentImageIndex = 0;
        let searchQuery = '';

        // Initialize
        document.addEventListener('DOMContentLoaded', () => {
            loadData();
            checkStorage();
            if (galleryItems.length === 0) initializeDefaultData();
            renderGallery();
            renderAdminItems();
            updateStats();
            setupEventListeners();
            setupIntersectionObserver();
        });

        function checkStorage() {
            try {
                const total = JSON.stringify(localStorage).length;
                const mb = (total / 1024 / 1024).toFixed(2);
                document.getElementById('storageSize').textContent = mb + ' MB';
                
                if (total > 4 * 1024 * 1024) { // 4MB warning
                    document.getElementById('storageWarning').style.display = 'block';
                }
            } catch(e) {
                console.error('Storage check failed:', e);
            }
        }

        function loadData() {
            try {
                const stored = localStorage.getItem(STORAGE_KEY);
                if (stored) {
                    galleryItems = JSON.parse(stored);
                    console.log('Loaded ' + galleryItems.length + ' items');
                }
            } catch (e) {
                console.error('Error loading data:', e);
                showToast('Error loading saved data', 'error');
            }
        }

        function saveData() {
            try {
                localStorage.setItem(STORAGE_KEY, JSON.stringify(galleryItems));
                checkStorage();
                console.log('Saved ' + galleryItems.length + ' items');
            } catch (e) {
                if (e.name === 'QuotaExceededError') {
                    showToast('Storage full! Export data and clear storage.', 'error');
                    document.getElementById('storageWarning').style.display = 'block';
                } else {
                    showToast('Error saving data', 'error');
                }
            }
        }

        function initializeDefaultData() {
            galleryItems = [
                {
                    id: Date.now() + 1,
                    category: 'sofas',
                    title: 'Luxury Sectional Sofa',
                    desc: 'Italian leather finish with premium cushioning',
                    price: '₦850,000',
                    src: 'https://images.unsplash.com/photo-1555041469-a586c61ea9bc?w=400&h=300&fit=crop',
                    type: 'image',
                    date: new Date().toISOString()
                },
                {
                    id: Date.now() + 2,
                    category: 'custom',
                    title: 'Master Bedroom Set',
                    desc: 'Complete bedroom transformation package',
                    price: '₦1,500,000',
                    src: 'https://images.unsplash.com/photo-1505693416388-ac5ce068fe85?w=400&h=300&fit=crop',
                    type: 'image',
                    date: new Date().toISOString()
                }
            ];
            saveData();
        }

        // Export/Import Functions
        function exportData() {
            const data = {
                items: galleryItems,
                exportDate: new Date().toISOString(),
                version: '1.0'
            };
            
            const blob = new Blob([JSON.stringify(data, null, 2)], { type: 'application/json' });
            const url = URL.createObjectURL(blob);
            const a = document.createElement('a');
            a.href = url;
            a.download = 'pz-furniture-backup-' + new Date().toISOString().split('T')[0] + '.json';
            document.body.appendChild(a);
            a.click();
            document.body.removeChild(a);
            URL.revokeObjectURL(url);
            
            showToast('Backup file downloaded!', 'success');
        }

        function importData(input) {
            const file = input.files[0];
            if (!file) return;
            
            const reader = new FileReader();
            reader.onload = (e) => {
                try {
                    const data = JSON.parse(e.target.result);
                    if (data.items && Array.isArray(data.items)) {
                        if (confirm('This will replace all current items. Continue?')) {
                            galleryItems = data.items;
                            saveData();
                            renderGallery();
                            renderAdminItems();
                            updateStats();
                            showToast('Data restored successfully!', 'success');
                        }
                    } else {
                        showToast('Invalid backup file format', 'error');
                    }
                } catch (err) {
                    showToast('Error reading backup file', 'error');
                }
            };
            reader.readAsText(file);
            input.value = '';
        }

        // Admin Panel Functions
        function toggleAdmin() {
            const panel = document.getElementById('adminPanel');
            const overlay = document.getElementById('adminOverlay');
            panel.classList.toggle('active');
            overlay.classList.toggle('active');
            document.body.style.overflow = panel.classList.contains('active') ? 'hidden' : '';
        }

        function switchTab(tab) {
            document.querySelectorAll('.admin-tab').forEach(t => t.classList.remove('active'));
            document.querySelectorAll('.tab-content').forEach(t => t.classList.remove('active'));
            
            event.target.classList.add('active');
            document.getElementById(tab + 'Tab').classList.add('active');
            
            if (tab === 'stats') {
                updateStats();
                checkStorage();
            }
            if (tab === 'items') renderAdminItems();
        }

        // Drag & Drop Upload
        function setupEventListeners() {
            const uploadZone = document.getElementById('uploadZone');
            const fileInput = document.getElementById('fileInput');

            uploadZone.addEventListener('click', () => fileInput.click());
            
            fileInput.addEventListener('change', (e) => handleFiles(e.target.files));

            uploadZone.addEventListener('dragover', (e) => {
                e.preventDefault();
                uploadZone.classList.add('dragover');
            });

            uploadZone.addEventListener('dragleave', () => {
                uploadZone.classList.remove('dragover');
            });

            uploadZone.addEventListener('drop', (e) => {
                e.preventDefault();
                uploadZone.classList.remove('dragover');
                handleFiles(e.dataTransfer.files);
            });
        }

        function handleFiles(files) {
            let validFiles = 0;
            
            Array.from(files).forEach(file => {
                // Check file type
                if (!file.type.match(/image.*|video.*/)) {
                    showToast('Skipped: ' + file.name + ' (not an image/video)', 'error');
                    return;
                }
                
                // Check file size (5MB limit)
                if (file.size > 5 * 1024 * 1024) {
                    showToast('Skipped: ' + file.name + ' (too large, max 5MB)', 'error');
                    return;
                }

                const reader = new FileReader();
                reader.onload = (e) => {
                    // Compress image if it's large
                    if (file.type.startsWith('image') && e.target.result.length > 500000) {
                        compressImage(e.target.result, file.type, (compressed) => {
                            tempFiles.push({
                                src: compressed,
                                type: 'image',
                                name: file.name
                            });
                            renderPreviews();
                        });
                    } else {
                        tempFiles.push({
                            src: e.target.result,
                            type: file.type.startsWith('video') ? 'video' : 'image',
                            name: file.name
                        });
                        renderPreviews();
                    }
                };
                reader.onerror = () => {
                    showToast('Error reading: ' + file.name, 'error');
                };
                reader.readAsDataURL(file);
                validFiles++;
            });
            
            if (validFiles > 0) {
                showToast('Processing ' + validFiles + ' file(s)...', 'success');
            }
        }

        function compressImage(dataUrl, type, callback) {
            const img = new Image();
            img.onload = () => {
                const canvas = document.createElement('canvas');
                const ctx = canvas.getContext('2d');
                
                // Max dimensions
                const maxWidth = 800;
                const maxHeight = 600;
                let width = img.width;
                let height = img.height;
                
                if (width > maxWidth || height > maxHeight) {
                    if (width / height > maxWidth / maxHeight) {
                        height = Math.round(height * maxWidth / width);
                        width = maxWidth;
                    } else {
                        width = Math.round(width * maxHeight / height);
                        height = maxHeight;
                    }
                }
                
                canvas.width = width;
                canvas.height = height;
                ctx.drawImage(img, 0, 0, width, height);
                
                const compressed = canvas.toDataURL(type, 0.7);
                callback(compressed);
            };
            img.src = dataUrl;
        }

        function renderPreviews() {
            const container = document.getElementById('uploadPreview');
            container.innerHTML = tempFiles.map((file, index) => `
                <div class="preview-item">
                    ${file.type === 'video' 
                        ? `<video src="${file.src}" muted></video>`
                        : `<img src="${file.src}" alt="Preview">`
                    }
                    <button class="preview-remove" onclick="removeTempFile(${index})">×</button>
                </div>
            `).join('');
        }

        function removeTempFile(index) {
            tempFiles.splice(index, 1);
            renderPreviews();
        }

        function processUpload() {
            if (tempFiles.length === 0) {
                showToast('Please select files first', 'error');
                return;
            }

            const category = document.getElementById('uploadCategory').value;
            const title = document.getElementById('uploadTitle').value || 'Untitled';
            const priceInput = document.getElementById('uploadPrice').value;
            const price = priceInput ? '₦' + priceInput : 'Contact for price';
            const desc = document.getElementById('uploadDesc').value || '';

            let successCount = 0;
            
            tempFiles.forEach(file => {
                try {
                    const newItem = {
                        id: Date.now() + Math.random(),
                        category,
                        title,
                        desc,
                        price,
                        src: file.src,
                        type: file.type,
                        date: new Date().toISOString()
                    };
                    galleryItems.unshift(newItem);
                    successCount++;
                } catch (e) {
                    console.error('Error adding item:', e);
                }
            });

            if (successCount > 0) {
                saveData();
                renderGallery();
                renderAdminItems();
                updateStats();
                
                // Reset form
                tempFiles = [];
                renderPreviews();
                document.getElementById('uploadTitle').value = '';
                document.getElementById('uploadPrice').value = '';
                document.getElementById('uploadDesc').value = '';
                
                showToast('Successfully added ' + successCount + ' item(s)!', 'success');
            } else {
                showToast('Failed to add items. Storage may be full.', 'error');
            }
        }

        // Gallery Functions
        function renderGallery() {
            const grid = document.getElementById('galleryGrid');
            let filtered = galleryItems;

            if (currentFilter !== 'all') {
                filtered = filtered.filter(item => item.category === currentFilter);
            }

            if (searchQuery) {
                const q = searchQuery.toLowerCase();
                filtered = filtered.filter(item => 
                    item.title.toLowerCase().includes(q) || 
                    item.desc.toLowerCase().includes(q) ||
                    item.category.toLowerCase().includes(q)
                );
            }

            document.getElementById('totalItems').textContent = filtered.length;

            if (filtered.length === 0) {
                grid.innerHTML = `
                    <div class="empty-state">
                        <div class="empty-state-icon">📦</div>
                        <h3>No items found</h3>
                        <p>Try adjusting your filters or search query</p>
                    </div>
                `;
                return;
            }

            grid.innerHTML = filtered.map((item, index) => `
                <div class="gallery-item fade-in" onclick="openLightbox(${index})">
                    <div class="gallery-media">
                        ${item.type === 'video' 
                            ? `<video src="${item.src}" muted loop playsinline></video>`
                            : `<img src="${item.src}" alt="${item.title}" loading="lazy" onerror="this.src='https://via.placeholder.com/400x300/D4AF37/FFFFFF?text=Image+Not+Found'">`
                        }
                        <span class="media-type">${item.type === 'video' ? '▶️' : '📷'}</span>
                        <span class="price-tag">${item.price}</span>
                    </div>
                    <div class="gallery-info">
                        <div class="gallery-meta">
                            <span class="gallery-category">${item.category}</span>
                            <span class="gallery-date">${formatDate(item.date)}</span>
                        </div>
                        <h3>${item.title}</h3>
                        <p>${item.desc}</p>
                    </div>
                    <div class="gallery-actions">
                        <button class="action-btn" onclick="event.stopPropagation(); editItem(${item.id})" title="Edit">✏️</button>
                        <button class="action-btn" onclick="event.stopPropagation(); deleteItem(${item.id})" title="Delete">🗑️</button>
                    </div>
                </div>
            `).join('');

            setupIntersectionObserver();
        }

        function filterGallery(category) {
            currentFilter = category;
            document.querySelectorAll('.filter-btn').forEach(btn => {
                btn.classList.remove('active');
                if (btn.textContent.toLowerCase().includes(category) || (category === 'all' && btn.textContent === 'All')) {
                    btn.classList.add('active');
                }
            });
            renderGallery();
        }

        function searchGallery() {
            searchQuery = document.getElementById('gallerySearch').value;
            renderGallery();
        }

        // Admin Items Management
        function renderAdminItems() {
            const list = document.getElementById('adminItemsList');
            const search = document.getElementById('adminSearch')?.value?.toLowerCase() || '';
            
            let items = galleryItems;
            if (search) {
                items = items.filter(item => 
                    item.title.toLowerCase().includes(search) || 
                    item.category.toLowerCase().includes(search)
                );
            }

            list.innerHTML = items.map(item => `
                <div class="admin-item">
                    <div class="admin-item-media">
                        ${item.type === 'video' 
                            ? `<video src="${item.src}"></video>`
                            : `<img src="${item.src}" alt="${item.title}" onerror="this.src='https://via.placeholder.com/70x70/D4AF37/FFFFFF?text=?'">`
                        }
                    </div>
                    <div class="admin-item-info">
                        <h4>${item.title}</h4>
                        <p>${item.category} • ${item.price} • ${formatDate(item.date)}</p>
                    </div>
                    <div class="admin-item-actions">
                        <button class="icon-btn edit" onclick="editItem(${item.id})" title="Edit">✏️</button>
                        <button class="icon-btn delete" onclick="deleteItem(${item.id})" title="Delete">🗑️</button>
                    </div>
                </div>
            `).join('');
        }

        function filterAdminItems() {
            renderAdminItems();
        }

        function deleteItem(id) {
            if (confirm('Are you sure you want to delete this item?')) {
                galleryItems = galleryItems.filter(item => item.id !== id);
                saveData();
                renderGallery();
                renderAdminItems();
                updateStats();
                showToast('Item deleted successfully', 'success');
            }
        }

        function editItem(id) {
            const item = galleryItems.find(i => i.id === id);
            if (!item) return;

            const newTitle = prompt('Edit title:', item.title);
            if (newTitle === null) return;
            
            const newPrice = prompt('Edit price:', item.price);
            if (newPrice === null) return;
            
            const newDesc = prompt('Edit description:', item.desc);
            if (newDesc === null) return;

            item.title = newTitle || item.title;
            item.price = newPrice || item.price;
            item.desc = newDesc || item.desc;
            
            saveData();
            renderGallery();
            renderAdminItems();
            showToast('Item updated successfully', 'success');
        }

        // Statistics
        function updateStats() {
            const total = galleryItems.length;
            const categories = [...new Set(galleryItems.map(i => i.category))].length;
            const images = galleryItems.filter(i => i.type === 'image').length;
            const videos = galleryItems.filter(i => i.type === 'video').length;

            document.getElementById('statTotal').textContent = total;
            document.getElementById('statCategories').textContent = categories;
            document.getElementById('statImages').textContent = images;
            document.getElementById('statVideos').textContent = videos;

            const categoryCounts = {};
            galleryItems.forEach(item => {
                categoryCounts[item.category] = (categoryCounts[item.category] || 0) + 1;
            });

            const chartContainer = document.getElementById('categoryChart');
            const maxCount = Math.max(...Object.values(categoryCounts), 1);
            
            chartContainer.innerHTML = Object.entries(categoryCounts).map(([cat, count]) => `
                <div class="chart-item">
                    <span class="chart-label">${cat.charAt(0).toUpperCase() + cat.slice(1)}</span>
                    <div class="chart-bar">
                        <div class="chart-fill" style="width: ${(count / maxCount * 100)}%"></div>
                    </div>
                    <span class="chart-value">${count}</span>
                </div>
            `).join('');
        }

        // Lightbox
        function openLightbox(index) {
            const filtered = getFilteredItems();
            currentImageIndex = index;
            const item = filtered[index];
            
            if (!item) return;
            
            const mediaContainer = document.getElementById('lightboxMedia');
            mediaContainer.innerHTML = item.type === 'video'
                ? `<video src="${item.src}" controls autoplay class="lightbox-media"></video>`
                : `<img src="${item.src}" alt="${item.title}" class="lightbox-media" onerror="this.src='https://via.placeholder.com/800x600/D4AF37/FFFFFF?text=Image+Not+Available'">`;
            
            document.getElementById('lightboxInfo').innerHTML = `
                <h3>${item.title}</h3>
                <p>${item.desc}</p>
                <div class="lightbox-price">${item.price}</div>
            `;
            
            document.getElementById('lightbox').classList.add('active');
            document.body.style.overflow = 'hidden';
        }

        function closeLightbox(e) {
            if (e && e.target !== e.currentTarget && e.target.className !== 'lightbox-close') return;
            document.getElementById('lightbox').classList.remove('active');
            document.body.style.overflow = '';
        }

        function changeImage(direction) {
            const filtered = getFilteredItems();
            if (filtered.length === 0) return;
            currentImageIndex = (currentImageIndex + direction + filtered.length) % filtered.length;
            openLightbox(currentImageIndex);
        }

        function getFilteredItems() {
            let filtered = galleryItems;
            if (currentFilter !== 'all') {
                filtered = filtered.filter(item => item.category === currentFilter);
            }
            if (searchQuery) {
                const q = searchQuery.toLowerCase();
                filtered = filtered.filter(item => 
                    item.title.toLowerCase().includes(q) || 
                    item.desc.toLowerCase().includes(q)
                );
            }
            return filtered;
        }

        // Utilities
        function formatDate(dateString) {
            if (!dateString) return 'Recently';
            try {
                const date = new Date(dateString);
                return date.toLocaleDateString('en-NG', { month: 'short', day: 'numeric', year: 'numeric' });
            } catch(e) {
                return 'Recently';
            }
        }

        function showToast(message, type = 'success') {
            const container = document.getElementById('toastContainer');
            const toast = document.createElement('div');
            toast.className = `toast ${type}`;
            toast.innerHTML = `
                <span class="toast-icon">${type === 'success' ? '✅' : '❌'}</span>
                <span>${message}</span>
            `;
            container.appendChild(toast);
            
            setTimeout(() => toast.classList.add('show'), 100);
            setTimeout(() => {
                toast.classList.remove('show');
                setTimeout(() => toast.remove(), 300);
            }, 3000);
        }

        function handleContact(e) {
            e.preventDefault();
            showToast('Message sent successfully! We will contact you soon.', 'success');
            e.target.reset();
        }

        // Intersection Observer
        function setupIntersectionObserver() {
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('visible');
                    }
                });
            }, { threshold: 0.1 });

            document.querySelectorAll('.fade-in').forEach(el => observer.observe(el));
        }

        // Keyboard Navigation
        document.addEventListener('keydown', (e) => {
            if (e.key === 'Escape') closeLightbox();
            if (e.key === 'ArrowLeft') changeImage(-1);
            if (e.key === 'ArrowRight') changeImage(1);
        });

        // Navbar Scroll Effect
        window.addEventListener('scroll', () => {
            const navbar = document.getElementById('navbar');
            if (window.scrollY > 50) {
                navbar.style.boxShadow = '0 4px 30px rgba(0,0,0,0.1)';
            } else {
                navbar.style.boxShadow = '0 4px 30px rgba(0,0,0,0.08)';
            }
        });

        // Smooth Scroll
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({ behavior: 'smooth', block: 'start' });
                }
            });
        });
    </script>
</body>
</html>
