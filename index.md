---
layout: page
---

<link rel="stylesheet" type="text/css" href="//cdn.datatables.net/1.10.23/css/jquery.dataTables.css">

<script type="text/javascript" charset="utf8" src="//code.jquery.com/jquery-3.5.1.js"></script>
<script type="text/javascript" charset="utf8" src="//cdn.datatables.net/1.10.23/js/jquery.dataTables.js"></script>

<script type="text/javascript" charset="utf8">
$(document).ready(function() {
    $('#vaccine-table').DataTable( {
        "ajax": 'data/vaccine-availability.json'
    } );
} );
</script>

```
This site is under development
```

<table id="vaccine-table" class="display" style="width:100%">
        <thead>
            <tr>
                <th>County</th>
                <th>Has capacity</th>
                <th>Updated</th>
            </tr>
        </thead>
  </table>
