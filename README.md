# fluent-plugin-dd

Output plugin for Datadog

[![Gem Version](https://badge.fury.io/rb/fluent-plugin-dd.png)](http://badge.fury.io/rb/fluent-plugin-dd)
[![Build Status](https://drone.io/bitbucket.org/winebarrel/fluent-plugin-dd/status.png)](https://drone.io/bitbucket.org/winebarrel/fluent-plugin-dd/latest)

## Installation

    $ gem install fluent-plugin-dd

## Configuration

```
<match datadog.**>
  type dd
  dd_api_key ...
  #host my_host.example.com
  #use_fluentd_tag_for_datadog_tag false
  #emit_in_background false
</match>
```

## Usage

```sh
echo '{"metric":"some.metric.name", "value":50.0}' | fluent-cat datadog.metric
echo '{"metric":"some.metric.name", "value":100.0, "tag":"any.tag", "host":"any.host", "type":"gauge"}' | fluent-cat datadog.metric
```

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
