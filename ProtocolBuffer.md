# Protocol Buffer

## Reference

  - [https://developers.google.com/protocol-buffers/](https://developers.google.com/protocol-buffers/)

  - [https://github.com/golang/protobuf](https://github.com/golang/protobuf)

  - [Code Style Guide](https://developers.google.com/protocol-buffers/docs/style)

## Style Guide

  - ### Enum

    - Name `CapitalCase`
    - Constant `ALL_UPPER_CASE`

      ```
      syntax = "proto3";

      package pb.game;

      option go_package = "g2gserverbase/internal/pkg/pb/game";

      enum GameType {

        GT_NONE = 0;

        GT_EXAMPLE = 1;

        GT_CHINESE_POKER_13 = 1001;

      }
      ```

  - ### Message

    - Name `CapitalCase`, attribute `lower_case` (`snake_case`)

      ```
      syntax = "proto3";

      package pb;

      option go_package = "g2gserverbase/internal/pkg/pb";

      message Player {
        string id = 1;
        int64 sn = 2;
        string name = 3;
        string display_name = 4;
        string platform = 5;
        int64 credit = 6;
        double balance = 7;
        string currency = 8;
        string id_at_platform = 9;
      }
      ```