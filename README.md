# Litea CodeSniffer rule-set

Opinionated PHP Code Sniffer rule-set used by Litea Solution.

## Usage

1. Install this package via composer

    ```shell
    $ composer require litea/cs-ruleset --dev
    ```
    
2. Create ruleset.xml in your project root


    ```xml
    <?xml version="1.0"?>
    <ruleset name="Litea">
        <rule ref="./vendor/litea/cs-ruleset">
            <!-- Here you can put overriding code sniffer rules -->
        </rule>
    </ruleset>
    ```
    
3. You can override the default rule-set using the `<rule>` tag

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