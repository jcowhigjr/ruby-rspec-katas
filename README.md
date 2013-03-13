# Ruby-RSpec for Katas

## Description

This is a scaffold for fast starting code with Ruby and RSpec

## Requirements

* [RVM](https://rvm.io/rvm/install/)
* [Ruby](http://www.ruby-lang.org/)

## Install

    git clone https://github.com/jguitar/ruby-rspec-katas.git [kata-name]
    cd [kata-name]
    bundle install

## Usage

#### Create a default lib/kata_class.rb and spec/kata_class_spec.rb

    rake

### Create specific file names and class: lib/bingo.rb and spec/bingo_spec.rb

    rake create[kata-name]

(**Brackets are mandatory**)

### Run guard

    guard

*Start to code!*

## Components

* [RSpec](https://github.com/rspec/rspec)
* [Guard-RSpec](https://github.com/guard/guard-rspec)
* [Rakefile](https://github.com/jimweirich/rake)

## Author
[Juan F. Pérez](https://github.com/jguitar)
