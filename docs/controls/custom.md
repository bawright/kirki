# Custom Control

Custom controls allow you to all raw HTML in a control. Mostly used for informative controls, expanatory headers etc, but you can use it for whatever you want.

```php
Kirki::add_field( '', array(
    'type'        => 'custom',
    'settings'    => 'my_setting',
    'label'       => __( 'This is the label', 'my_textdomain' ),
    'section'     => 'my_section',
    'default'     => '<div style="padding: 30px;background-color: #333; color: #fff; border-radius: 50px;">' . esc_html__( 'You can enter custom markup in this control and use it however you want', 'my_textdomain' ) . '</div>',
    'priority'    => 10,
) );
```

The content of the field is defined in the `default` argument.
You can use valid HTML.

> Please keep in mind that you should always use WordPress's i18n functions for your labels and descriptions so they are translatable. More information on WordPress's i18n functions can be found on the [WordPress Codex](https://codex.wordpress.org/I18n_for_WordPress_Developers).