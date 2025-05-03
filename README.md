# Meipaly - Smart Web Design Agency Website

## 📌 Overview

**Meipaly** is a modern, responsive website template designed for a smart web design agency. It highlights services, showcases, blogs, statistics, and contact information with a sleek design, animations, and interactive elements. Built using HTML, CSS, and JavaScript, it integrates various libraries to enhance functionality and user experience.

## ✨ Features

- **Responsive Design**: Adapts to different screen sizes (desktop, tablet, mobile).
- **Interactive Animations**: Powered by Animate.css and WOW.js for engaging transitions.
- **Slick Carousel**: Used for displaying services in a slider format.
- **Portfolio Gallery**: Integrated with Fancybox for lightbox image viewing.
- **Counter Animation**: Displays statistics with a custom JavaScript counter effect.
- **Contact Form**: Includes a form and Google Maps integration for user interaction.
- **Video Section**: Showcases a video with a fallback audio option.
- **Custom Fonts**: Uses Oswald from Google Fonts and a custom font (`aztekb.ttf`).
- **Social Media Integration**: Footer links to social media platforms with hover effects.

## 🛠 Technologies Used

- **HTML5**: Semantic markup for structure.
- **CSS3**: Custom styles with flexbox, grid, CSS variables, and animations.
- **JavaScript**: jQuery for DOM manipulation and plugin integration.

### 📚 Libraries and Frameworks

- FontAwesome 6.7.2 for icons.
- Slick Carousel 1.9.0 for sliders.
- Animate.css 4.1.1 for animations.
- WOW.js for scroll-triggered animations.
- Fancybox 5.0 for portfolio lightbox.
- Google Fonts (Oswald) for typography.

### 🌐 External Resources

- CDN-hosted libraries (e.g., jQuery, Slick Carousel, Fancybox).
- Local assets for images, videos, and custom fonts.

## 📁 Project Structure

```
meipaly/
├── css/
│   └── style.css
├── fonts/
│   └── aztekb.ttf
├── img/
│   ├── home_slider.jpg
│   ├── showcase_img_1.webp
│   ├── showcase_img_2.webp
│   ├── ...
│   ├── grid-metro-1.jpg
│   ├── ...
│   ├── video.mp4
│   └── bussiness_img_1.jpg
└── index.html
```

## 🧾 Installation

1. **Clone or Download the repository**:
   ```bash
   git clone <repository-url>
   ```

2. **Navigate to the project directory**:
   ```bash
   cd meipaly
   ```

3. **Open `index.html` in a web browser**:
   - Use a local server (e.g., Live Server in VS Code) for best results, as some features (e.g., video, form submission) may not work correctly with the `file://` protocol.
   - Alternatively, host the files on a web server.

## 🚀 Usage

### 🖼️ Customization

- Replace images in the `img/` folder with your own.
- Update content in `index.html` (e.g., text, links, showcase items).
- Modify `css/style.css` for custom colors, fonts, or layouts.

### 🧩 Adding Showcase Items

- Update the showcase section in `index.html` with new images and descriptions.
- Ensure images are added to the `img/` folder and referenced correctly.

### 🧮 Services Slider

- Add or modify service items in the `.list` section of `index.html`.
- Adjust Slick Carousel settings in the script section if needed.

### ✉️ Contact Form

- Connect the form to a backend service (e.g., Formspree, Node.js) by updating the `<form>` `action` attribute.

### 🎥 Video Section

- Replace the video in `img/video.mp4` with your own media file.

## 🎨 CSS Highlights

### 📌 CSS Variables

Defined in `:root` for consistent typography and colors:

```css
:root {
    --text-primary: #fff;
    --text-base: 16px;
    --text-6xl: 60px;
    --fw-light: 300;
}
```

### 🔤 Fonts

- Uses `aztekb.ttf` (commented out).
- Primary font is **Oswald** from Google Fonts.

### 🔲 Grid Layout

Showcase section uses CSS Grid for a metro-style layout:

```css
.blogs .grid-view {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    gap: 15px;
}
```

### 🌟 Hover Effects & Animations

- Applied to showcase overlays, buttons, and social icons.
- Custom keyframes for carousel arrows and showcase overlays.

## 🧠 JavaScript Highlights

### 🎠 Slick Carousel

Configured for the services section:

```js
$('.list').slick({
    infinite: true,
    slidesToShow: 5,
    dots: true
});
```

### 🖼️ Fancybox

Enables lightbox for showcase images:

```js
Fancybox.bind('[data-fancybox="gallery"]', {
    compact: false,
    contentClick: "iterateZoom",
    Images: {
        Panzoom: {
            maxScale: 2
        }
    }
});
```

### 🔢 Counter Animation

Custom script for animating statistics:

```js
let counts = document.querySelectorAll(".number");
setInterval(() => {
    counts.forEach((count) => {
        let data = +count.getAttribute("data");
        let dataTo = +count.getAttribute("data-to");
        if (data < dataTo) {
            data += 25;
            count.innerHTML = data.toLocaleString();
            count.setAttribute("data", data);
        }
    });
}, 1);
```

### 💫 WOW.js

Initializes scroll animations:

```js
new WOW().init();
```

## 📱 Responsive Design

### 🔍 Breakpoints

- **Mobile**: Adjusts layouts for single-column views (not fully specified in CSS but implied by flex and grid).
- **Tablet/Desktop**: Multi-column layouts for services, showcase, and contact sections.

### 🧩 Key Adjustments

- Services slider (`slidesToShow: 5`) may need responsive settings.
- Showcase grid collapses gracefully on smaller screens (media queries recommended).
- Contact form and map stack vertically on smaller screens.

## 🐞 Known Issues

- **Slick Carousel Responsiveness**: Add responsive breakpoints:

```js
responsive: [
    { breakpoint: 768, settings: { slidesToShow: 3 } },
    { breakpoint: 576, settings: { slidesToShow: 1 } }
]
```

- **Form Submission**: Contact and register forms are static; needs backend integration.
- **Video Playback**: Ensure `video.mp4` is correctly formatted and accessible.
- **Statistics Counter**: Hardcoded values (`data-to="8705"`) repeated across items.
- **Custom Font**: `aztekb.ttf` is commented out; make sure it's functional or remove.

## 🔮 Future Improvements

- Add a **mobile navigation menu** (hamburger menu) for better usability.
- Implement **form validation** and **submission** for contact/register forms.
- Enhance **Slick Carousel** with responsive breakpoints.
- Optimize **images and videos** (e.g., WebP, lazy loading).
- Add **pagination or filtering** for the showcase section.
- Include a **blog section** with dynamic content loading.

## 👨‍🎓 Credits

- **Course**: CyberSoft  
- **Icons**: FontAwesome  
- **Images/Videos**: Placeholder assets (replace with your own for production)

## 📝 License

This project is part of a **CyberSoft course assignment**.  
**All rights reserved © 2021 UI-CYBERSOFT**
