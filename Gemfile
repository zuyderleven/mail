source "https://rubygems.org"

%w[rspec-core].each do |lib|
  gem lib, :github => "bf4/#{lib}", :branch => "handle_non_utf8_exception_messages"
end
%w[rspec rspec-expectations rspec-mocks rspec-support].each do |lib|
  gem lib, :git => "git://github.com/rspec/#{lib}.git", :branch => "master"
end
gemspec

gem "tlsmail", "~> 0.0.1" if RUBY_VERSION <= "1.8.6"
gem "jruby-openssl", :platforms => :jruby

group :development, :test do
  gem "appraisal", "~> 1.0"
end

# For gems not required to run tests
group :local_development, :test do
  gem "ruby-debug", :platforms => :mri_18
end
