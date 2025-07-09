# Use the official Apache HTTP Server image
FROM httpd:2.4

# Copy custom configuration (optional)
COPY ./my-httpd.conf /usr/local/apache2/conf/httpd.conf

# Copy website files to the Apache document root
COPY ./public-html/ /usr/local/apache2/htdocs/
EXPOSE 80
