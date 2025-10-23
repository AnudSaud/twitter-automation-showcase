# Twitter Thread Automation Tool

A web application that converts blog articles into Twitter threads using AI and publishes them automatically.

**Note: Source code is private**

## What This Tool Does

This application automates the process of creating Twitter threads from blog content. It monitors RSS feeds, converts articles to tweet threads using AI, and publishes them to Twitter after review.

## Core Functionality

### Content Processing
- Monitors RSS feeds for new blog posts
- Extracts article content and metadata
- Removes duplicate content using content hashing
- Parses full article text for processing

### Thread Generation
- Uses Groq API with Llama 3.3 70B model to convert articles to threads
- Generates 7-8 tweets per thread
- Maintains 20-45 word limit per tweet
- Attempts to match an authoritative and educational writing style
- Finds and suggests relevant hashtags

### Quality Control
- Scores generated content for tone consistency
- Requires minimum tone score before allowing publication
- Provides feedback on content quality
- Allows manual editing of generated threads

### Review Interface
- Three-panel layout: original content, generated thread, Twitter preview
- Individual tweet approval/rejection
- Edit functionality for generated content
- Bulk operations for multiple tweets

### Publishing
- Integrates with Twitter v2 API
- Posts threads in proper sequence
- Handles Twitter rate limits
- Provides error handling and retry logic

## Technical Stack

### Backend
- Python 3.11 with FastAPI
- PostgreSQL 17 with JSONB storage
- SQLAlchemy ORM with async operations
- JWT authentication

### Frontend
- React 18 with hooks
- Tailwind CSS for styling
- Axios for API communication
- Real-time UI updates

### External Services
- Groq API for AI text generation
- Twitter v2 API for publishing
- RSS feed parsing
- Hashtag trend analysis

## System Architecture

The application follows a standard web architecture:
- REST API backend with database persistence
- React frontend with component-based UI
- External API integrations for AI and social media
- Background job processing for RSS monitoring

## Key Features

- **RSS Monitoring**: Checks feeds every 30 minutes for new content
- **AI Integration**: Uses free tier Groq API for text generation
- **Content Review**: Manual approval workflow before publishing
- **Twitter Integration**: Direct posting to Twitter accounts
- **Quality Scoring**: Automated assessment of generated content
- **Multi-user Support**: Designed for team environments

## Deployment

The application is containerized and can be deployed using Docker. It requires:
- PostgreSQL database
- Environment variables for API keys
- Twitter API v2 credentials
- Groq API access

## Development Approach

Built using modern web development practices:
- Type hints and validation in Python
- Component-based React architecture
- Database migrations and version control
- Environment-based configuration
- Structured error handling

## Contact

For inquiries about this project:
- LinkedIn: https://linkedin.com/in/anudsaud
- Email: anudsaud07@gmail.com

---

**Source code is proprietary and not publicly available**
