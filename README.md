# Sunray Coding Standard

A coding standard to use for common PHP and JavaScript modules.

The main objectives of this standard are outlined in the 
[Sunray Coding Philosophy](/sunray/coding-standard/blob/master/coding-philosophy.md) which
aims to create an efficient development workflow resulting from readable, debuggable, and 
maintainable code. The general principles are:
* [Consistency](/sunray/coding-standard/blob/master/coding-philosophy.md#Consistency)
* [Strict and Predictable Code](/sunray/coding-standard/blob/master/coding-philosophy.md#Strict and Predictable Code)
* [Minimize Impact of Changes](/sunray/coding-standard/blob/master/coding-philosophy.md#Minimize Impact of Changes)
* [Optimize for Readability](/sunray/coding-standard/blob/master/coding-philosophy.md#Optimize for Readibility)
* [Optimize for Code Completion](/sunray/coding-standard/blob/master/coding-philosophy.md#Optimize for Code Completion)



## PHP


#### Requirements
* PHP 7.1+
* Composer

#### Installation
1. Add `"sunray/coding-standard": "dev-master"` to the `require-dev` block in your application's
   `composer.json` as follows:
    ```json
    {
        "require-dev": {
            "sunray/coding-standard": "dev-master"
        }
    }
    ```
    or automatically:
    ```bash
    composer require --dev sunray/coding-standard:dev-master
    ```
   
#### Usage
1. Create a `phpcs.xml` file in the root of your application as follows:
    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE xml>
    <ruleset name="ProjectName">
        <!-- Configure Project Paths -->

        <!-- PHPCS Settings -->
        <arg value="p" />
        <arg value="s" />
        <arg name="basepath" value="." />
        <arg name="colors" />
        <arg name="cache" />
        <arg name="extensions" value="php" />
        <arg name="encoding" value="utf-8"/>
        <arg name="report-width" value="80" />
    
        <!-- Include the Sunray coding standard -->
        <rule ref="vendor/sunray/coding-standard/ruleset.xml" />
    </ruleset>
    ```
2. From your application root execute the following:
    ```bash
    vendor/bin/phpcs
    ```

## JavaScript