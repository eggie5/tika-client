# Tika::Client

TODO: Write a gem description

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'tika-client'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install tika-client

## Usage

```
require 'tika-client'
require "open-uri"
require 'mini_mime'

web_path = "web.html"
ocr_path = "ocr.jpg"
file = open(ocr_path)
content_type = MiniMime.lookup_by_filename(file).content_type

client = Tika::Client.new(host: "localhost", port: 9998)
text = client.get_text(file: file, content_type: content_type)

puts text
```

## Contributing

1. Fork it ( https://github.com/[my-github-username]/tika-client/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
