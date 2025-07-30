source "https://rubygems.org"

# GitHub Pages와 Jekyll을 위한 gem들
gem "github-pages", group: :jekyll_plugins

# Jekyll 플러그인들 (_config.yml에 명시된 것들)
group :jekyll_plugins do
  gem "jemoji"
  gem "jekyll-sitemap"
  gem "jekyll-redirect-from"
  gem "jekyll-paginate"
end

# Windows와 JRuby 호환성을 위한 gem들
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1"
  gem "tzinfo-data"
end

# 성능 향상을 위한 gem들
gem "wdm", "~> 0.1.1", :platforms => [:mingw, :x64_mingw, :mswin]
gem "webrick", "~> 1.7"