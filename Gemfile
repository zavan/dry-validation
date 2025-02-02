# frozen_string_literal: true

source "https://rubygems.org"

eval_gemfile "Gemfile.devtools"

gemspec

if ENV["DRY_CONFIGURABLE_FROM_MAIN"].eql?("true")
  gem "dry-configurable", github: "dry-rb/dry-configurable", branch: "main"
end

if ENV["DRY_SCHEMA_FROM_MAIN"].eql?("true")
  # main targets 2.0
  gem "dry-schema", github: "dry-rb/dry-schema", branch: "release-1.12"
end

if ENV["DRY_TYPES_FROM_MAIN"].eql?("true")
  gem "dry-types", github: "dry-rb/dry-types", branch: "main"
end

group :test do
  gem "dry-monads", github: "dry-rb/dry-monads", branch: "main"
  gem "i18n", require: false
end

group :tools do
  gem "pry", platform: :jruby
  gem "pry-byebug", platform: :mri
end

group :benchmarks do
  gem "actionpack"
  gem "activemodel"
  gem "activerecord"
  gem "benchmark-ips"
  gem "hotch", platform: :mri
  gem "sqlite3"
  gem "virtus"
end
