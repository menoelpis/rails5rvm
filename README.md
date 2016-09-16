# Rails 5 Kali Linux Application Using RVM

## Installation Instruction

1. Clean up your system first

$apt-get autoremove

2.whereis ruby – we will install a new version and overwrite the existing version instead of removing it.

ruby: /usr/bin/ruby /usr/lib/ruby /usr/bin/X11/ruby /usr/share/man/man1/ruby.1.gz

If you still want to remove it by any reason then you can use these commands if you want but it’s not recommended😉. Try do $apt-get remove ruby

If ruby are installed from source then you need to do the following to remove them.

rm -rf /usr/local/lib/ruby
rm -rf /usr/lib/ruby
rm -f /usr/local/bin/ruby
rm -f /usr/bin/ruby
rm -f /usr/local/bin/irb
rm -f /usr/bin/irb
rm -f /usr/local/bin/gem
rm -f /usr/bin/gem

3. apt-get install build-essential zlib1g zlib1g-dev libreadline6 libreadline6-dev libssl-dev

$\curl -L https://get.rvm.io | bash -s -- --ignore-dotfiles --autolibs=0 --ruby

[root] $ source /etc/profile.d/rvm.sh
[root] $ type rvm | head -n 1
[root] $ ruby -v
[root] $ rvm gemset use global
[root] $ gem outdated
[root] $ gem update
[root] $ echo “gem: –no-document” >> ~/.gemrc
[root] $ rvm use ruby-2.3.1@rails5.0 --create
[root] $ gem install rails
[root] $ rails -v
[root] $ apt-get install libxslt-dev libxml2-dev
[root] $ sudo apt-get install sqlite3 libsqlite3-dev
[root] $ gem install sqlite3-ruby

