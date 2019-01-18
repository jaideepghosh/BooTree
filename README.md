# BooTree

A simple solution for displaying check-boxes in hierarchical tree structures (i.e. a Tree View) with Amazing Bootstrap.

![BooTree Screenshot](https://i.imgur.com/eHr71T2.png)

## Dependencies

For UI better experiece, Include following dependencies:

1. [jQuery v2.1.3 (>= 1.9.0)](http://jquery.com/)
2. [Bootstrap v3.3.4 (>= 3.0.0)](http://getbootstrap.com/)

## Getting Started

### Installation

Include the following files in your project.

1. bootree.min.css 
2. bootree.min.js

### Usage

Add the following resources in your html file.

```
  <!-- Required Stylesheets -->
  <link href="../dist/bootree.min.css" rel="stylesheet" type="text/css" />
  <link href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" rel="stylesheet"/>

  <!-- Required Javascript -->
  <script src="https://code.jquery.com/jquery-3.3.1.min.js"></script>
  <script src="../dist/bootree.min.js" type="text/javascript"></script>
```

The component will bind to any existing DOM element.

```
	<div id="tree"></div>
```

To initialize the BooTree and plot the check-boxes in #tree:

```
    <script type="text/javascript">
            $(document).ready(function () {
                var tree = $('#tree').tree({
                    primaryKey: 'id',
                    uiLibrary: 'bootstrap',
                    dataSource: [ { id: 1, text: 'Apple', children: [ { id: 2, text: 'Avocado' } ] } ]
                    checkboxes: true
                });
                $('#btnSave').on('click', function () {
                    var checkedIds = tree.getCheckedNodes();
                    alert(checkedIds);
                });
            });
    </script>
```

# Example
You can see BooTree [here](https://jaideepghosh.github.io/BooTree/example/index.html).
