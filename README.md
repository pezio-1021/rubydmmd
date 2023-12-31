# rubydmmd

It is an API Client for DMM Web Service API v3.0 written in Ruby.

https://affiliate.dmm.com/api/

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'rubydmmd'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install rubydmmd

## Usage

Initialize client

```rb
api_id = 'YOUR-API-ID'
affiliate_id = 'YOUR-AFFILIATE-ID'
client = DMM.new(:api_id => api_id, :affiliate_id => affiliate_id)
```

### items(商品情報 API)

```rb
response = client.items(:site => 'DMM.com', :hits => 5, :sort => 'rank')
response.result[:items].first[:title]
# => "【受注生産】ミュージカル『刀剣乱舞』 江 おん すていじ 〜新編 里見八犬伝〜 ランダムブロマイド"
```

### floors(フロア API)

```rb
response = client.floors
```

### actress(女優検索 API)

```rb
response = client.actresses
```

### genre(ジャンル検索 API)

```rb
response = client.genres
```

### maker(メーカー検索 API)

```rb
response = client.makers(:floor_id => 92)
```

### series(シリーズ検索 API)

```rb
response = cllient.series(:floor_id => 92)
```

### authores(作者検索 API)

```rb
response = client.authores(:floor_id => 92)
```

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake spec` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/[USERNAME]/rubydmmd. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.

## License

The gem is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).

## Code of Conduct

Everyone interacting in the R::Dmm project’s codebases, issue trackers, chat rooms and mailing lists is expected to follow the [code of conduct](https://github.com/[USERNAME]/rubydmmd/blob/master/CODE_OF_CONDUCT.md).
