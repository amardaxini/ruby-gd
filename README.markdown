
ruby-gd gem try to make ruby 1.9.2 compatible

I have just figured out that in ruby >1.9 io.h i.e ruby less than 1.9 (rubyio.h)
rb_io_t structure has replace path variable with pathv variable.

After Installing 
# sudo apt-get install libgd-ruby 
# sudo apt-get install libpng-dev 
# sudo apt-get install libgd2-xpm-dev 
# sudo apt-get install libjpeg-dev
# sudo apt-get install libfreetype-dev 


Then try this

# ruby extconf.rb --with-xpm --with-ttf --with-freetype --with-jpeg  --enable-gd2_0
 
Then Do follwing steps
# rake gem
# gem install pkg/ruby-gd-0.8.0.gem


