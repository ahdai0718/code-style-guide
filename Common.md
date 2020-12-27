# Common

## Reference

  -

## Style Guide

  - ### As `Singular` as possible (盡可能使用單數命名)

  - ### URL Path & Parameter

    - `lower_case` (`snake_case`)

      ```
      http://localhost/users/get_list?limit=1&order_by=xxx
      ```

  - ### HTTP Header

    - `Capital-Case`

      ```
      header("X-Server-Name", "xxx");

      or

      header := http.Header{
        "X-Server-Name": []string{ServerInfo().Name},
      }
      ```