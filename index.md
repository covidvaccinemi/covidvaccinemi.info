---
layout: page
---

<link rel="stylesheet" type="text/css" href="//cdn.datatables.net/1.10.23/css/jquery.dataTables.css">

<script type="text/javascript" charset="utf8" src="//code.jquery.com/jquery-3.5.1.js"></script>
<script type="text/javascript" charset="utf8" src="//cdn.datatables.net/1.10.23/js/jquery.dataTables.js"></script>


```
This site is under development
```

<table id="vaccine-table" class="display" style="width:100%"></table>

<script type="text/javascript" charset="utf8">
$(document).ready(function() {
    $.ajax({
        url:"https://docs.google.com/spreadsheets/d/1sb7kiNFSKm5QMq-5oysDufGwhF7FLk5OUsjwT9ycCp0/export?format=csv&gid=0",
        dataType:"text",
        success:function(raw)
        {
            let rows = raw.split(/\r?\n|\r/);
            var table = $('#vaccine-table').DataTable({
                "columns": [
                    {"title": "County"},
                    {"title": "Available"},
                    {"title": "Updated"}
                ]
            });

            for(var r=1; r<rows.length; r++) {
                data = rows[r].split(",")
                table.row.add([
                    "<a href='" + data[1] + "' target='_blank'>" + data[0] + "</a>",
                    data[2],
                    data[3]
                ]).draw();
            }
        }
    });
});
</script>
