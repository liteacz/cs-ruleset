# Litea codesniffer rules
PHP Code Sniffer ruleset used by our projects

##How to use

1, Install this package via composer

    composer require litea/cs-ruleset
    
2, in root folder create ruleset.xml like this

    <?xml version="1.0"?>
    <ruleset name="Litea">
        <rule ref="./vendor/litea/cs-ruleset">
            <!-- There you can put overriding codesniffer rules -->
        </rule>
    </ruleset>
    
3, if you want override default rulesets you can put to ruleset.xml for example like this:

    <?xml version="1.0"?>
    <ruleset name="Litea">
        <rule ref="./vendor/litea/cs-ruleset">
            <exclude name="SlevomatCodingStandard.Functions.StrictCall"/>
        </rule>
        <rule ref="Squiz.Strings.DoubleQuoteUsage.ContainsVar">
            <message>Variable "%s" not allowed in double quoted string; use sprintf() instead</message>
        </rule>
    </ruleset>

