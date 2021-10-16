### Dangerous functions for different languages

Java: https://stackoverflow.com/a/4351516  
.NET: https://stackoverflow.com/a/20903746  
PHP: https://stackoverflow.com/a/3115645  
Ruby: https://cheatsheetseries.owasp.org/cheatsheets/Ruby_on_Rails_Cheat_Sheet.html  

Then just manually search them in a source code and examine

## Good static analysis tools:
Python: bandit  
Ruby: brakeman

## Not good but can help somehow
c#: sonarqube/PVS-Studio/Re-Sharper

## Ruby
#### search for vulnerable gems  
`$ gem install bundle-audit`  
`$ cd my/cool/ruby/project/folder/with/Gemfile.lock/`  
`$ bundle-audit check --update`  

#### static vuln analysis  
`$ gem install rubocop`  
`$ cd my/cool/ruby/project`  
`$ rubocop`  

#### also searches for vulns
`$ gem install brakeman`   
`$ brakeman my/cool/ruby-on-rails/project --run-all-checks --branch-limit -1 --parser-timeout 120 -o ./brakeman-report.txt`  

#### `mysql_real_escape_string` edge cases/bypasses
* https://www.sqlinjection.net/advanced/php/mysql-real-escape-string/
* https://shiflett.org/blog/2006/addslashes-versus-mysql-real-escape-string
