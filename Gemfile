source 'https://rubygems.org' 

# Fix for Ruby 4.0 compatibility with Liquid 4.0 (Jekyll 3.9)
if RUBY_VERSION >= '3.2'
  [Object, String, Array, Hash].each do |klass|
    klass.class_eval do
      def tainted?; false; end unless method_defined?(:tainted?)
      def taint; self; end unless method_defined?(:taint)
      def untaint; self; end unless method_defined?(:untaint)
    end
  end
end

gem "github-pages", group: :jekyll_plugins
gem "jekyll-theme-cayman"
gem "jekyll-remote-theme"

gem "jekyll", "~> 3.9"

gem "webrick"
gem "csv"
gem "bigdecimal"
gem "tzinfo-data", platforms: [:mingw, :mswin, :x64_mingw, :jruby]
