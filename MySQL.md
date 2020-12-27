# MySQL

## Reference

## Style Guide

  - ### Keywords and Reserved Words

      - `UPPERCASE`

        ```
        SELECT *
        FROM `table_name`
        WHERE 1 AND `column_name` = 'xxx'
        ORDER BY `column_name`
        LIMIT 1;
        ```

  - ### Schema

    - `lower_case` (`snake_case`)

      ```
      CREATE SCHEMA `for_example` DEFAULT CHARACTER SET utf8;
      ```

  - ### Table

    - `lower_case` (`snake_case`)

      ```
      CREATE TABLE `platform_provider` (
      ```

  - ### Column

      - `lower_case` (`snake_case`)

        ```
        CREATE TABLE `platform_provider` (
          `name` varchar(32) NOT NULL,
          `factory_name` varchar(32) NOT NULL DEFAULT 'default',
          `aes_key` varchar(64) NOT NULL,
          `aes_iv` varchar(64) NOT NULL,
          `auth_type` int(11) NOT NULL DEFAULT '1' COMMENT '1: JWT 2: OAuth',
          `auth_id` varchar(64) NOT NULL,
          `auth_secret` varchar(64) NOT NULL,
          `auth_grant_type` varchar(256) NOT NULL DEFAULT 'client_credentials',
          `auth_scope` varchar(256) NOT NULL DEFAULT 'bets',
          `api_url_base` varchar(256) NOT NULL,
          PRIMARY KEY (`name`)
        ) ENGINE=InnoDB DEFAULT CHARSET=utf8;
        ```

  - ### Statement

    - Use `` ` ` `` for all `` `Schema` ``, `` `Table` ``, `` `Column` ``

      ```
      SELECT * FROM `table_name` WHERE 1 AND `column_name` = 'xxx' ORDER BY `column_name` LIMIT 1;

      SELECT `table_a`.`column_a`, `table_b`.`column_b`
      FROM `table_a` LEFT JOIN `table_b` ON ` `table_a`.`column_c` = `table_b`.`column_c`
      WHRER 1 AND `table_a`.`column_d` = 'xxx'
      ORDER BY `table_b`.`column_e`
      LIMIT 1;
      ```

    - Use `;` for end

  - ### Stored Procedures

    - `[TableName]_SP_[ActionDescription]` (`CapitialCase_SP_CapitcalCase`)

      ```
      CREATE DEFINER=CURRENT_USER PROCEDURE `PlatformProvider_SP_GetAll`()
          SQL SECURITY INVOKER
      BEGIN
        SELECT * FROM `platform_provider`;
      END
      ```