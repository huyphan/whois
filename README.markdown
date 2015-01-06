# [Whois](http://whoisrb.org/)

<tt>Whois</tt> is an intelligent — pure Ruby — WHOIS client and parser.

This library was extracted from [RoboWhois](https://www.robowhois.com/) and [RoboDomain](http://robodomain.com/). It has been performing queries in production since July 2009.

## This patch

This is a patch to the original ruby's `whois` module so that the parser doesn't always rely on the `host` part when parsing whois body. This is done by performing a multi-pattern search on a set of pre-generated signatures against given Whois body. More details are discussed [here](https://github.com/weppos/whois/pull/312).

This patch also includes some minor fixes to gracefully handle some whois properties instead of throwing out errors. 

## Features

- Ability to lookup WHOIS record for [IPv4, IPv6, TLDs, and ICANN new gTLDs](http://ruby-whois.org/manual/usage/#usage-objects)
- Ability to [parse WHOIS responses](http://ruby-whois.org/manual/parser/)
- Flexible and extensible interface (e.g. You can define [custom servers](http://ruby-whois.org/manual/server/) on the fly)
- Object oriented design, featuring 10 different design patterns
- Pure Ruby library, without any external dependency other than Ruby itself
- Successfully tested against several [Ruby implementations](http://ruby-whois.org/manual/interpreters/)

## Requirements

* Ruby >= 1.9.2

For older versions of Ruby, see the [CHANGELOG](CHANGELOG.md).


## Installation

As I don't want to put this patch to [RubyGems](https://rubygems.org/), the only way to install it is to download the project from github and build it:

    $ git clone https://github.com/huyphan/whois
    $ cd whois
    $ gem build whois.gemspec
    $ ls whois-*.gem | xargs gem install

## How to use

My patch is totally compatible with the main `Whois` module, that means your code should work just fine if you install this patch. Please refer to the original [README](https://github.com/weppos/whois/blob/master/README.md) for a quick tutorial on how to use it, or read the full [documentation](http://ruby-whois.org/documentation/).

## Credits

This patch was created and is maintained by [Huy Phan](http://zepvn.com). Commits from original project are also updated here. 
Original <tt>Whois</tt> was created and is maintained by [Simone Carletti](http://www.simonecarletti.com/). Many improvements and bugfixes were contributed by the [open source community](https://github.com/weppos/whois/graphs/contributors).

## Contributing

Direct questions and discussions to [Stack Overflow](https://stackoverflow.com/questions/tagged/whois-ruby).

[Pull requests](https://github.com/weppos/whois/pulls) are very welcome! Please include spec and/or feature coverage for every patch, and create a topic branch for every separate change you make.

Report issues or feature requests to [GitHub Issues](https://github.com/weppos/whois/issues).

## License

The original `Whois` module is Free Software distributed under the MIT license, copyright (c) 2009-2014 Simone Carletti.

This patch is also licensed under MIT license, copyright (c) 2014 Huy Phan.

## More Information
#
- [Homepage](http://whoisrb.org/)
- [RubyGems](https://rubygems.org/gems/whois)
- [Issues](https://github.com/weppos/whois)
- [Stack Overflow](https://stackoverflow.com/questions/tagged/whois-ruby)
