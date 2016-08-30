# WP Term Order

Sort taxonomy terms, your way.

WP Term Order allows users to order any visible category, tag, or taxonomy term numerically, providing a customized order for their taxonomy terms.

# Installation

* Download and install using the built in WordPress plugin installer.
* Activate in the "Plugins" area of your admin by clicking the "Activate" link.
* No further setup or configuration is necessary.

# Demo

![Term Reorder](screenshot-1.gif)

# FAQ

### Does this create new database tables?

No. There are no new database tables with this plugin.

### Does this modify existing database tables?

No! This fork uses Term Meta to save the term order.

### Can I query and sort by `order`?

Yes. Use it like:

```
$terms = get_terms( array(
    'taxonomy'   => 'category',
	'depth'      => 1,
	'number'     => 100,
	'parent'     => 0,
	'orderby'    => 'order', // <--- Looky looky!
	'order'      => 'ASC',
	'hide_empty' => false,
) );
```
