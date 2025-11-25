# Use the official WordPress image for development

FROM wordpress:latest AS development

# Set build arguments
ARG WORDPRESS_SITE_NAME
ARG WORDPRESS_SITE_EMAIL

# Configure environment variables
ENV WORDPRESS_SITE_NAME=$WORDPRESS_SITE_NAME
ENV WORDPRESS_SITE_EMAIL=$WORDPRESS_SITE_EMAIL

# Copy custom wp-content (if any)
COPY wp-content /var/www/html/wp-content

# Set permissions

RUN chown -R www-data:www-data /var/www/html/wp-content

# Expose the WordPress port

EXPOSE 80