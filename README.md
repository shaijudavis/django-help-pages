#Simple, pluggable help-section/FAQs app.

Still *very* much in progress.

##Requirements

 * Django 1.1+
 * django-tagging

## Product backlog 

 * DONE extensible heirarchy of HelpCategories
 * DONE 1..n HelpItems in each endpoint category
 * DONE ordering, within categories and overall

 * DONE tagging for categories

 * use tagging to suggest related topics
 * get_related_items() method, returning other items in cateory and/or items with shared tags

 * Unit tests for:
  * subcategory joining; recursion limits
  * ordering
  * searching
  * tagging
  (This is what I get for breaking my TDD approach...)

 * Views 
  * DONE slug-based/SEO friendly help topics
  * DONE category breakdown
  * DONE per-category listings of all items in category
  * DONE single item access, with link back to category
  * DONE tag-related items

 * Search
  * DONE sensible, scalable but database independent search
  * DONE inclusion tag for searching help

  * Ability for any user to rate usefulness (boolean) of help items 
    + use cookies to remember whether the user has rated this before
    + possibly track which authenticated users have marked this as useful

 * Cacheing
  * add cache support
  * cache-buster, too, for when users rate something as being useful

 * Templates
  * DONE simple out-of-the-box views and templates extending base.html
  * AJAX-driven option too

 * Admin
  * Better, less verbose list view pages
  * DONE fix the order of fields to be more sane
