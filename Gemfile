# encoding: utf-8

source 'https://rubygems.org'

gemspec

group :guard do
  gem 'guard',         '~> 1.1.1'
  gem 'guard-bundler', '~> 0.1.3'
  gem 'guard-rspec',   '~> 0.7.3'
end

group :benchmarks do
  gem 'rbench', '~> 0.2.3'
end

platform :jruby do
  group :jruby do
    gem 'jruby-openssl', '~> 0.7.4'
  end
end

group :metrics do
  gem 'flay',      '~> 1.4.2'
  gem 'flog',      '~> 2.5.1'
  gem 'reek',      '~> 1.2.8', :github => 'dkubb/reek'
  gem 'roodi',     '~> 2.1.0'
  gem 'yardstick', '~> 0.7.0'
  gem 'simplecov'

  platforms :ruby_18, :ruby_19 do
    # this indirectly depends on ffi which does not build on ruby-head
    gem 'yard-spellcheck', '~> 0.1.5'
  end

  platforms :mri_18 do
    gem 'arrayfields', '~> 4.7.4'  # for metric_fu
    gem 'fattr',       '~> 2.2.0'  # for metric_fu
    gem 'heckle',      '~> 1.4.3'
    gem 'json',        '~> 1.7.3'  # for metric_fu rake task
    gem 'map',         '~> 6.0.1'  # for metric_fu
    gem 'metric_fu',   '~> 2.1.1'
    gem 'mspec',       '~> 1.5.17'
    gem 'rcov',        '~> 1.0.0'
    gem 'ruby2ruby',   '= 1.2.2'   # for heckle
  end

  platforms :rbx do
    gem 'pelusa', '~> 0.2.1'
  end
end
