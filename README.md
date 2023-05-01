# Heroku Buildpack for `family-ties`

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) for [`family-ties`](https://github.com/abhchand/family-ties).

Runs the following:

0. `yarn install` - Install dependencies
1. `bundle exec i18n export --config ./app/frontend/locales/config.yml` - I18n translations export for frontend assets, via the `i18n-js` gem
2. `yarn run build:prod` - Asset compilation with webpack

## Usage

```bash
$ heroku config:set BUILDPACK_URL=https://github.com/abhchand/family-ties-heroku-buildpack
```
