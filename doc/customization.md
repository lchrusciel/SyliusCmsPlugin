# Customization

You can customize this plugin using:

- [Sylius templating overriding system](http://docs.sylius.org/en/latest/customization/template.html)
- [Symfony decorator pattern](https://symfony.com/doc/current/service_container/service_decoration.html)
- [Symfony form extension](https://symfony.com/doc/current/form/create_form_type_extension.html)

In order to check what services are available with this plugin, run the following command:

```bash
$ bin/console debug:container | grep bitbag_sylius_cms_plugin
```

**Note:**

*All forms are prefixed with 'bitbag_sylius_cms_plugin.form.*'*

If you want to check what routes are available with this plugin, use:

```bash
$ bin/console debug:router | grep bitbag_sylius_cms_plugin
```

To check parameters available with the plugin, execute:

```bash
$ bin/console debug:container --parameters | grep bitbag
```

## Testing

```bash
$ composer install
$ cd tests/Application
$ yarn install
$ yarn run gulp
$ bin/console doctrine:schema:create -e test
$ bin/console ckeditor:install
$ bin/console assets:install web -e test
$ bin/console server:run 127.0.0.1:8080 -d web -e test
$ open http://localhost:8080
$ bin/behat
$ bin/phpspec run
```
