/* ========================================
   PROFESSIONAL THEME SYSTEM - MASTER STYLES
   Modern, scalable, and production-ready
   ======================================== */

/* ----------------------------------------
   1. CSS RESET & BASE
   ---------------------------------------- */
*, *::before, *::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

body {
  font-family: var(--font-primary);
  color: var(--text-primary);
  background: var(--bg-primary);
  line-height: var(--leading-normal);
  transition: background-color var(--transition-base) var(--ease-out);
}

/* ----------------------------------------
   2. DESIGN TOKENS (CSS Variables)
   ---------------------------------------- */
:root {
  /* 🎨 COLOR PALETTE - Navy & Teal (Professional) */
  --primary: #0a192f;
  --primary-light: #172a45;
  --primary-dark: #060f1f;
  --secondary: #64ffda;
  --secondary-dark: #4ad3b3;
  --accent: #ff6b6b;
  
  /* Neutral Colors */
  --bg-primary: #ffffff;
  --bg-secondary: #f8fafc;
  --bg-tertiary: #f1f5f9;
  --bg-dark: #0f172a;
  --text-primary: #1e293b;
  --text-secondary: #475569;
  --text-tertiary: #64748b;
  --text-light: #94a3b8;
  --text-inverse: #f8fafc;
  --border: #e2e8f0;
  --border-dark: #cbd5e1;
  
  /* Status Colors */
  --success: #10b981;
  --success-bg: #d1fae5;
  --warning: #f59e0b;
  --warning-bg: #fef3c7;
  --error: #ef4444;
  --error-bg: #fee2e2;
  --info: #3b82f6;
  --info-bg: #dbeafe;
  
  /* 🎯 TYPOGRAPHY */
  --font-primary: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
  --font-secondary: 'Poppins', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  --font-mono: 'Fira Code', 'JetBrains Mono', 'Courier New', monospace;
  
  /* Font Sizes - Modular Scale 1.250 (Major Third) */
  --text-xs: 0.75rem;    /* 12px */
  --text-sm: 0.875rem;   /* 14px */
  --text-base: 1rem;     /* 16px */
  --text-lg: 1.125rem;   /* 18px */
  --text-xl: 1.25rem;    /* 20px */
  --text-2xl: 1.5rem;    /* 24px */
  --text-3xl: 1.875rem;  /* 30px */
  --text-4xl: 2.25rem;   /* 36px */
  --text-5xl: 3rem;      /* 48px */
  --text-6xl: 3.75rem;   /* 60px */
  --text-7xl: 4.5rem;    /* 72px */
  
  /* Font Weights */
  --font-thin: 100;
  --font-light: 300;
  --font-regular: 400;
  --font-medium: 500;
  --font-semibold: 600;
  --font-bold: 700;
  --font-extrabold: 800;
  
  /* Line Heights */
  --leading-none: 1;
  --leading-tight: 1.25;
  --leading-snug: 1.375;
  --leading-normal: 1.5;
  --leading-relaxed: 1.625;
  --leading-loose: 2;
  
  /* 📏 SPACING (4px base unit) */
  --space-0: 0;
  --space-1: 0.25rem;   /* 4px */
  --space-2: 0.5rem;    /* 8px */
  --space-3: 0.75rem;   /* 12px */
  --space-4: 1rem;      /* 16px */
  --space-5: 1.25rem;   /* 20px */
  --space-6: 1.5rem;    /* 24px */
  --space-8: 2rem;      /* 32px */
  --space-10: 2.5rem;   /* 40px */
  --space-12: 3rem;     /* 48px */
  --space-16: 4rem;     /* 64px */
  --space-20: 5rem;     /* 80px */
  --space-24: 6rem;     /* 96px */
  --space-32: 8rem;     /* 128px */
  --space-40: 10rem;    /* 160px */
  --space-48: 12rem;    /* 192px */
  
  /* 📦 BORDERS & RADII */
  --radius-none: 0;
  --radius-sm: 0.125rem;   /* 2px */
  --radius-base: 0.25rem;  /* 4px */
  --radius-md: 0.375rem;   /* 6px */
  --radius-lg: 0.5rem;     /* 8px */
  --radius-xl: 0.75rem;    /* 12px */
  --radius-2xl: 1rem;      /* 16px */
  --radius-3xl: 1.5rem;    /* 24px */
  --radius-full: 9999px;
  
  /* 🌓 SHADOWS */
  --shadow-sm: 0 1px 2px 0 rgb(0 0 0 / 0.05);
  --shadow-base: 0 1px 3px 0 rgb(0 0 0 / 0.1), 0 1px 2px -1px rgb(0 0 0 / 0.1);
  --shadow-md: 0 4px 6px -1px rgb(0 0 0 / 0.1), 0 2px 4px -2px rgb(0 0 0 / 0.1);
  --shadow-lg: 0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1);
  --shadow-xl: 0 20px 25px -5px rgb(0 0 0 / 0.1), 0 8px 10px -6px rgb(0 0 0 / 0.1);
  --shadow-2xl: 0 25px 50px -12px rgb(0 0 0 / 0.25);
  --shadow-inner: inset 0 2px 4px 0 rgb(0 0 0 / 0.05);
  
  /* Colored Shadows */
  --shadow-primary: 0 10px 15px -3px rgba(10, 25, 47, 0.2);
  --shadow-secondary: 0 10px 15px -3px rgba(100, 255, 218, 0.2);
  --shadow-success: 0 10px 15px -3px rgba(16, 185, 129, 0.2);
  --shadow-error: 0 10px 15px -3px rgba(239, 68, 68, 0.2);
  
  /* 🥂 GLASSMORPHISM */
  --glass-bg: rgba(255, 255, 255, 0.7);
  --glass-border: rgba(255, 255, 255, 0.2);
  --glass-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.15);
  --glass-blur: blur(10px);
  
  /* ⚡ ANIMATIONS */
  --transition-fast: 150ms;
  --transition-base: 250ms;
  --transition-slow: 350ms;
  --transition-slower: 500ms;
  --transition-slowest: 700ms;
  
  --ease-linear: linear;
  --ease-in: cubic-bezier(0.4, 0, 1, 1);
  --ease-out: cubic-bezier(0, 0, 0.2, 1);
  --ease-in-out: cubic-bezier(0.4, 0, 0.2, 1);
  --ease-bounce: cubic-bezier(0.68, -0.55, 0.265, 1.55);
  --ease-elastic: cubic-bezier(0.68, -0.6, 0.32, 1.6);
  
  /* 📱 BREAKPOINTS (for reference) */
  --breakpoint-sm: 640px;
  --breakpoint-md: 768px;
  --breakpoint-lg: 1024px;
  --breakpoint-xl: 1280px;
  --breakpoint-2xl: 1536px;
  
  /* 🔢 Z-INDEX LAYERS */
  --z-negative: -1;
  --z-elevate: 1;
  --z-dropdown: 10;
  --z-sticky: 20;
  --z-fixed: 30;
  --z-modal: 40;
  --z-popover: 50;
  --z-tooltip: 60;
  --z-toast: 70;
}

/* ----------------------------------------
   3. DARK MODE
   ---------------------------------------- */
@media (prefers-color-scheme: dark) {
  :root {
    --bg-primary: #0f172a;
    --bg-secondary: #1e293b;
    --bg-tertiary: #334155;
    --text-primary: #f1f5f9;
    --text-secondary: #cbd5e1;
    --text-tertiary: #94a3b8;
    --text-light: #64748b;
    --border: #334155;
    --border-dark: #475569;
    
    --glass-bg: rgba(15, 23, 42, 0.7);
    --glass-border: rgba(255, 255, 255, 0.1);
    
    --shadow-sm: 0 1px 2px 0 rgb(0 0 0 / 0.3);
    --shadow-base: 0 1px 3px 0 rgb(0 0 0 / 0.4);
    --shadow-md: 0 4px 6px -1px rgb(0 0 0 / 0.5);
  }
}

/* ----------------------------------------
   4. KEYFRAME ANIMATIONS
   ---------------------------------------- */
@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}

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

@keyframes fadeInDown {
  from {
    opacity: 0;
    transform: translateY(-20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes fadeInLeft {
  from {
    opacity: 0;
    transform: translateX(-20px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes fadeInRight {
  from {
    opacity: 0;
    transform: translateX(20px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes scaleIn {
  from {
    opacity: 0;
    transform: scale(0.95);
  }
  to {
    opacity: 1;
    transform: scale(1);
  }
}

@keyframes slideIn {
  from {
    transform: translateX(-100%);
  }
  to {
    transform: translateX(0);
  }
}

@keyframes rotate {
  from { transform: rotate(0deg); }
  to { transform: rotate(360deg); }
}

@keyframes pulse {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.5; }
}

@keyframes bounce {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-10px); }
}

@keyframes shimmer {
  0% { background-position: -1000px 0; }
  100% { background-position: 1000px 0; }
}

/* ----------------------------------------
   5. TYPOGRAPHY UTILITIES
   ---------------------------------------- */
.text-xs { font-size: var(--text-xs); }
.text-sm { font-size: var(--text-sm); }
.text-base { font-size: var(--text-base); }
.text-lg { font-size: var(--text-lg); }
.text-xl { font-size: var(--text-xl); }
.text-2xl { font-size: var(--text-2xl); }
.text-3xl { font-size: var(--text-3xl); }
.text-4xl { font-size: var(--text-4xl); }
.text-5xl { font-size: var(--text-5xl); }
.text-6xl { font-size: var(--text-6xl); }

.font-thin { font-weight: var(--font-thin); }
.font-light { font-weight: var(--font-light); }
.font-regular { font-weight: var(--font-regular); }
.font-medium { font-weight: var(--font-medium); }
.font-semibold { font-weight: var(--font-semibold); }
.font-bold { font-weight: var(--font-bold); }
.font-extrabold { font-weight: var(--font-extrabold); }

.leading-none { line-height: var(--leading-none); }
.leading-tight { line-height: var(--leading-tight); }
.leading-snug { line-height: var(--leading-snug); }
.leading-normal { line-height: var(--leading-normal); }
.leading-relaxed { line-height: var(--leading-relaxed); }
.leading-loose { line-height: var(--leading-loose); }

.font-primary { font-family: var(--font-primary); }
.font-secondary { font-family: var(--font-secondary); }
.font-mono { font-family: var(--font-mono); }

/* Special Text Effects */
.gradient-text {
  background: linear-gradient(135deg, var(--primary), var(--secondary));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.gradient-text-secondary {
  background: linear-gradient(135deg, var(--secondary), var(--accent));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

/* ----------------------------------------
   6. SPACING UTILITIES
   ---------------------------------------- */
/* Margin */
.m-0 { margin: var(--space-0); }
.m-1 { margin: var(--space-1); }
.m-2 { margin: var(--space-2); }
.m-3 { margin: var(--space-3); }
.m-4 { margin: var(--space-4); }
.m-5 { margin: var(--space-5); }
.m-6 { margin: var(--space-6); }
.m-8 { margin: var(--space-8); }
.m-10 { margin: var(--space-10); }
.m-12 { margin: var(--space-12); }
.m-16 { margin: var(--space-16); }

/* Padding */
.p-0 { padding: var(--space-0); }
.p-1 { padding: var(--space-1); }
.p-2 { padding: var(--space-2); }
.p-3 { padding: var(--space-3); }
.p-4 { padding: var(--space-4); }
.p-5 { padding: var(--space-5); }
.p-6 { padding: var(--space-6); }
.p-8 { padding: var(--space-8); }
.p-10 { padding: var(--space-10); }
.p-12 { padding: var(--space-12); }
.p-16 { padding: var(--space-16); }

/* Gap */
.gap-1 { gap: var(--space-1); }
.gap-2 { gap: var(--space-2); }
.gap-3 { gap: var(--space-3); }
.gap-4 { gap: var(--space-4); }
.gap-5 { gap: var(--space-5); }
.gap-6 { gap: var(--space-6); }
.gap-8 { gap: var(--space-8); }
.gap-10 { gap: var(--space-10); }

/* ----------------------------------------
   7. LAYOUT UTILITIES
   ---------------------------------------- */
.container {
  width: 100%;
  max-width: 1280px;
  margin: 0 auto;
  padding: 0 var(--space-4);
}

@media (min-width: 640px) {
  .container { padding: 0 var(--space-6); }
}

@media (min-width: 1024px) {
  .container { padding: 0 var(--space-8); }
}

/* Flexbox */
.flex { display: flex; }
.inline-flex { display: inline-flex; }
.flex-row { flex-direction: row; }
.flex-col { flex-direction: column; }
.flex-wrap { flex-wrap: wrap; }
.flex-nowrap { flex-wrap: nowrap; }

.justify-start { justify-content: flex-start; }
.justify-end { justify-content: flex-end; }
.justify-center { justify-content: center; }
.justify-between { justify-content: space-between; }
.justify-around { justify-content: space-around; }
.justify-evenly { justify-content: space-evenly; }

.items-start { align-items: flex-start; }
.items-end { align-items: flex-end; }
.items-center { align-items: center; }
.items-baseline { align-items: baseline; }
.items-stretch { align-items: stretch; }

.flex-1 { flex: 1 1 0%; }
.flex-auto { flex: 1 1 auto; }
.flex-initial { flex: 0 1 auto; }
.flex-none { flex: none; }

/* Grid */
.grid { display: grid; }
.inline-grid { display: inline-grid; }

.grid-cols-1 { grid-template-columns: repeat(1, minmax(0, 1fr)); }
.grid-cols-2 { grid-template-columns: repeat(2, minmax(0, 1fr)); }
.grid-cols-3 { grid-template-columns: repeat(3, minmax(0, 1fr)); }
.grid-cols-4 { grid-template-columns: repeat(4, minmax(0, 1fr)); }

@media (min-width: 640px) {
  .sm\:grid-cols-2 { grid-template-columns: repeat(2, minmax(0, 1fr)); }
  .sm\:grid-cols-3 { grid-template-columns: repeat(3, minmax(0, 1fr)); }
}

@media (min-width: 768px) {
  .md\:grid-cols-2 { grid-template-columns: repeat(2, minmax(0, 1fr)); }
  .md\:grid-cols-3 { grid-template-columns: repeat(3, minmax(0, 1fr)); }
  .md\:grid-cols-4 { grid-template-columns: repeat(4, minmax(0, 1fr)); }
}

@media (min-width: 1024px) {
  .lg\:grid-cols-3 { grid-template-columns: repeat(3, minmax(0, 1fr)); }
  .lg\:grid-cols-4 { grid-template-columns: repeat(4, minmax(0, 1fr)); }
}

/* Auto-fit grid */
.grid-auto-fit {
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
}

.grid-auto-fill {
  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
}

/* ----------------------------------------
   8. COMPONENT STYLES
   ---------------------------------------- */
/* Buttons */
.btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  padding: var(--space-3) var(--space-6);
  font-size: var(--text-base);
  font-weight: var(--font-medium);
  line-height: var(--leading-none);
  border-radius: var(--radius-lg);
  transition: all var(--transition-base) var(--ease-out);
  cursor: pointer;
  border: none;
  gap: var(--space-2);
  text-decoration: none;
  white-space: nowrap;
}

.btn:disabled {
  opacity: 0.5;
  cursor: not-allowed;
  pointer-events: none;
}

.btn-primary {
  background: var(--primary);
  color: white;
  box-shadow: var(--shadow-md);
}

.btn-primary:hover:not(:disabled) {
  transform: translateY(-2px);
  box-shadow: var(--shadow-lg);
  background: var(--primary-light);
}

.btn-primary:active:not(:disabled) {
  transform: translateY(0);
}

.btn-secondary {
  background: var(--secondary);
  color: var(--primary);
  box-shadow: var(--shadow-md);
}

.btn-secondary:hover:not(:disabled) {
  transform: translateY(-2px);
  box-shadow: var(--shadow-secondary);
  filter: brightness(1.1);
}

.btn-outline {
  background: transparent;
  color: var(--primary);
  border: 2px solid var(--primary);
}

.btn-outline:hover:not(:disabled) {
  background: var(--primary);
  color: white;
}

.btn-ghost {
  background: transparent;
  color: var(--text-primary);
}

.btn-ghost:hover:not(:disabled) {
  background: var(--bg-tertiary);
}

.btn-sm {
  padding: var(--space-2) var(--space-4);
  font-size: var(--text-sm);
  border-radius: var(--radius-md);
}

.btn-lg {
  padding: var(--space-4) var(--space-8);
  font-size: var(--text-lg);
  border-radius: var(--radius-xl);
}

.btn-icon {
  padding: var(--space-3);
  border-radius: var(--radius-full);
}

.btn-block {
  width: 100%;
}

/* Cards */
.card {
  background: var(--bg-primary);
  border-radius: var(--radius-2xl);
  padding: var(--space-6);
  box-shadow: var(--shadow-base);
  transition: all var(--transition-base) var(--ease-out);
  border: 1px solid var(--border);
}

.card:hover {
  transform: translateY(-4px);
  box-shadow: var(--shadow-lg);
  border-color: var(--primary);
}

.card-glass {
  background: var(--glass-bg);
  backdrop-filter: var(--glass-blur);
  border: 1px solid var(--glass-border);
  box-shadow: var(--glass-shadow);
}

.card-glass:hover {
  background: rgba(255, 255, 255, 0.8);
}

.card-header {
  padding-bottom: var(--space-4);
  border-bottom: 1px solid var(--border);
  margin-bottom: var(--space-4);
}

.card-body {
  padding: var(--space-4) 0;
}

.card-footer {
  padding-top: var(--space-4);
  border-top: 1px solid var(--border);
  margin-top: var(--space-4);
}

/* Badges */
.badge {
  display: inline-flex;
  align-items: center;
  padding: var(--space-1) var(--space-3);
  font-size: var(--text-xs);
  font-weight: var(--font-medium);
  border-radius: var(--radius-full);
  line-height: var(--leading-none);
}

.badge-primary {
  background: var(--primary);
  color: white;
}

.badge-secondary {
  background: var(--secondary);
  color: var(--primary);
}

.badge-success {
  background: var(--success-bg);
  color: var(--success);
}

.badge-warning {
  background: var(--warning-bg);
  color: var(--warning);
}

.badge-error {
  background: var(--error-bg);
  color: var(--error);
}

.badge-info {
  background: var(--info-bg);
  color: var(--info);
}

/* Forms */
.form-group {
  margin-bottom: var(--space-4);
}

.form-label {
  display: block;
  margin-bottom: var(--space-2);
  font-size: var(--text-sm);
  font-weight: var(--font-medium);
  color: var(--text-secondary);
}

.form-input {
  width: 100%;
  padding: var(--space-3) var(--space-4);
  font-size: var(--text-base);
  color: var(--text-primary);
  background: var(--bg-primary);
  border: 1px solid var(--border);
  border-radius: var(--radius-lg);
  transition: all var(--transition-fast) var(--ease-out);
}

.form-input:focus {
  outline: none;
  border-color: var(--primary);
  box-shadow: 0 0 0 3px rgba(10, 25, 47, 0.1);
}

.form-input.error {
  border-color: var(--error);
}

.form-input.error:focus {
  box-shadow: 0 0 0 3px rgba(239, 68, 68, 0.1);
}

.form-input:disabled {
  background: var(--bg-tertiary);
  cursor: not-allowed;
}

.form-hint {
  margin-top: var(--space-2);
  font-size: var(--text-sm);
  color: var(--text-tertiary);
}

.form-error {
  margin-top: var(--space-2);
  font-size: var(--text-sm);
  color: var(--error);
}

/* Alerts */
.alert {
  padding: var(--space-4);
  border-radius: var(--radius-lg);
  margin-bottom: var(--space-4);
  border: 1px solid transparent;
}

.alert-success {
  background: var(--success-bg);
  color: var(--success);
  border-color: var(--success);
}

.alert-warning {
  background: var(--warning-bg);
  color: var(--warning);
  border-color: var(--warning);
}

.alert-error {
  background: var(--error-bg);
  color: var(--error);
  border-color: var(--error);
}

.alert-info {
  background: var(--info-bg);
  color: var(--info);
  border-color: var(--info);
}

/* Navigation */
.nav {
  display: flex;
  align-items: center;
  gap: var(--space-6);
}

.nav-link {
  color: var(--text-secondary);
  text-decoration: none;
  font-weight: var(--font-medium);
  transition: color var(--transition-fast) var(--ease-out);
  position: relative;
}

.nav-link:hover {
  color: var(--primary);
}

.nav-link.active {
  color: var(--primary);
}

.nav-link.active::after {
  content: '';
  position: absolute;
  bottom: -4px;
  left: 0;
  width: 100%;
  height: 2px;
  background: var(--primary);
  border-radius: var(--radius-full);
}

/* ----------------------------------------
   9. SECTION STYLES
   ---------------------------------------- */
.section {
  padding: var(--space-16) var(--space-4);
}

.section-sm {
  padding: var(--space-8) var(--space-4);
}

.section-lg {
  padding: var(--space-24) var(--space-4);
}

.section-title {
  font-size: var(--text-4xl);
  font-weight: var(--font-bold);
  color: var(--text-primary);
  margin-bottom: var(--space-8);
  position: relative;
}

.section-title::after {
  content: '';
  position: absolute;
  bottom: -10px;
  left: 0;
  width: 80px;
  height: 4px;
  background: var(--primary);
  border-radius: var(--radius-full);
}

.section-title.center {
  text-align: center;
}

.section-title.center::after {
  left: 50%;
  transform: translateX(-50%);
}

.section-subtitle {
  font-size: var(--text-xl);
  color: var(--text-secondary);
  margin-bottom: var(--space-12);
  max-width: 600px;
}

.section-subtitle.center {
  margin-left: auto;
  margin-right: auto;
  text-align: center;
}

/* ----------------------------------------
   10. ANIMATION UTILITIES
   ---------------------------------------- */
.animate-fade-in {
  animation: fadeIn var(--transition-slow) var(--ease-out);
}

.animate-fade-up {
  animation: fadeInUp var(--transition-slow) var(--ease-out);
}

.animate-fade-down {
  animation: fadeInDown var(--transition-slow) var(--ease-out);
}

.animate-fade-left {
  animation: fadeInLeft var(--transition-slow) var(--ease-out);
}

.animate-fade-right {
  animation: fadeInRight var(--transition-slow) var(--ease-out);
}

.animate-scale {
  animation: scaleIn var(--transition-slow) var(--ease-out);
}

.animate-pulse {
  animation: pulse 2s var(--ease-in-out) infinite;
}

.animate-bounce {
  animation: bounce 2s var(--ease-bounce) infinite;
}

.animate-spin {
  animation: rotate 1s linear infinite;
}

/* Transition Utilities */
.transition-all { transition: all var(--transition-base) var(--ease-out); }
.transition-transform { transition: transform var(--transition-base) var(--ease-out); }
.transition-opacity { transition: opacity var(--transition-base) var(--ease-out); }
.transition-colors { transition: background-color var(--transition-base) var(--ease-out), border-color var(--transition-base) var(--ease-out), color var(--transition-base) var(--ease-out); }
.transition-shadow { transition: box-shadow var(--transition-base) var(--ease-out); }

/* Hover Effects */
.hover-lift {
  transition: transform var(--transition-base) var(--ease-out);
}

.hover-lift:hover {
  transform: translateY(-4px);
}

.hover-scale {
  transition: transform var(--transition-base) var(--ease-out);
}

.hover-scale:hover {
  transform: scale(1.05);
}

.hover-glow {
  transition: box-shadow var(--transition-base) var(--ease-out);
}

.hover-glow:hover {
  box-shadow: var(--shadow-primary);
}

.hover-border {
  position: relative;
  overflow: hidden;
}

.hover-border::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 2px;
  background: var(--primary);
  transform: translateX(-100%);
  transition: transform var(--transition-base) var(--ease-out);
}

.hover-border:hover::after {
  transform: translateX(0);
}

/* ----------------------------------------
   11. BACKGROUND UTILITIES
   ---------------------------------------- */
.bg-primary { background: var(--primary); }
.bg-secondary { background: var(--secondary); }
.bg-accent { background: var(--accent); }
.bg-white { background: var(--bg-primary); }
.bg-light { background: var(--bg-secondary); }
.bg-dark { background: var(--bg-dark); }
.bg-gradient {
  background: linear-gradient(135deg, var(--primary), var(--secondary));
}
.bg-gradient-secondary {
  background: linear-gradient(135deg, var(--secondary), var(--accent));
}

/* ----------------------------------------
   12. TEXT COLOR UTILITIES
   ---------------------------------------- */
.text-primary { color: var(--text-primary); }
.text-secondary { color: var(--text-secondary); }
.text-tertiary { color: var(--text-tertiary); }
.text-light { color: var(--text-light); }
.text-inverse { color: var(--text-inverse); }
.text-success { color: var(--success); }
.text-warning { color: var(--warning); }
.text-error { color: var(--error); }
.text-info { color: var(--info); }

/* ----------------------------------------
   13. BORDER UTILITIES
   ---------------------------------------- */
.border { border: 1px solid var(--border); }
.border-2 { border-width: 2px; }
.border-4 { border-width: 4px; }
.border-primary { border-color: var(--primary); }
.border-secondary { border-color: var(--secondary); }
.rounded-none { border-radius: var(--radius-none); }
.rounded-sm { border-radius: var(--radius-sm); }
.rounded { border-radius: var(--radius-lg); }
.rounded-lg { border-radius: var(--radius-xl); }
.rounded-xl { border-radius: var(--radius-2xl); }
.rounded-full { border-radius: var(--radius-full); }

/* ----------------------------------------
   14. SHADOW UTILITIES
   ---------------------------------------- */
.shadow-none { box-shadow: none; }
.shadow-sm { box-shadow: var(--shadow-sm); }
.shadow { box-shadow: var(--shadow-base); }
.shadow-md { box-shadow: var(--shadow-md); }
.shadow-lg { box-shadow: var(--shadow-lg); }
.shadow-xl { box-shadow: var(--shadow-xl); }
.shadow-2xl { box-shadow: var(--shadow-2xl); }
.shadow-inner { box-shadow: var(--shadow-inner); }
.shadow-primary { box-shadow: var(--shadow-primary); }
.shadow-secondary { box-shadow: var(--shadow-secondary); }

/* ----------------------------------------
   15. DISPLAY UTILITIES
   ---------------------------------------- */
.block { display: block; }
.inline-block { display: inline-block; }
.inline { display: inline; }
.hidden { display: none; }

/* Visibility */
.visible { visibility: visible; }
.invisible { visibility: hidden; }

/* Overflow */
.overflow-hidden { overflow: hidden; }
.overflow-auto { overflow: auto; }
.overflow-scroll { overflow: scroll; }
.overflow-visible { overflow: visible; }

/* ----------------------------------------
   16. POSITION UTILITIES
   ---------------------------------------- */
.relative { position: relative; }
.absolute { position: absolute; }
.fixed { position: fixed; }
.sticky { position: sticky; }
.static { position: static; }

/* Z-Index */
.z-negative { z-index: var(--z-negative); }
.z-0 { z-index: 0; }
.z-10 { z-index: var(--z-elevate); }
.z-20 { z-index: var(--z-dropdown); }
.z-30 { z-index: var(--z-sticky); }
.z-40 { z-index: var(--z-fixed); }
.z-50 { z-index: var(--z-modal); }

/* ----------------------------------------
   17. RESPONSIVE UTILITIES
   ---------------------------------------- */
/* Hide on mobile */
@media (max-width: 639px) {
  .hidden-mobile { display: none; }
}

/* Hide on tablet */
@media (min-width: 640px) and (max-width: 1023px) {
  .hidden-tablet { display: none; }
}

/* Hide on desktop */
@media (min-width: 1024px) {
  .hidden-desktop { display: none; }
}

/* ----------------------------------------
   18. PRINT STYLES
   ---------------------------------------- */
@media print {
  .no-print { display: none; }
  body { background: white; }
  a[href]::after { content: " (" attr(href) ")"; }
}

/* ----------------------------------------
   19. ACCESSIBILITY
   ---------------------------------------- */
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: now
