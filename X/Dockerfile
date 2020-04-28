FROM php:apache                                                                                                         
# Heroku assigns ports dynamically                                                                                      
RUN sed 's/80/${PORT}/g' -i /etc/apache2/sites-available/000-default.conf /etc/apache2/ports.conf                       
# But outside Heroku, let's default to PORT 80                                                                          
ENV PORT=80                                                                                                             
COPY index.php . 
