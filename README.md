# Shopify Developer Test Task

## Description:
This repository contains the implementation of a custom product showcase slider for the Rueckwand24 Shopify store using SwiperJS. The task was to create a slider section with multiple images that are connected to products and metaobjects. When any image is clicked, the user is redirected to the corresponding product page.

The slider was developed using the SwiperJS library and includes custom styling for pagination and navigation. Additionally, a Shopify schema was created to allow the settings to be accessible and customizable through the Shopify Theme Customizer.

## Task Overview:
- **Metaobject Creation**: 
   - I created a new metaobject named `Product Showcase` in the Shopify Admin. This metaobject contains fields for:
     - Image: The product image.
     - Title: The product title.
     - Subtitle: The product description or subtitle.
     - Product URL: The link to the specific product.
   - I linked this metaobject to products via a `Product Showcase Metaobject Reference` metafield.

- **Adding Block to the Product Template**: 
   - I added a custom block to the `main-product.liquid` file to integrate the metaobject showcase into the product template.
   - This block fetches the `Product Showcase` metaobject data for each product, displaying the image, title, subtitle, and linking the image to the correct product URL.

- **SwiperJS Slider Integration**:
   - I integrated the SwiperJS library into the Shopify theme by adding SwiperJS CDN links for CSS and JavaScript in the `theme.liquid` file.
   - I added a custom slider in the `main-product.liquid` file that dynamically loops through metaobjects and displays them in a slider.
   - I created custom SwiperJS settings for slide navigation and pagination (e.g., number of slides, autoplay, navigation arrows, etc.).
   - The slider is fully customizable through the Shopify Theme Customizer by updating the schema.

- **Product Image Clickable**: 
   - I ensured that each image in the slider is clickable and redirects to the correct product URL by pulling the `product_url` field from the metaobject and using it in the `<a>` tag.

- **Pagination and Navigation Controls**:
   - I customized the pagination and navigation controls to match the design in Figma, using SwiperJS’s built-in navigation functionality. Arrows and pagination bullets were styled to fit the design requirements.

- **Gradient Overlay and Captions**:
   - I added a gradient overlay on each product image for better text readability.
   - I displayed the product title and subtitle on top of the gradient.

## Task Description Provided by Rueckwand24:
Shopify Task description:
Please implement the section shown on the left side. The section is a slider of multiple images, each of these images can have a product and a metaobject item connected to it, and if any of these boxes are clicked then you will be redirected to that product page. For the slider, use the SwiperJS component, with the navigation points and arrows. The settings that are needed should be in the Shopify schema and accessible through the Theme Customizer. For the showcase, you can use the same image that is shown in Figma.

## Time Estimate:
This task took approximately **6-8 hours** to complete, including:
- Setting up the metaobjects in Shopify.
- Coding the product template block and integrating the SwiperJS slider.
- Styling the slider and adding the required functionality.

## Feedback on the Task:
The task was a great opportunity to work with Shopify’s metafields and metaobjects, and integrate SwiperJS for a dynamic product showcase slider. One of the key challenges was ensuring that each product’s metaobject was properly linked and displayed in the slider. However, the flexibility provided by SwiperJS made it easier to meet the design requirements. Overall, it was an enjoyable task and helped me to showcase my abilities in working with Shopify’s theme development and external libraries.

## Files Changed:
- `layout/theme.liquid`: Added SwiperJS CSS and JavaScript links in the header.
- `sections/main-product.liquid`: Added the custom slider code and logic to fetch product data, handle product URLs, and display product information in a carousel.


