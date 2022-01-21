# Nginx Configuration for Vue Projects

- Open nginx configuration file
- Search for `try_files $uri $uri/ /index.php?$query_string;`
- Comment that line
- Add this line `try_files $uri $uri/ /index.html;`
- Save the file & that's it