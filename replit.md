# Cattus Hotel

## Overview

Cattus Hotel is a full-stack web application for a cat hotel and veterinary service business. The application provides a modern, responsive interface for customers to explore services, book appointments, view events, and subscribe to newsletters. Built with Django/Python framework using HTML templates, it demonstrates a complete business solution with booking management, event handling, and customer engagement features.

## User Preferences

Preferred communication style: Simple, everyday language.
User preference: Multi-page navigation structure with separate pages for each section rather than single-page application.

## System Architecture

The application follows a Django-based architecture with server-side templating and modern responsive design:

### Frontend Architecture
- **Framework**: Django Templates with HTML5
- **Styling**: Custom CSS with purple, blue, and white color scheme
- **Navigation**: Multi-page structure with separate routes for each section
- **Responsive Design**: Mobile-first approach with flexible grid systems
- **Interactive Elements**: Vanilla JavaScript for dynamic components

### Backend Architecture
- **Framework**: Django 5.2.4 with Python
- **Database**: SQLite (development) with Django ORM
- **Templates**: Django template engine with inheritance
- **URL Routing**: Django URLconf with app-based namespacing
- **API Endpoints**: Django views for AJAX interactions

## Key Components

### Database Layer
- **ORM**: Django ORM with model-based approach
- **Models**: Defined in `hotel/models.py`
- **Tables**: 
  - `Booking` - Service appointment management with UUID primary keys
  - `Event` - Event and workshop management
  - `NewsletterSubscriber` - Email subscription management
  - `TeamMember` - Team member information
  - `Testimonial` - Customer testimonials
  - `Partnership` - Strategic partnerships
- **Migrations**: Django's built-in migration system

### API Layer
- **Views**: Django function-based views for both pages and API endpoints
- **Endpoints**:
  - `/api/booking/` - Booking creation via AJAX
  - `/api/events/` - Event listings JSON API
  - `/api/newsletter/` - Newsletter subscriptions
- **Validation**: Django model validation and form handling
- **CSRF Protection**: Django's built-in CSRF middleware

### Template Structure
- **Base Template**: `templates/hotel/base.html` with shared navigation and styling
- **Page Templates**: Individual templates for each section
  - `home.html` - Main landing page with facilities, history, team, testimonials
  - `servicios.html` - Services page with integrated booking system
  - `alianzas.html` - Strategic partnerships page
  - `eventos.html` - Special events and activities page

### Business Logic
- **Services**: Four main service categories (Hospedaje, Estética, Medicina Preventiva, Cuidado en Casa)
- **Booking System**: Integrated calendar-based appointment scheduling on services page
- **Event Management**: Dedicated events page with monthly and special annual events
- **Newsletter**: Email subscription functionality
- **Strategic Partnerships**: Dedicated page highlighting collaboration with Gatopia Col

## Page Structure

1. **Home Page** (`/`): Landing page with hero section, facilities, history, team of 4 members, testimonials
2. **Services Page** (`/servicios/`): All four services with integrated booking system and calendar
3. **Partnerships Page** (`/alianzas/`): Strategic partnerships, primarily featuring Gatopia Col collaboration
4. **Events Page** (`/eventos/`): Special events, monthly activities, and educational workshops

## Data Flow

1. **User Navigation**: Multi-page navigation via Django URL routing
2. **Form Submission**: AJAX forms submit to Django API endpoints
3. **Server Processing**: Django views handle requests with model validation
4. **Database Operations**: Django ORM performs database operations
5. **Template Rendering**: Server-side template rendering with context data
6. **Response Handling**: JSON responses for AJAX, redirects for form submissions

## External Dependencies

### Backend Dependencies
- **Django**: Web framework and ORM
- **Pillow**: Image processing capabilities
- **Python-decouple**: Environment variable management
- **WhiteNoise**: Static file serving

### Frontend Styling
- **Custom CSS**: Purple, blue, and white color scheme
- **Responsive Design**: Mobile-first grid systems
- **Web Fonts**: Modern typography stack
- **Icons**: Unicode emojis and symbols

## Deployment Strategy

### Development
- **Local Development**: Django development server with template rendering
- **Auto-reload**: Django's built-in auto-reloading for Python code changes
- **Static Files**: Django's development static file serving

### Production Considerations
- **Static Files**: WhiteNoise for efficient static file serving
- **Database**: SQLite for development, PostgreSQL for production
- **Templates**: Pre-compiled template caching

### Environment Configuration
- **Database**: Django database configuration in settings.py
- **Static Files**: Configured for both development and production
- **Debug Mode**: Environment-based debug settings

### Key Architectural Decisions

1. **Django Framework**: Chosen for rapid development and built-in features (admin, ORM, templates)
2. **Multi-Page Structure**: Separate pages for each section per user preference (vs single-page app)
3. **Server-Side Rendering**: Django templates for better SEO and initial page load performance
4. **Integrated Booking**: Booking system embedded in services page rather than separate page
5. **AJAX Enhancements**: Modern JavaScript for dynamic interactions while maintaining page-based navigation
6. **Responsive Design**: Mobile-first CSS approach with custom grid systems

## Recent Changes (July 29, 2024)

- ✅ Migrated from React/TypeScript to Django/Python framework
- ✅ Created multi-page structure with separate routes for each section
- ✅ Implemented integrated booking system within services page
- ✅ Developed comprehensive home page with facilities, history, team, and testimonials
- ✅ Built dedicated alianzas page featuring Gatopia Col partnership
- ✅ Created eventos page with monthly and annual special events
- ✅ Established Django models for bookings, events, newsletter, team, testimonials
- ✅ Configured Django templates with inheritance and responsive CSS design
- ✅ Set up API endpoints for AJAX booking and newsletter functionality