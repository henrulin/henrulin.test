hlin.co
=======
Personal blog, generated by Jekyll.

Fonts:
https://icomoon.io/app/

Gems:
bourbon
jekyll-assets

Install and upgrade:
====================
# installing fresh jekyll
sudo apt-get install ruby-full
gem install jekyll
gem install bundle

# upgrade site from Jekyll 2.x to 3.x
>> inside site directory
bundle update
bundle update jekyll

>> possibly add redcarpet into Gemfile and install gem


# command to get site specific gems if they are missing
jekyll build 2>&1 | grep "Could not find" | awk -F'Could not find ' '{print $2}' | awk '{print $1}' | sed 's/\(.*\)-/\1 /' | awk '{print "gem install " $1 " -v " $2}' | source  /dev/stdin
