source "https://rubygems.org"

# Core gems
gem "github-pages", "~> 228"
gem "jekyll-feed", "0.15.1"  # Explicitly specify the version
gem "webrick", "~> 1.8"
gem "json", "~> 2.7"

# Platform specific gems
gem "tzinfo-data", platforms: [:mingw, :mswin, :x64_mingw, :jruby]
gem "wdm", "~> 0.1.0" if Gem.win_platform?

# Jekyll plugins
group :jekyll_plugins do
  gem "jekyll-sitemap"
  gem "hawkins"
end

# Additional dependencies
gem "nokogiri"
gem "rack", "~> 2.2.4"