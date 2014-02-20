# fluent-plugin-tailpath, a plugin for [Fluentd](http://fluentd.org)

Fluentd plugin to tail files and add the file path to the message

Adds the following fields to log entires:
```
log_path - the full path to the source log file (eg. /var/log/nginx/access.log)
raw_message - the full un-modified log message
```

## Installation

Use RubyGems:

    gem install fluent-plugin-tailpath

## Configuration

For more info, the configuration is identical to [im_file](http://docs.fluentd.org/articles/in_tail)

Example:

     <source>
       type tailpath
       path /var/log/httpd-access.log
       pos_file /var/log/td-agent/httpd-access.log.pos
       tag apache.access
       format apache2
     </source>

## Copyright

Copyright (c) 2014 Jacob Wirth. See [LICENSE](LICENSE) for details.
