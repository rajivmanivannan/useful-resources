# Configure the git template

* To apply the template save the ".git-commit-template.txt" file to your local machine and use

``` bash
git config --global commit.template <.git-commit-template.txt file path>
```

* If you allow empty commit messages run the below command. To prevent git from using the template as the commit message.

``` bash
git config --global commit.cleanup strip
```
