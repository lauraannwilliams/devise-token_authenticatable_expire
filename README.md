# Devise::TokenAuthenticatable

[![Build Status](https://travis-ci.org/baschtl/devise-token_authenticatable.png?branch=master)](https://travis-ci.org/baschtl/devise-token_authenticatable) [![Code Climate](https://codeclimate.com/github/baschtl/devise-token_authenticatable.png)](https://codeclimate.com/github/baschtl/devise-token_authenticatable)

This gem provides the extracted Token Authenticatable module of devise. It includes the functionality that was also in [version 3.1.2](https://github.com/plataformatec/devise/tree/v3.1.2) of devise. With the inclusion of this module a user is able to sign in via an authentication token. This token can be given via a query string or HTTP Basic Authentication.

## Installation

Add this line to your application's Gemfile:

    gem 'devise-token_authenticatable'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install devise-token_authenticatable

## Usage

Add `:token_authenticatable` to your devise model:

    class User < ActiveRecord::Base
      devise :database_authenticatable, :token_authenticatable
    end

The authentication key name used by this module defaults to `auth_token`. Use the following configuration to alter the name:

    Devise::TokenAuthenticatable.setup do |config|
      config.token_authentication_key = :other_key_name
    end

## Contributing

1. Fork it.
2. Create your feature branch (`git checkout -b my-new-feature`).
3. Commit your changes (`git commit -am 'Add some feature'`).
4. Push to the branch (`git push origin my-new-feature`).
5. Create new Pull Request.
6. Get a thank you!
