# 💰 ALATPay Donations WordPress Plugin
The ALATPay Donations plugin provides a lightweight, custom, and secure solution for accepting donations directly on your WordPress site using the ALATPay payment gateway - without requiring WooCommerce.

Need a simple way to collect contributions? This custom-built plugin is your answer. 

| Metadata | Value | 
| ----- | ----- | 
| **Stable Version** | 1.1.0 | 
| **Requires WP** | 6.0 | 
| **Tested Up To** | 6.8 | 
| **License** | GPLv2 or later | 
| **Tags** | donation, fundraising, alatpay, payment gateway, non-profit | 

## 🚀 Key Features

* **Direct ALATPay Integration:** Accept payments via Card, Bank Transfer, Bank Details, and Phone Number using your ALATPay API credentials.

* **Custom Donation Form:** Easily embed a simple, responsive form using a single shortcode.

* **Secure & Lightweight:** Uses modern security features (CSRF protection, input sanitization) and avoids the bloat of a full e-commerce system.

* **Configurable Amounts:** Define suggested donation amounts to guide your donors or allow them to enter a custom value.

* **Clean Architecture:** Built using a modern, class-based structure for stability and future expansion.

## 💾 Installation

1. **Download:** Obtain the plugin zip file for `alatpay-donations`.

2. **Upload:** In your WordPress Admin, go to **Plugins > Add New**, click "Upload Plugin," and upload the zip file.

3. **Activate:** Click "Activate Plugin."

4. **Dependencies:** Ensure your hosting environment meets the minimum requirements (PHP 7.4+ is highly recommended).

## ⚙️ Configuration

After installation, you **must** configure your ALATPay credentials:

1. Go to **Settings > ALATPay Donations** in your WordPress Admin menu.

2. Enter your **ALATPay API Key** and **Business ID**. These credentials authenticate your site with the ALATPay service.

3. Click **Save Settings**.

## 📝 Usage

To display the donation form on any page, post, or widget area that supports shortcodes, use the following:

### Basic Shortcode:

```

[alatpay\_donation\_form]

```

### Customizing Amounts and Text:

You can customize the suggested amounts and the form's display text using attributes:

```

[alatpay_donation_form 
    title="Help Us Reach Our Goal" 
    description="Every Naira counts. Choose an amount or enter your own." 
    amounts="500, 1000, custom, 5000"
]
```

## ❓ Frequently Asked Questions

**Q: Does this plugin require WooCommerce?**
A: No. This plugin is built as a standalone solution for fundraising and does not rely on the WooCommerce cart system.

**Q: How do I handle payment confirmation?**
A: All confirmation is handled by **ALATPay's webhook**. You **MUST configure this webhook** in your ALATPay merchant dashboard to ensure donations are automatically marked as 'successful' on your WordPress site.

**Q: Where can I change the default suggested donation amounts?**
A: You can set the suggested amounts directly within the shortcode by using the `amounts` attribute, separating values with a comma (e.g., `amounts="1000,2000,5000"`).

**Q: How do I allow donors to enter their own amount?**
A: Use the keyword custom within the amounts attribute of the shortcode (e.g., amounts="1000, custom, 5000"). The plugin will automatically render a user input field for that option.

## 📜 Changelog

### 1.1.0

* **Security:** Added server-side validation for donation amounts, names, and emails.

* **Security:** Implemented unique transaction reference generation to prevent replay attacks.

* **Architecture:** Refactored AJAX handler for clearer flow and error logging.

### 1.0.0

* Initial Release. Core functionality for form rendering and API integration framework established.
```