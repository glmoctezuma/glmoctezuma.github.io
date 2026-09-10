source 'https://rubygems.org'

# NOTE: build this with Ruby 3.3.x.
# Every current github-pages release declares a Ruby ceiling that excludes
# Ruby 4.x, so on 4.x bundler silently backtracks to a 2019-era github-pages
# whose liquid 4.0.3 calls Object#tainted? -- removed in Ruby 3.2 -- and the
# build dies rendering the first layout.
#   brew install ruby@3.3
#   export PATH="$(brew --prefix ruby@3.3)/bin:$PATH"

# Matches what GitHub Pages runs server-side.
gem 'github-pages', group: :jekyll_plugins
gem 'jekyll-seo-tag'

# Ruby 3.0 dropped webrick from the standard library; `jekyll serve` needs it.
gem 'webrick', '~> 1.8'

# Ruby 3.4/4.0 removed these from the default gems. Jekyll 3.x and the
# ActiveSupport it depends on still require them, so they have to be
# declared explicitly or the build dies with "cannot load such file".
gem 'csv'
gem 'base64'
gem 'bigdecimal'
gem 'logger'
gem 'ostruct'
gem 'mutex_m'
gem 'drb'
gem 'benchmark'
