source "https://rubygems.org"

# Hello! This is where you manage which Jekyll version is used to run.
# When you want to use a different version, change it below, save the
# file and run `bundle install`. Run Jekyll with `bundle exec`, like so:
#
#     bundle exec jekyll serve
#
# This will help ensure the proper Jekyll version is running.
# Happy Jekylling!

# Frozen GitHub Pages gem stack (Jekyll 3.9.x) — too old for Ruby 4.x.
# Using modern Jekyll for local development instead.
# gem "github-pages", group: :jekyll_plugins

# Native modern Jekyll for local dev.
gem "jekyll", "~> 4.3"

# wdm 0.1.x fails to compile on Ruby 4 (implicit rb_thread_call_without_gvl);
# 0.2.0 fixes the native extension for modern Ruby.
gem "wdm", "~> 0.2.0" if Gem.win_platform?

# Add tzinfo-data for Windows time zone support
gem "tzinfo-data"  # Add this line

# If you have any plugins, put them here!
# These were previously pulled in transitively by github-pages; with native
# Jekyll they must be declared explicitly so the plugins: list in _config.yml resolves.
group :jekyll_plugins do
  # gem "jekyll-archives"
  gem "jekyll-feed"
  gem 'jekyll-sitemap'
  gem 'jekyll-paginate'
  gem 'jekyll-gist'
  gem 'jekyll-redirect-from'
  # hawkins is capped at Jekyll ~> 3.x and cannot resolve against Jekyll 4.
  # Jekyll 4 has LiveReload built in: use `bundle exec jekyll serve --livereload`.
  # gem 'hawkins'
end

gem "webrick", "~> 1.8"
