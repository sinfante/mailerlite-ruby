# MailerLite API v2 Ruby wrapper

A Ruby gem which helps to communicate with [MailerLite][mailerlite] API.

[![Gem Version](https://img.shields.io/gem/v/mailerlite.svg?style=flat-square)][rubygems]
[![Build Status](https://img.shields.io/travis/jpalumickas/mailerlite-ruby.svg?style=flat-square)][travis]
[![Dependency Status](https://img.shields.io/gemnasium/jpalumickas/mailerlite-ruby.svg?style=flat-square)][gemnasium]
[![Code Climate](https://img.shields.io/codeclimate/maintainability/jpalumickas/mailerlite-ruby.svg?style=flat-square)][codeclimate]
[![Test Coverage](https://img.shields.io/codeclimate/c/jpalumickas/mailerlite-ruby.svg?style=flat-square)][codeclimate_coverage]

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'mailerlite'
```

## Usage

Before making any request, you should authenticate first. Use the response object to
make requests afterward.
See [create a campaign][create_a_campaign] example.

### Authentication

When you sign up for an account, you are given an **API key**. You authenticate to
the [MailerLite][mailerlite] API by providing your API key in the request.
You can find your API key in page: Integrations » Developer API.

```ruby
client = MailerLite::Client.new(api_key: 'my-secret-api-key')
```

Example:

```ruby
client.campaigns
```

Or create file under `config/initializers/mailerlite.rb`

```ruby
MailerLite.configure do |config|
  config.api_key = 'my-secret-api-key'
end
```

When you configured global settings in file, then you can request methods
on `MailerLite` class directly.

Example:

```ruby
MailerLite.campaigns
```

See more documentation in [examples][examples] directory.

## Supported Ruby Versions

This library aims to support and is [tested against][travis] the following Ruby
implementations:

* Ruby 2.1.0
* Ruby 2.2.0
* Ruby 2.3.0
* Ruby 2.4.0
* Ruby 2.5.0

## Copyright
Copyright (c) 2018 Justas Palumickas. See [LICENSE][license] for details.

[rubygems]: https://rubygems.org/gems/mailerlite
[travis]: https://travis-ci.org/jpalumickas/mailerlite-ruby
[gemnasium]: https://gemnasium.com/jpalumickas/mailerlite-ruby
[codeclimate]: https://codeclimate.com/github/jpalumickas/mailerlite-ruby
[codeclimate_coverage]: https://codeclimate.com/github/jpalumickas/mailerlite-ruby/test_coverage

[license]: https://raw.githubusercontent.com/jpalumickas/mailerlite-ruby/master/LICENSE
[create_a_campaign]: https://raw.githubusercontent.com/jpalumickas/mailerlite-ruby/master/examples/create_campaign.md
[examples]: https://github.com/jpalumickas/mailerlite-ruby/tree/master/examples

[mailerlite]: https://www.mailerlite.com
