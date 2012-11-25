# Ruby-RSpec for Katas

## Description

This is a scaffold for fast starting code with Ruby and RSpec

## Requirements

* [RVM](https://rvm.io/rvm/install/)
* [Ruby](http://www.ruby-lang.org/)

## Install
	
    git clone https://github.com/jguitar/ruby-rspec-katas.git
    cd ruby-rspec-katas
    bundle install

## Usage

### Create a default lib/kata_class.rb and spec/kata_class_spec.rb

    rake

### Create specific file names and class: lib/bingo.rb and spec/bingo_spec.rb

    rake create[bingo]

### Run guard

    bundle exec guard
    
*Start to code!*

## Components

* [RSpec](https://github.com/rspec/rspec)
* [Guard-RSpec](https://github.com/guard/guard-rspec)
* [Rakefile](https://github.com/jimweirich/rake)

## Author
[Juan F. Pérez](https://github.com/jguitar)
