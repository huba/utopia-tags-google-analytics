# Utopia::Tags::GoogleAnalytics

[Utopia](http://www.codeotaku.com/projects/utopia) is a website generation framework which provides a robust set of tools to build highly complex dynamic websites. It uses the filesystem heavily for content and provides frameworks for interacting with files and directories as structure representing the website.

This package includes a useful `<google-analytics>` tag for easily integrating with Google Analytics.

## Installation

Add this line to your application's Gemfile:

    gem 'utopia-tags-google-analytics'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install utopia-tags-google-analytics

## Usage

First make sure to add the `<google-analytics>` tag to `Utopia::Content` in your rackup file along with all the other tags you
wish to use:

```ruby
require 'utopia/tags/google-analytics'

...

use Utopia::Content,
	tags: {
		...
		'google-analytics' => Utopia::Tags::GoogleAnalytics,
		...
	}
```

You might want to combine this tag with the `<environment>` tag to ensure that Google Analytics is only tracked in production. Simply set the `id` attribute to whatever you have been provided by Google Analytics:

	<env only="production">
		<google-analytics id="UA-XXXXXXX-XX" />
	</env>

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## License

Released under the MIT license.

Copyright, 2012, by [Samuel G. D. Williams](http://www.codeotaku.com/samuel-williams).

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
