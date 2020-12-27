# PHP

## Reference

  - [PSR-1: Basic Coding Standard](https://www.php-fig.org/psr/psr-1/)

  - [PSR-12: Coding Style Guide](https://www.php-fig.org/psr/psr-12/)

  - [PSR-4: Autoloader](https://www.php-fig.org/psr/psr-4/)

## Formatter

  - VSCode

    - [phpfmt](https://marketplace.visualstudio.com/items?itemName=kokororin.vscode-phpfmt)

      ```
      {
        "[php]": {
            "editor.formatOnSave": true
        },
        "phpfmt.psr1": true,
        "phpfmt.psr1_naming": true,
        "phpfmt.psr2": true
      }
      ```

## Style Guide

  - ### Namespace

    - `UpperCase` (`CapitalCase`)

      ```
      namespace App\Http\Controllers;
      ```

  - ### Class

    - Name

      - `UpperCase` (`CapitalCase`)
        ```
        class ExampleController extends Controller
        ```

    - Constant

      - `ALL_UPPER_CASE`

        ```
        public const HOME = '/home';

        or

        public const HOME_URL = '/home';
        ```

    - Property

      - `lowerCase` (`camelCase`)

        ```
        protected $redirectTo = RouteServiceProvider::HOME;
        ```

    - Method

      - `lowerCase` (`camelCase`) 盡可能第一個字使用動詞，或是可以表達意圖

        ```
        public function index()

        or

        public function getList()
        ```

  - ### Config (Laravel)

    - `lower_case` (`snake_case`)

      ```
      // in config file

      'asset_url' => './asset',


      // retrive config value

      config('app.asset_url')

      ```
