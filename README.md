# Litea codesniffer rules
PHP Code Sniffer ruleset used by our projects

## Usage

1. Install this package via composer

    ```shell
    $ composer require litea/cs-ruleset
    ```
    
2. Create ruleset.xml in your project root


    ```xml
    <?xml version="1.0"?>
    <ruleset name="Litea">
        <rule ref="./vendor/litea/cs-ruleset">
            <!-- There you can put overriding codesniffer rules -->
        </rule>
    </ruleset>
    ```
    
3. You can override the default rule-set using <rule> tag

    ```xml
    <?xml version="1.0"?>
    <ruleset name="Litea">
        <rule ref="./vendor/litea/cs-ruleset">
            <exclude name="SlevomatCodingStandard.Functions.StrictCall"/>
        </rule>
        <rule ref="Squiz.Strings.DoubleQuoteUsage.ContainsVar">
            <message>Variable "%s" not allowed in double quoted string; use sprintf() instead</message>
        </rule>
    </ruleset>
    ```