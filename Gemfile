source "https://rubygems.org"

# Jekyll 核心 - 升级到最新版本支持 Ruby 3.4
gem "jekyll", "~> 4.3.0"

# Ruby 3.0+ 需要的标准库 gem
gem "csv"
gem "base64"
gem "bigdecimal"

# Jekyll 插件
gem "jekyll-feed", "~> 0.17"
gem "jekyll-sitemap"
gem "jekyll-seo-tag"

# Windows 平台支持
gem "wdm", ">= 0.1.0" if Gem.win_platform?

# 时区数据
gem "tzinfo-data", platforms: [:mingw, :mswin, :x64_mingw, :jruby]

# 性能优化
gem "jekyll-include-cache"

# 开发工具
group :development do
  gem "webrick", "~> 1.7"  # Ruby 3.0+ 需要
end

