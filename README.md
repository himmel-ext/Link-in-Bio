# Link-in-Bio Next.js Application

A modern, interactive Link-in-Bio application built with Next.js featuring profile showcase, social links, and protected media content.

## Features

- 🎨 Modern UI with Instagram-like gradient design
- 🔗 Multiple social media and website links
- 🔄 Interactive 3D profile image flip
- 🎵 Background music with autoplay
- 🛡️ Media protection against inspection and downloading
- 📱 Fully responsive design
- 🌙 Dark theme optimized interface
- 🎭 Animated transitions and hover effects
- 🚫 Right-click and keyboard shortcut blocking

## Tech Stack

- **Framework**: Next.js 14
- **Language**: JavaScript (React)
- **Styling**: CSS3 with custom properties
- **Fonts**: Google Fonts (Poppins & Victor Mono)
- **Icons**: Font Awesome 6.4
- **Notifications**: SweetAlert2
- **Deployment**: Vercel (recommended)

## Project Structure

```
link-in-bio/
├── pages/
│   ├── _app.js          # Application wrapper
│   └── index.js         # Main page component
├── styles/
│   └── globals.css      # Global styles and CSS variables
├── public/
│   ├── images/          # Profile images folder
│   │   ├── profile-front.jpg
│   │   └── profile-back.jpg
│   └── audio/           # Background music folder
│       └── background-music.mp3
├── package.json         # Dependencies and scripts
└── README.md            # This file
```

## Installation

1. **Clone the repository:**
```bash
git clone <repository-url>
cd link-in-bio
```

2. **Install dependencies:**
```bash
npm install
```

3. **Add media files:**
- Place profile images in `public/images/`
- Place background music in `public/audio/`

4. **Run development server:**
```bash
npm run dev
```

5. **Build for production:**
```bash
npm run build
npm start
```

## Media Protection Features

The application includes several layers of media protection:

- **Right-click blocking** on all media elements
- **Drag & drop prevention** for images
- **Text selection disabled** throughout the application
- **Keyboard shortcut blocking** (F12, Ctrl+Shift+I, etc.)
- **Local file paths** instead of external URLs
- **CSS-based user selection prevention**

## Customization

### Profile Information
Edit the profile data in `pages/index.js`:
```javascript
const profileData = {
  username: "@your_username",
  bio: "Your custom bio text",
  profileImages: {
    front: "/images/your-front-image.jpg",
    back: "/images/your-back-image.jpg"
  }
};
```

### Social Links
Modify the social links array:
```javascript
const socialLinks = [
  { icon: "fab fa-instagram", url: "your-instagram-url" },
  { icon: "fab fa-twitter", url: "your-twitter-url" },
  // Add more social links
];
```

### Main Links
Update the main link buttons:
```javascript
const links = [
  { icon: "fas fa-globe", text: "Website Portfolio", url: "your-website-url" },
  // Add more links
];
```

## Dependencies

- `next`: 14.0.0
- `react`: 18.2.0
- `react-dom`: 18.2.0
- `sweetalert2`: ^11.0.0

## Environment Requirements

- Node.js 16.14.0 or later
- npm 8 or later (or yarn equivalent)

## Deployment

### Vercel (Recommended)
1. Push code to GitHub
2. Import project to Vercel
3. Set environment variables if needed
4. Deploy automatically

### Other Platforms
```bash
npm run build
# Serve the out/ directory
```

## Browser Support

- Chrome 60+
- Firefox 60+
- Safari 12+
- Edge 79+

## Security Notes

⚠️ **Important**: The media protection is client-side only and can be bypassed by determined users. For stronger protection:
- Use server-side authentication
- Implement proper CORS policies
- Use signed URLs for media files
- Add server-side logging

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For support, please open an issue in the GitHub repository or contact the project maintainer.

## Author

Created with ❤️ using Next.js and React.

---
*Note: This is a client-side application. For production use, consider implementing additional server-side security measures.*
