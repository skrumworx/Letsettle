---
ID: 1173
post_title: Test
author: Admin-Skrumworx
post_excerpt: ""
layout: page
permalink: http://letsettle.net.au/test/
published: true
post_date: 2018-04-20 01:43:21
---
<style type='text/css'>
  .bold-green-font {<br />
    font-weight: bold;<br />
    color: green;<br />
  }</p>
<p>  .bold-font {<br />
    font-weight: bold;<br />
  }</p>
<p>  .right-text {<br />
    text-align: right;<br />
  }</p>
<p>  .large-font {<br />
    font-size: 15px;<br />
  }</p>
<p>  .italic-darkblue-font {<br />
    font-style: italic;<br />
    color: darkblue;<br />
  }</p>
<p>  .italic-purple-font {<br />
    font-style: italic;<br />
    color: purple;<br />
  }</p>
<p>  .underline-blue-font {<br />
    text-decoration: underline;<br />
    color: blue;<br />
  }</p>
<p>  .gold-border {<br />
    border: 3px solid gold;<br />
  }</p>
<p>  .deeppink-border {<br />
    border: 3px solid deeppink;<br />
  }</p>
<p>  .orange-background {<br />
    background-color: orange;<br />
  }</p>
<p>  .orchid-background {<br />
    background-color: orchid;<br />
  }</p>
<p>  .beige-background {<br />
    background-color: beige;<br />
  }</p>
</style>

...

function drawTable() {
var cssClassNames = {
'headerRow': 'italic-darkblue-font large-font bold-font',
'tableRow': '',
'oddTableRow': 'beige-background',
'selectedTableRow': 'orange-background large-font',
'hoverTableRow': '',
'headerCell': 'gold-border',
'tableCell': '',
'rowNumberCell': 'underline-blue-font'};

var options = {'showRowNumber': true, 'allowHtml': true, 'cssClassNames': cssClassNames};

var data = new google.visualization.DataTable();
data.addColumn('string', 'Name');
data.addColumn('number', 'Salary');
data.addColumn('boolean', 'Full Time');
data.addRows(5);
data.setCell(0, 0, 'John');
data.setCell(0, 1, 10000, '$10,000', {'className': 'bold-green-font large-font right-text'});
data.setCell(0, 2, true, {'style': 'background-color: red;'});
data.setCell(1, 0, 'Mary', null, {'className': 'bold-font'});
data.setCell(1, 1, 25000, '$25,000', {'className': 'bold-font right-text'});
data.setCell(1, 2, true, {'className': 'bold-font'});
data.setCell(2, 0, 'Steve', null, {'className': 'deeppink-border'});
data.setCell(2, 1, 8000, '$8,000', {'className': 'deeppink-border right-text'});
data.setCell(2, 2, false, null);
data.setCell(3, 0, 'Ellen', null, {'className': 'italic-purple-font large-font'});
data.setCell(3, 1, 20000, '$20,000');
data.setCell(3, 2, true);
data.setCell(4, 0, 'Mike');
data.setCell(4, 1, 12000, '$12,000');
data.setCell(4, 2, false);
var container = document.getElementById('table');
var table = new google.visualization.Table(container);
table.draw(data, options);
table.setSelection([{'row': 4}]);
}