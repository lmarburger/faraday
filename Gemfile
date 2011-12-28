source 'https://rubygems.org'

group :development do
  gem 'sinatra', '~> 1.2'
end

group :test do
  # ActiveSupport::JSON will be used in ruby 1.8 and Yajl in 1.9; this is to test against both adapters
  gem 'activesupport', '~> 2.3', :require => nil, :platforms => [:ruby_18, :jruby]
  gem 'em-http-request', '~> 1.0', :require => 'em-http'
  gem 'em-synchrony', '~> 1.0', :require => ['em-synchrony', 'em-synchrony/em-http'], :platforms => :ruby_19
  gem 'excon', '~> 0.6'
  gem 'leftright', '~> 0.9', :require => false
  gem 'yajl-ruby', '~> 1.0', :require => 'yajl', :platforms => :ruby_19
end

platforms :ruby do
  gem 'patron', '~> 0.4'
  gem 'typhoeus', '~> 0.3'
end

platforms :jruby do
  gem 'jruby-openssl'
  # Once these changes get merged I'll set this to the aesterline's repo
  gem 'jruby-httpclient', :git => 'https://github.com/aesterline/jruby-httpclient.git', :ref => 'ebb9b6e', :require => false, :platforms => :jruby
  gem 'ffi-ncurses', '~> 0.3'
end

gemspec
