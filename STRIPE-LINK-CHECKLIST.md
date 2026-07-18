# Stripe Link Checklist

For every product: create a one-time Payment Link, collect customer email, set metadata `product_id` to the exact product slug, and redirect after payment to `success.html?session_id={CHECKOUT_SESSION_ID}`. Paste each link into `public-site/assets/js/config.js`.
