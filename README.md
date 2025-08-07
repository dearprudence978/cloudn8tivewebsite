# Cloudn8tive Website

> AI Observability, Human-in-the-Loop & SRE Services

[![Live Site](https://img.shields.io/badge/🌐_Live_Site-www.cloudn8tive.com-green)](https://www.cloudn8tive.com)
[![Google Analytics](https://img.shields.io/badge/Analytics-Google_Analytics_4-blue)](https://analytics.google.com)

## Overview

This is the official website for **Cloudn8tive**, a company providing AI observability, Human-in-the-Loop (HITL), and SRE services. The website is built as a pure HTML/CSS/JavaScript application with no build process or external dependencies.

## 🚀 Features

- **📱 Fully Responsive Design** - Mobile-first approach with Tailwind CSS
- **📊 Google Analytics 4 Integration** - Comprehensive visitor tracking and behavior analysis  
- **📝 Contact Form** - Cloud Run backend integration with SendGrid email delivery
- **🎯 Service Modals** - Interactive showcases for all six service offerings
- **👥 Partner Logos** - Showcase of technology partnerships
- **⚡ Performance Optimized** - CDN delivery, image optimization, and caching
- **🔍 SEO Optimized** - Structured data, meta tags, and semantic HTML

## 🛠 Tech Stack

- **Frontend**: Pure HTML5, CSS3, JavaScript (ES6+)
- **Styling**: [Tailwind CSS](https://tailwindcss.com) (CDN)
- **Icons**: [Font Awesome](https://fontawesome.com)
- **Fonts**: [Google Fonts](https://fonts.google.com) (Inter)
- **Analytics**: Google Analytics 4
- **Backend**: Google Cloud Run (contact form)
- **Email**: SendGrid API
- **Hosting**: Google Cloud Storage + Load Balancer + CDN

## 📊 Analytics & Tracking

The website includes comprehensive visitor intelligence:

### Core Analytics
- Real-time visitor tracking
- Page views and sessions  
- Visitor demographics and locations
- Traffic sources and campaigns
- Device and browser analytics

### Custom Events
- **Contact Form**: Submission attempts, successes, failures
- **Service Modals**: Which services generate most interest
- **CTA Buttons**: "Book a Call" and "Book Consultation" clicks  
- **Partner Logos**: Technology partnership engagement
- **Navigation**: Section visits and user journey
- **Engagement**: Scroll depth (25%, 50%, 75%, 100%) and time on page

## 🏗 Architecture

```
/
├── index.html          # Main website file (self-contained)
├── images/            # Image assets
│   ├── Color logo - no background.png
│   ├── Color logo PSC- no background.png  
│   ├── Coralogix-green-horizontal.png
│   ├── Daco_5435433.png
│   ├── flavicon.png
│   ├── pngaaa.com-1486415.png
│   └── pngaaa.com-5125583.png
├── CLAUDE.md          # Development guidelines
├── .gitignore         # Git ignore rules
└── README.md          # This file
```

## 🎯 Services Offered

1. **AI & LLM Observability** - End-to-end monitoring and insights
2. **Human-in-the-Loop (HITL)** - Expert human oversight for AI systems  
3. **Human-Run Disaster Recovery** - AI-era resilience and continuity
4. **Manned AI Sandboxes** - Safe testing and validation environments
5. **Managed BPO Services** - Philippines-based business process outsourcing
6. **DevOps, SRE & Platform Engineering** - Cloud-native infrastructure expertise

## 🚀 Development

### Local Development
No build process required:
```bash
# Simply open index.html in your browser
open index.html
```

### Deploy to Google Cloud Storage
```bash
# Upload files
gsutil cp index.html gs://www.cloudn8tive.com/
gsutil -m cp -r images gs://www.cloudn8tive.com/

# Invalidate CDN cache  
gcloud compute url-maps invalidate-cdn-cache cloudn8tive-lb --path="/index.html"
```

## 📧 Contact Form Integration

The contact form integrates with:
- **Google Cloud Run** service for processing
- **SendGrid API** for email delivery
- **Google Analytics** for conversion tracking

Environment variables required:
- `SENDGRID_API_KEY`
- `TO_EMAIL=info@cloudn8tive.com`  
- `FROM_EMAIL=benr@cloudn8tive.com`

## 🔧 Configuration

### Google Analytics
- **Property**: My Website
- **Measurement ID**: `G-GLM3MKHW6G`  
- **Stream URL**: https://www.cloudn8tive.com

### DNS & Hosting
- **Domain**: cloudn8tive.com (managed via Google Cloud DNS)
- **CDN**: Google Cloud CDN with caching
- **SSL**: Google-managed SSL certificate
- **Load Balancer**: HTTPS with apex domain redirect

## 📱 Mobile Optimization

Special mobile optimizations:
- Partner logos display in single column on mobile (vs 2x2 grid on desktop)
- Responsive navigation with hamburger menu
- Touch-optimized buttons and modals
- Optimized images and loading

## 🔒 Privacy & Compliance

- **GDPR Compliant**: Anonymous analytics tracking
- **Privacy Policy**: Included in site footer
- **Terms of Service**: Available via modal
- **Cookie Notice**: Integrated with Google Analytics

## 📈 Performance

- **CDN Caching**: 1-hour TTL with manual invalidation
- **Image Optimization**: Compressed assets with fallbacks
- **Lazy Loading**: Implemented for non-critical resources  
- **Minification**: Single-file architecture reduces HTTP requests

## 🤝 Contributing

This website is managed by the Cloudn8tive team. For updates or modifications, please contact [info@cloudn8tive.com](mailto:info@cloudn8tive.com).

## 📄 License

Copyright © 2025 Cloudn8tive. All rights reserved.

---

**Built with ❤️ and AI assistance from [Claude Code](https://claude.ai/code)**