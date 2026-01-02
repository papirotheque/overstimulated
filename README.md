# Overstimulated - Master's Thesis Project

Overstimulated is an interactive web-based experience developed as the creative component of my Master's Thesis. The project serves as a visual and sensory exploration of neurodivergence, specifically focusing on my personal autistic experience.

This piece was displayed on a big screen with access to a mouse and a sign that said **"scroll & click"**.

Through four distinct interactive modules: **Hyperfixation, Sensory Overload, Masking, and Alienation**, the project aims to translate abstract internal states into a tangible digital narrative. Leaving the person interacting with the piece all the freedom they want to get into and out of the experience whenever and however they want, for the next person to experience it their own way.

**Live Demo:** [https://papirotheque.github.io/overstimulated/](https://papirotheque.github.io/overstimulated/)

**Full Research and Creative Process:** [papiro.space/blog/posts/overstimulated/](https://papiro.space/blog/posts/overstimulated/)

<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/9c6fa330-026b-4718-b76d-ef62ca646a5b" />


## Technical Implementation

The project is built using native web technologies. It was not designed for mobile devices, since it was displayed on a big screen in an exhibition. I've taken the chance to adapt it as much as I could without modifying the project itself.

### Core Technologies
- **HTML5:** Semantic structure for a multi-page interactive narrative.
- **CSS3:** - **Layering & Depth:** Extensive use of `z-index` and absolute positioning to create a 2.5D environment.
  - **Visual Blending:** Implementation of `mix-blend-mode: lighten` to merge text and textures organically with background assets.
  - **Layout:** Flexbox-based responsive grid for the project index.
- **Vanilla JavaScript:** Custom logic for real-time DOM manipulation based on user input (scroll events).

### Key Features

#### Custom Parallax Engine
To simulate the feeling of depth and overwhelming stimuli, the sub-pages utilize a parallax scrolling mechanism. This is implemented through a scroll event listener that calculates vertical offsets and applies unique movement ratios to different layers:

```javascript
window.addEventListener('scroll', function() {
    var value = window.scrollY;
    bg.style.top = value * 0.4 + 'px';
    mountain.style.top = -value * 0.1 + 'px';
    front.style.top = value * 0.15 + 'px';
});
```

## Project Structure

- `index.html`: The main landing page and module selection.
    
- `hyperfixation.html`, `overload.html`, `masking.html`, `alienation.html`: Individual interactive experiences.
    
- `styleindex.css`: Styles for the index and responsive grid.
    
- `style.css`: Global visual framework and parallax layer settings.
    
- `/images`: Directory containing all visual assets and textures for the experience.

## Intellectual Property & Licensing

The images I created are my own, it took a lot of time and effort to put everything together, yet I wanted to make my project public so other people can use my code freely.

This project uses a dual-licensing model to protect different types of intellectual property:

- **Code:** The source code (HTML, CSS, JS) is licensed under the **MIT License**. You are free to use and modify it for your own projects.
    
- **Visual Assets:** All images, illustrations, and artworks contained in the `/images` folder are licensed under **Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0)**.
    
    - **Attribution:** You must give appropriate credit.
        
    - **Non-Commercial:** You may not use these assets for commercial purposes.
        
    - **No Derivatives:** If you remix, transform, or build upon the material, you may not distribute the modified material.
        
For the full licenses, check the licensing files in the repo.
For any inquiries regarding the use of the artwork beyond these terms, please contact me.
