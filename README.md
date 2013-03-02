# TcmbCurrency

Tcmb Currencies for [Money Gem](https://github.com/RubyMoney/money)

it based on [money gem](https://github.com/RubyMoney/money), [money-rails Gem](https://github.com/RubyMoney/money-rails), and adapted from [google-currency gem](https://github.com/RubyMoney/google_currency)

## Installation

Add this line to your application's Gemfile:
	
	gem 'money-rails'
    gem 'tcmb_currency'

And then execute:

    $ bundle install

Or install it yourself as:

    $ gem install tcmb_currency

## Usage
	
After the installing gems run:

	$ rails g money_rails:initializer

then add
	

	require 'money'
	require 'money/bank/tcmb_currency'
	require 'json'
	MultiJson.engine = :json_gem # or :yajl

	# set default bank to instance of GoogleCurrency
	Money.default_bank = Money::Bank::TcmbCurrency.new


And you can use it as

	Money.new(1000,"USD").exchange_to(:EUR)
	Money.new(1000,"USD").exchange_to(:EUR, "2013-03-02")


	
