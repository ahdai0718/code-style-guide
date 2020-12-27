# Typescript

## Reference

  - [Google Typescript Style](https://github.com/google/gts)

## Style Guide

  - ### Class

    - Name
      - `UpperCase` (`CapitalCase`)
        ```
        class Boot extends Phaser.Scene {
        ```

    - Constant
      - `ALL_UPPER_CASE`
        ```
        const CENTER_HORIZONTALLY: integer;
        ```

    - Property
      - `lowerCase` (`camelCase`)
        ```
        private static loaderInstance: AssetLoader;
        ```

    - Method
      - `lowerCase` (`camelCase`)
        ```
        public getBaseURL(): string {

        or

        public setBasePath(basePath: string): void {
        ```