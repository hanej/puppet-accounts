source "https://rubygems.org"

group :test do
  gem "rake"
  gem "puppet", ENV['PUPPET_VERSION'] || ['> 3.3.0','< 5.0']
  gem "rspec", '< 3.2.0'
  gem 'rspec-puppet', '~> 2.3.0'
  gem "puppetlabs_spec_helper"
  gem "metadata-json-lint"
  gem "rspec-puppet-facts"
  gem 'rubocop', '0.33.0'
  gem 'simplecov', '>= 0.11.0'
  gem 'simplecov-console'
  gem 'deep_merge'
  gem 'librarian-puppet' , '>=2.0'
  # newer versions require ruby 2.2
  gem 'listen', '< 3.1'
  if RUBY_VERSION =~ /^1\.9\./ or RUBY_VERSION =~ /^1\.8\./
    gem 'json', '< 2.0' # newer versions requires at least ruby 2.0
    gem 'json_pure', '< 2.0.0'
    gem 'fog-google', '< 0.1.1'
  end
  gem "puppet-lint-absolute_classname-check"
  gem "puppet-lint-leading_zero-check"
  gem "puppet-lint-trailing_comma-check"
  gem "puppet-lint-version_comparison-check"
  gem "puppet-lint-classes_and_types_beginning_with_digits-check"
  gem "puppet-lint-unquoted_string-check"
  gem 'puppet-lint-resource_reference_syntax'
end

group :development do
  gem "travis"
  gem "travis-lint"
  gem "puppet-blacksmith"
  gem "guard-rake"
end

group :system_tests do
  gem 'pry'
  if RUBY_VERSION =~ /^2\.0\./ or RUBY_VERSION =~ /^2\.1\./
    # beaker 3 requires Ruby version >= 2.2.5
    gem 'beaker', '< 3.0'
  else
    gem 'beaker'
  end
  gem 'beaker-rspec'
  gem 'beaker-hiera'
  gem 'beaker-puppet_install_helper'
end
