# Portfolio Website Development

A comprehensive guide to building a modern, eye-catching portfolio website using **Vite + React + TypeScript + SCSS**.

## 📁 Project Structure

```
portfolio-website/
├── public/
│   ├── favicon.ico
│   └── profile-photo.jpg (your photo)
├── src/
│   ├── components/
│   │   ├── Header/
│   │   │   ├── Header.tsx
│   │   │   └── Header.scss
│   │   ├── Hero/
│   │   │   ├── Hero.tsx
│   │   │   └── Hero.scss
│   │   ├── About/
│   │   │   ├── About.tsx
│   │   │   └── About.scss
│   │   ├── Skills/
│   │   │   ├── Skills.tsx
│   │   │   └── Skills.scss
│   │   ├── Experience/
│   │   │   ├── Experience.tsx
│   │   │   └── Experience.scss
│   │   ├── Projects/
│   │   │   ├── Projects.tsx
│   │   │   └── Projects.scss
│   │   ├── Contact/
│   │   │   ├── Contact.tsx
│   │   │   └── Contact.scss
│   │   └── Footer/
│   │       ├── Footer.tsx
│   │       └── Footer.scss
│   ├── data/
│   │   ├── personalInfo.ts
│   │   ├── skills.ts
│   │   ├── experience.ts
│   │   ├── projects.ts
│   │   └── education.ts
│   ├── types/
│   │   └── index.ts
│   ├── styles/
│   │   ├── globals.scss
│   │   ├── variables.scss
│   │   └── mixins.scss
│   ├── hooks/
│   │   └── useScrollAnimation.ts
│   ├── utils/
│   │   └── constants.ts
│   ├── App.tsx
│   ├── App.scss
│   ├── main.tsx
│   └── vite-env.d.ts
├── package.json
├── tsconfig.json
├── vite.config.ts
└── README.md
```

## 🚀 Getting Started

### 1. Initialize the Project

```bash
npm create vite@latest portfolio-website -- --template react-ts
cd portfolio-website
npm install
npm install -D sass
```

## 📝 Implementation Guide

### 2. Types Definition (`src/types/index.ts`)

Create TypeScript interfaces for:
- **`PersonalInfo`** - name, title, contact details, social links
- **`Skill`** - name, level, category, icon
- **`Experience`** - company, role, duration, description, technologies
- **`Project`** - name, description, technologies, links, status
- **`Education`** - institution, degree, duration, grade

### 3. Data Files (Dynamic Content)

#### `src/data/personalInfo.ts`
Export an object containing:
- Full name, title, email, phone, location
- Professional summary
- Social media links (LinkedIn, GitHub)
- Profile photo path

#### `src/data/skills.ts`
Export an array of skill objects categorized by:
- **Technical Skills** (GCP, Kubernetes, Docker, etc.)
- **Programming Languages**
- **Databases**
- **Tools & Platforms**

Each skill should have name, proficiency level, and category

#### `src/data/experience.ts`
Export an array with your Zee Entertainment experience:
- Company details
- Role and duration
- Key achievements (use your resume bullet points)
- Technologies used

#### `src/data/projects.ts`
Export an array including:
- Self Service Portal project
- Any other projects you want to showcase
- Include tech stack, description, and links

#### `src/data/education.ts`
Export your IIT Guwahati education details

### 4. Styling Architecture

#### `src/styles/variables.scss`
Define:
- Color palette (primary, secondary, accent colors)
- Typography scales
- Spacing units
- Breakpoints for responsive design
- Animation durations

#### `src/styles/mixins.scss`
Create mixins for:
- Flexbox layouts
- Grid layouts
- Animations (fade-in, slide-up, etc.)
- Responsive breakpoints
- Glassmorphism effects

#### `src/styles/globals.scss`
Set up:
- CSS reset
- Global typography
- Smooth scrolling
- Base animations

### 5. Custom Hooks

#### `src/hooks/useScrollAnimation.ts`
Create a hook that:
- Detects when elements enter viewport
- Triggers animations on scroll
- Returns animation state for components

### 6. Components

#### `src/components/Header/Header.tsx`
Create a sticky navigation with:
- Logo/name
- Navigation menu (smooth scroll to sections)
- Mobile hamburger menu
- Dark/light theme toggle

#### `src/components/Hero/Hero.tsx`
Design a full-screen hero section with:
- Animated greeting text
- Your name and title
- Call-to-action buttons
- Particle animation background or geometric shapes

#### `src/components/About/About.tsx`
Include:
- Professional summary from your data
- Profile photo
- Key highlights in animated cards

#### `src/components/Skills/Skills.tsx`
Create:
- Skill categories as tabs or sections
- Animated progress bars or skill cards
- Hover effects for each skill

#### `src/components/Experience/Experience.tsx`
Design:
- Timeline layout
- Company logos
- Expandable achievement cards
- Technology tags

#### `src/components/Projects/Projects.tsx`
Build:
- Project cards with hover effects
- Tech stack badges
- Live demo and GitHub links
- Filter by technology

#### `src/components/Contact/Contact.tsx`
Include:
- Contact form
- Contact information
- Social media links
- Interactive elements

### 7. Styling Guidelines

For each component's SCSS file, implement:
- **Modern design trends**: Glassmorphism, gradient backgrounds, subtle shadows
- **Animations**: Smooth transitions, hover effects, scroll animations
- **Responsive design**: Mobile-first approach
- **Color scheme**: Dark theme with accent colors
- **Typography**: Modern font pairings, proper hierarchy

### 8. App Structure

#### `src/App.tsx`
Structure your app with:
- Import all components
- Use React.lazy for code splitting
- Implement smooth scrolling between sections
- Add loading states

#### `src/App.scss`
Style the main app container with:
- Full-height sections
- Smooth scrolling behavior
- Section transitions

### 9. Configuration Files

#### Update `vite.config.ts`
Add any necessary plugins or configurations

#### Update `tsconfig.json`
Ensure proper TypeScript configuration

## 🎨 Design Principles

1. **Color Scheme**: Use a dark theme with vibrant accent colors
2. **Animations**: Implement subtle micro-animations and scroll-triggered effects
3. **Layout**: Use CSS Grid and Flexbox for modern layouts
4. **Typography**: Choose contrasting fonts for headers and body text
5. **Visual Hierarchy**: Use size, color, and spacing to guide user attention
6. **Mobile Responsiveness**: Ensure perfect mobile experience

## 🛠️ Development Commands

### Install Dependencies
```bash
npm install
```

### Start Development Server
```bash
npm run dev
```

### Build for Production
```bash
npm run build
```

### Preview Production Build
```bash
npm run preview
```

## ✨ Additional Enhancements

Consider adding:
- **Framer Motion** for advanced animations
- **React Router** for multi-page navigation
- **Email.js** for contact form functionality
- **Intersection Observer** for scroll animations
- **PWA capabilities**

## ✅ Features Checklist

- ✅ Fully dynamic (data-driven)
- ✅ Type-safe with TypeScript
- ✅ Modular and maintainable
- ✅ Modern and eye-catching
- ✅ Responsive across all devices
- ✅ Performance optimized

## 📱 Responsive Breakpoints

```scss
// Mobile First Approach
$mobile: 320px;
$tablet: 768px;
$desktop: 1024px;
$large-desktop: 1440px;
```

## 🎯 Key Goals

- Create a visually stunning portfolio that stands out
- Implement smooth animations and interactions
- Ensure excellent mobile experience
- Maintain clean, organized code structure
- Enable easy content updates through data files

---

**Happy Coding! 🚀**
