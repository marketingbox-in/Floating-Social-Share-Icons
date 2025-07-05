# Floating Social Share Buttons for WordPress (Global Implementation)

This project provides a simple, responsive, and globally implemented set of floating social share buttons designed for WordPress websites. These buttons stick to the left side of the viewport, making it easy for users to share your content on popular social media platforms like Facebook, Twitter, LinkedIn, and WhatsApp.

The implementation is designed to be added directly into your WordPress theme's `header.php` or `footer.php` file, or via a plugin that allows site-wide custom HTML/CSS/JS injection, ensuring the buttons appear on all posts and pages.

## ✨ Features

* **Floating Position:** Buttons are `position: fixed;` to stay visible as the user scrolls.
* **Vertically Centered:** Automatically centers itself vertically on the left side of the screen.
* **Responsive Design:** Adapts to various screen sizes, maintaining its visibility on all devices.
* **Popular Platforms:** Includes sharing options for Facebook, Twitter, LinkedIn, and WhatsApp.
* **Dynamic URL/Title:** Automatically retrieves the current page's URL and title for accurate sharing.
* **Modern Styling:** Utilizes Tailwind CSS for utility-first styling and Font Awesome for crisp social media icons.
* **Subtle Hover Effects:** Buttons slightly enlarge on hover for a better user experience.

## 🚀 Installation (WordPress Global Implementation)

To make these floating social share buttons appear on **all** posts and pages of your WordPress site, you need to inject the provided code block into a file that's loaded globally.

**Important:** Modifying theme files directly can lead to lost changes upon theme updates. It is highly recommended to use a **Child Theme** or a **Custom Code Plugin** for safer implementation.

### Method 1: Using a Custom Code Plugin (Recommended for Non-Developers)

Many WordPress plugins allow you to inject custom HTML, CSS, and JavaScript site-wide without modifying theme files. This is generally the safest and easiest method.

1.  **Install a Plugin:** Search for and install a plugin like "Insert Headers and Footers," "Custom CSS, JavaScript & PHP," or similar from the WordPress Plugin Directory.
2.  **Activate the Plugin.**
3.  **Paste the Code:** Navigate to the plugin's settings page.
    * Paste the **entire code block** (including `script` and `style` tags, and the main `div` structure) into the section designated for "Header Scripts" or "Footer Scripts." If there's a specific HTML injection area, use that.
    * **Ensure the code starts with the `` comment and ends after the final `</script>` tag.**
4.  **Save Changes.**

### Method 2: Adding to Your Theme's `header.php` or `footer.php` (For Developers)

If you're comfortable editing theme files (and ideally using a child theme):

1.  **Access Theme Files:**
    * Via FTP/SFTP: Connect to your website's server and navigate to `wp-content/themes/your-theme-name/`.
    * Via WordPress Admin (Appearance > Theme File Editor): **Use with extreme caution.**
2.  **Open `header.php` or `footer.php`:**
    * **For `header.php`:** Paste the entire code block just before the closing `</head>` tag.
    * **For `footer.php`:** Paste the entire code block just before the closing `</body>` tag.
3.  **Save Changes.**

## 🛠️ Customization

### Styling (CSS)

The basic styling is handled via direct `style` tags and Tailwind CSS classes.

* **Positioning:**
    * Modify `top`, `left`, and `transform` properties within the `#floating-social-share-container-blog` style block to adjust the position (e.g., change `left: 5px;` to `right: 5px;` to float on the right).
* **Colors:**
    * Change the `background-color` values for `.facebook-bg`, `.twitter-bg`, etc., in the `<style>` block to match your brand colors.
* **Responsiveness:**
    * The commented-out media query in the CSS provides an example of how you could change the layout for smaller screens (e.g., move to the bottom, change to a row layout). Uncomment and modify this section as needed.

### Icons

* The icons are powered by Font Awesome 6.0.0-beta3. You can change the `<i>` tags' `class` attributes (e.g., `fab fa-facebook-f`) to other Font Awesome icons.
* If you need different icons, you may need to update the Font Awesome CDN link to a newer version or include a different icon library.

### Social Media Platforms

* To add more social media buttons (e.g., Pinterest, Reddit):
    1.  Add a new `<a>` tag with appropriate Tailwind classes and a new background color class in the HTML section.
    2.  Add a corresponding Font Awesome `<i>` tag for the new icon.
    3.  In the JavaScript `updateShareLinks()` function, add new `if` block and URL construction logic for the new platform's sharing endpoint.

## ⚙️ Technologies Used

* **HTML5:** Structure of the buttons.
* **CSS3:** Custom styling and layout.
* **JavaScript (ES6+):** Dynamic URL/title fetching and link generation.
* **Tailwind CSS:** Utility-first CSS framework for rapid styling.
* **Font Awesome:** Icon library for social media brand icons.

## 🤝 Contributing

This is a simple, self-contained solution. If you find issues or have suggestions, please feel free to:

1.  **Open an Issue:** Describe the bug or feature request.
2.  **Fork the Repository:** Make your changes and submit a pull request.

## 📄 License

This code is distributed under the MIT License. See the `LICENSE` file for more information.

## 📧 Contact

If you have questions or need assistance, feel free to reach out. marketingboxofficial@gmail.com


