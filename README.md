# AI VFX – AI-Powered Video Generator

Transform static images into stunning cinematic videos with AI-powered visual effects. Apply Hollywood-style camera movements, explosive VFX, and creative AI transformations with a single click.

<img width="1401" alt="AI VFX Screenshot" src="https://github.com/user-attachments/assets/082b050d-72d8-4e30-a163-cfd20fdf3945" />

## Features

### Cinematic Camera Moves (50+)
Professional camera movements used in blockbuster films:
- **Orbit Shots** – 360 Orbit, Arc Shot, Hero Run
- **Zoom Effects** – Crash Zoom In/Out, Dolly In/Out
- **Crane Movements** – Crane Up/Down, Overhead Crane
- **Dynamic Shots** – Matrix Shot, Car Chase, Vertigo Effect

### Visual Effects (30+)
Dramatic VFX transformations:
- **Destruction** – Disintegration, Decay Time-Lapse, Building/Car Explosion
- **Elements** – Fire, Electricity, Tornado, Tsunami
- **Supernatural** – Levitate, Flying, Invisibility, Tentacles
- **Transformations** – Robotic Face Reveal, Turning Metal

### AI Effects
Creative AI-powered transformations:
- Kiss Me AI, Venom, Hulk, Muscle Surge, Tiger Touch, and more

### Core Capabilities
- Drag-and-drop image upload or URL input
- Multiple aspect ratios (16:9, 9:16, 1:1)
- Adjustable duration (5s, 10s)
- Resolution options (480p, 720p)
- Quality presets (medium, high)
- Real-time generation status with progress tracking

## Demo Videos

https://github.com/user-attachments/assets/e273d1d7-1793-4f10-a407-d3677677d0bf

https://github.com/user-attachments/assets/cb7e3aaa-987b-4c0c-8e23-97c32637bb97

https://github.com/user-attachments/assets/9b2813d1-6abf-496e-961e-e9014aab31c2

## Tech Stack

| Technology | Purpose |
|------------|---------|
| [Next.js 15](https://nextjs.org/) | React framework with App Router |
| [MuAPI](https://muapi.ai/) | AI VFX generation API |
| [TailwindCSS](https://tailwindcss.com/) | Styling |
| [Vercel](https://vercel.com/) | Deployment |

## Quick Start

### Prerequisites
- Node.js 18+
- MuAPI API key ([Get one here](https://muapi.ai/))

### Installation

```bash
# Clone the repository
git clone https://github.com/SamurAIGPT/AI-VFX.git
cd AI-VFX

# Install dependencies
npm install

# Start development server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### Environment Variables

Create a `.env.local` file in the root directory:

```env
MUAPI_API_KEY=your_api_key_here
```

> Note: Users can also enter their API key directly in the app's modal interface.

## Usage

1. **Select an Effect** – Browse the grid of 80+ effects and click to select
2. **Upload an Image** – Drag & drop, click to upload, or paste an image URL
3. **Add a Prompt** (optional) – Describe additional details for the generation
4. **Configure Settings** – Choose aspect ratio, duration, resolution, and quality
5. **Generate** – Click the send button and wait for your video (typically 1-3 minutes)
6. **Download** – Preview and download your generated video

## Project Structure

```
AI-VFX/
├── app/                    # Next.js App Router
│   ├── page.js            # Main application page
│   ├── layout.js          # Root layout
│   └── globals.css        # Global styles
├── components/
│   └── BottomInputBar.js  # Input controls component
├── hooks/
│   └── useVideoGeneration.js  # Video generation hook
├── pages/api/             # API routes
│   ├── proxy-muapi.js     # MuAPI proxy endpoint
│   └── generate-video.js  # Video generation handler
└── lib/
    └── vadoo.js           # API client utilities
```

## API Reference

### Generate Video
```
POST /api/proxy-muapi
```

**Request Body:**
```json
{
  "prompt": "A cinematic explosion",
  "image_url": "https://example.com/image.jpg",
  "name": "Crash Zoom In",
  "aspect_ratio": "16:9",
  "size": "832*480",
  "quality": "medium",
  "duration": 5
}
```

### Check Status
```
GET /api/proxy-muapi?id={request_id}
```

## Deploy

### One-Click Deploy

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/SamurAIGPT/AI-VFX)

### Manual Deployment

```bash
# Build for production
npm run build

# Start production server
npm start
```

## Live Demo

**Try it now:** [https://video-generator-three-kappa.vercel.app/](https://video-generator-three-kappa.vercel.app/)

## VFX API

Powered by MuAPI – explore the API playground: [https://muapi.ai/playground/vfx](https://muapi.ai/playground/vfx)

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is open source and available under the [MIT License](LICENSE).
