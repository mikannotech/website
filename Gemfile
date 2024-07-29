source "https://rubygems.org"

# GitHub Pagesを使用するため、jekyll gemはコメントアウトし、github-pages gemを使用
# gem "jekyll", "~> 4.3.3"
gem "github-pages", group: :jekyll_plugins

# Minimal Mistakesテーマを使用する場合、minimaは不要
# gem "minima", "~> 2.5"

# 必要なプラグイン
group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.12"
  gem "jekyll-include-cache"
  gem "jekyll-seo-tag"
  gem "jekyll-archives"
end

# Windows環境の場合に必要
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# Windowsでのパフォーマンス向上
# gem "wdm", "~> 0.1.1", platforms: [:mingw, :x64_mingw, :mswin]

# JRuby環境の場合に必要
gem "http_parser.rb", "~> 0.6.0", platforms: [:jruby]

# 必要なgemを追加
gem 'webrick'
gem 'csv'
gem 'faraday-retry'
