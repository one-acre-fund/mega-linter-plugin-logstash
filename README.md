# mega-linter-plugin-logstash

This is a linter plugin for the excellent [MegaLinter](https://oxsecurity.github.io/megalinter), which supports checking Logstash pipeline definition files using [mustache](https://github.com/breml/logstash-config).

## Usage

To enable this plugin into your Megalinter config, add the following in your `.mega-linter.yml`:

```yaml
PLUGINS:
  - https://raw.githubusercontent.com/one-acre-fund/mega-linter-plugin-logstash/main/mega-linter-plugin-logstash/logstash.megalinter-descriptor.yml
ENABLE_LINTERS:
  - LOGSTASH_MUSTACHE
```

By default, the plugin will scan all `*.conf` file on your project, which might be broader than you'd like, so you may want to tweak the file selection options using the usual parameters, including:

- `LOGSTASH_DIRECTORY`
- `LOGSTASH_MUSTACHE_FILTER_REGEX_INCLUDE`
- `LOGSTASH_MUSTACHE_FILTER_REGEX_EXCLUDE`
- `LOGSTASH_MUSTACHE_FILE_EXTENSIONS`
- `LOGSTASH_MUSTACHE_FILE_NAMES_REGEX`
