# fake-ip-filter

Exceptions for domains that are incompatible with [fake IP](https://www.rfc-editor.org/rfc/rfc3089).

## License

[CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)

## Usage

1. Add the following subscription to the mihomo configuration file.

    ```
    rule-providers:
      fake-ip-filter-set:
        type: http
        behavior: domain
        url: "https://github.com/silver716/fake-ip-filter/raw/master/fake_ip_filter_set.yaml"
        interval: 600
    ```

2. Modify the dns module configuration in the mihomo configuration file as follows.

    ```
    dns:
      fake-ip-filter:
        - rule-set:fake-ip-filter-set
      fake-ip-filter-mode: "blacklist"
    ```
