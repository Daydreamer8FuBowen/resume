# Data Analyst Resume

This project contains the source code for my personal resume, deployed as a static website.

## Project Structure

- `data_analyst_resume.html`: Chinese version of the resume.
- `data_analyst_resume_en.html`: English version of the resume.
- `assets/`: Contains static resources (CSS, JS, images, fonts) used by the deployed service.
- `resume/assets/`: A local copy of the `assets` folder. This is used for local testing to mimic the production URL structure where resources are served from `/resume/assets/`.

## Local Development & Testing

The HTML files are configured to use absolute paths for resources, pointing to `/resume/assets/`. To preview the resume locally with working styles and scripts:

1.  **Ensure `resume/assets/` exists**: This folder should contain a copy of the content from `assets/`.
2.  **Serve the project root**: Use a local static file server at the project root.
    *   For example, using Python: `python -m http.server 8000`
3.  **Access the resume**: Open your browser and navigate to:
    *   `http://localhost:8000/data_analyst_resume.html`
    *   `http://localhost:8000/data_analyst_resume_en.html`

The browser will resolve `/resume/assets/...` requests to the `resume/assets/` directory in your local project, ensuring correct rendering.

## Deployment

This project is designed to be deployed on GitHub Pages (Project Pages).

- **Deployment Source**: Root directory.
- **URL Structure**: `https://<username>.github.io/resume/`
    - The `/resume/` path in the URL corresponds to the repository name.
    - Resource links like `/resume/assets/css/style.css` will correctly map to the `assets` folder in the deployed repository.

## Features

- **Bilingual Support**: Toggle between Chinese and English versions.
- **Dynamic QR Code**: Automatically generates a QR code for the current page URL using `qrcode.js`.
- **Responsive Design**: optimized for various screen sizes.
