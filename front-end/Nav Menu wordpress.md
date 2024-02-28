To create stylish and visually appealing custom navbars in WordPress, you can either use a plugin or write custom CSS and HTML. Here are two methods to achieve this:

### Method  1: Using a Plugin

Use a plugin like CSS Hero to style your WordPress navigation menus without writing any code.

1. Install and activate the CSS Hero plugin.
2. Upon activation, click the ‘Customize with CSS Hero’ button in the WordPress admin toolbar.
3. Use the WYSIWYG editor to edit the elements you wish to change. CSS Hero will highlight the navigation menu when you hover over it, allowing you to select and edit various properties such as background, typography, borders, etc.

### Method  2: Custom CSS and HTML

If you prefer to code your navbar or need more control over its appearance, you can manually add custom CSS and HTML to your WordPress theme.

1. **Style the Navigation Menu**: Use the Inspect Element tool in your browser to identify the CSS classes associated with your navigation menu. Then, write custom CSS rules to style the menu according to your preferences.

2. **Add Custom Classes**: If you want to style specific menu items differently, you can add custom classes to them. For example, you could add `.first` and `.last` classes to the first and last items in your menu and apply custom styles to these classes.

Here's an example of how you might add these classes to your theme's `functions.php` file:

```php
function wpb_first_and_last_menu_class($items) {
    $items[1]->classes[] = 'first';
    $items[count($items)]->classes[] = 'last';
    return $items;
}
add_filter('wp_nav_menu_objects', 'wpb_first_and_last_menu_class');
```

And here's how you might style these classes in your theme's `style.css`:

```css
.first a { font-weight: bold; }
.last a { font-weight: bold; }
```

3. **Responsive Design**: Ensure your navbar is responsive by testing it on different devices and adjusting your CSS accordingly.

4. **Inspiration**: Look for inspiration from existing Bootstrap navbar examples or other websites to understand what works well in terms of design and user experience. Websites like CodePen offer many examples of navbars that you can study and incorporate into your own design [2].

Remember, consistency in design and ease of navigation are key factors in creating an effective and visually appealing navbar.