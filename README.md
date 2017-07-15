# ActiveModelPresenters

This gem adds `Presenter` pattern to ActiveModel/Record models. The idea is that each model in the application is enhanced with a `p` or `present(er)` method that returns a SimpleDelegator backed object which enhances the original model. TL;DR it is meant to solve simple problem, seamlessly: when you generate a new model, you get a new presenter class that by default does nothing. But when you reach a point when you start adding methods to your model, that look like 'formatted_created_at' or 'full_name' or 'to_something...' it's the moment when you should move this code to the presenter class. Wtih the help of this gem, you should get a dedicated presenter class each time you generate a new model.

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'active_model_presenters'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install active_model_presenters

## Usage

`@person.p.full_name` ot `@person.present.full_name`

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake test` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/[USERNAME]/active_model_presenters. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.

## License

The gem is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).

## Code of Conduct

Everyone interacting in the ActiveModelPresenters project’s codebases, issue trackers, chat rooms and mailing lists is expected to follow the [code of conduct](https://github.com/[USERNAME]/active_model_presenters/blob/master/CODE_OF_CONDUCT.md).
