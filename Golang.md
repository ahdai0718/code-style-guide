# Golang

## Reference

  - [https://github.com/golang/go/wiki/Modules](https://github.com/golang/go/wiki/Modules)

  - [https://github.com/golang-standards/project-layout](https://github.com/golang-standards/project-layout)


## Style Guide

  - ### Architecture

    - Base on [project-layout](https://github.com/golang-standards/project-layout)

    - Directory

      - `lower_case` (`snake_case`)

        ```
        platform

        or

        third_party
        ```

    - File

      - `lower_case` (`snake_case`)

        ```
        platform.go

        or

        websocket_connection.go

        ```

  - ### Namespace alias

    - import `pkgPlayer` "module/internal/pkg/player"