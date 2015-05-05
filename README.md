# Spree PagSeguroSimple (Brazilian Payment Method)

Add support for Pagseguro checkout as a payment method.
__Only tested on Spree 3.0__

## Installation

1. Add the following to your Gemfile

    gem 'spree_pagseguro_simple'

2. Run `bundle install`

3. To copy and apply migrations run: `rails g spree_pagseguro_simple:install`

## Configuring

1. Add a new Payment Method, using: `Spree::PaymentMethod::PagSeguro` as the `Provider`

2. Click `Create`, and enter your Store's Pagseguro Email and Token in the fields provided.

3. `Save` and enjoy!

4. Is important to go to general settings in spree and configure the store url for redirects and notifications

Testing
-------

To make real tests register in PagSeguro sandbox and configure the payment method as test.

Be sure to add the rspec-rails gem to your Gemfile and then create a dummy test app for the specs to run against.

    $ bundle exec rake test app
    $ bundle exec rspec spec

Disclaimer
----------

This gem is inspired by [João Netto gem](https://github.com/jnettome/spree_pagseguro) but updated to spree 3 and using a new approach to checkout flow.

Copyright (c) 2014-2015 Locomotiva.pro, released under the New BSD License