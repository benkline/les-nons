# Les Nons - SvelteKit Project

## Theme
Franco-german-swiss electronic artistry, european punk rebellion, continental soundscapes, artistic noise, cultural fusion, underground rhythms, experimental compositions

## Framework: SvelteKit
Modern, performant framework perfect for creative band websites with smooth animations and interactivity.

## Local Development

### Prerequisites
- Node.js 18+
- npm, yarn, or pnpm

### Setup
```bash
# Install dependencies
npm install

# Start development server
npm run dev
```

Open `http://localhost:5173`

### Available Scripts
- `npm run dev` - Development server with HMR
- `npm run build` - Production build
- `npm run preview` - Preview production build  
- `npm run check` - Type checking
- `npm run lint` - ESLint
- `npm run format` - Prettier formatting

## Project Structure
```
src/
├── lib/          # Shared utilities and components
├── routes/       # File-based routing
├── app.html      # HTML template
└── app.css       # Global styles
```

## Audio Integration
Perfect for band website features:
- Music player components
- Audio visualization
- Streaming integration
- Track listings and albums

## Deployment to Cloudflare Pages

### Git Integration (Recommended)
1. Push to Git repository
2. Connect to Cloudflare Pages
3. Build settings:
   - **Framework preset**: SvelteKit
   - **Build command**: `npm run build`
   - **Build output**: `build`
   - **Node.js version**: 18

### Static Adapter Configuration
Update `svelte.config.js`:
```javascript
import adapter from '@sveltejs/adapter-static';

export default {
  kit: {
    adapter: adapter({
      pages: 'build',
      assets: 'build',
      fallback: undefined,
      precompress: false,
      strict: true
    })
  }
};
```

### Manual Deployment
```bash
# Build for static deployment
npm run build

# Deploy with Wrangler
npx wrangler pages publish build --project-name les-nons
```

### Multiple Domains
Configure all band domains in Cloudflare Pages:
- `les-nons.com`
- `non.band` 
- `nonbots.tv`
- `thenonbots.com`
- `thenons.com`
- `thenonsband.com`

## Band Website Features
- Tour dates and venue listings
- Music streaming integration  
- Photo galleries
- News and blog posts
- Contact and booking forms
- Social media integration
- Mailing list signup

## Performance Benefits
- Minimal bundle size
- Server-side rendering
- Progressive enhancement
- Smooth page transitions
- Component-level CSS