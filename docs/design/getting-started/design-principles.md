# Design Principles

The main intention is to provide a series a modules that can be embedded on every web or app plateform (website, CMS, app...).

## Keep it simple

A plateform may have various levels of complexity. Using embbeded modules let the user deal with the complexity. Our plateform only challenge is to provide an adaptable front-end interface for a shared data source of projects. As simple as it can be, using clear and effective rules is highly important to maitain usability.

## Main concepts

### Anatomy of a module

![Module Anatomy](../../assets/module-anatomy.png)

A typical module composition is based on :

- the header
- the main menu zone 
- the view menu
- the search icon
- the filter sidebar
- the status bar
- the main content
- the ranking filters

### Content 

The purpose of any module is to display content from the dataserver. One module should only take car of one type of data (projects, people, ...). Display is limited to two hierarchical levels : 

- *List Level*

![Module Anatomy - List Level](../../assets/module-anatomy-list-level.png)

The list level displays the results of a request on the dataserver where :
- any active filters has been applied 
- an optional ranking filter has been applied. The list is ordered alphabetically by default. 
- data is display accordingly to the selected view

- *Detail Level*

![Module Anatomy - Detail Level](../../assets/module-anatomy-detail-level.png)

The detail level displays the content of one entry in the results list. The detail level contains :
- a global media slider (photos, videos, ...)
- a social sharing menu
- a content section which is used to display the available content of a entry 
- a sidebar to display related info

### Views

Every list level content can be displayed from a different view. Views are text or graphic representations of the result of a request. 
Every module must implement at least a list view which display the results as rows. Switching from a view to another must not alter the filters applyed to the request (and the results).

### Navigation

Navigation is handled by 3 different menu :

- The main menu, on the left side, has to be used for top level module navigation items (CRUD operation in a detailed viex for example).
- The views menu, at the top, list all the differents views offered by the module (list, grid, map, semantic graph...)

### Searching / Filtering

At the list level, the result of the request is altered by the filters accessible for the module. A module implements at least :
- the tag/full text search filter
- the location filter

### Ranking

// To be continued....