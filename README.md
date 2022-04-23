# How-filter-and-action-hooks-work-with-example

Hoooks for wordpress:

We can create hook with simgple calling add_action() function here is example for wordpress hooks

  add_action('hook_name','function_name');

- hooks can be used for make some changes in output for update the static values / default values.
- Hooks can be start works after sucessfully perform any specific operation.
- We need to add this hook in the active theme's function.php file

Syntex:

function function_name(){
  perform opetion
}
add_action('hook_name','funciton_name');


Filter for wordpress:

We can create filter with same way like hook, we just need to replace action with filter.

  add_filter('filter_name','function_name');
  
- filter can be start working during execution time, when we want to change the any static value during execution time then we can use filters in wordpress
- we can also add the filters in function.php files

Syntex:

  add_filter('filter_name','function_name');
  funciton function_name(){
   add some code here
  }


Example: 

function cus_css_body_class( $classes ) {
    if ( ! is_admin() ) {
        $classes[] = 'wporg-is-awesome';
    }
    return $classes;
}
add_filter( 'body_class', 'cus_css_body_class' );
