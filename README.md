# \<isw-route\>

Router with app-route like API, wrapped in an iron-selectable element that binds the active route.

```html
<app-location route="{{route}}"></app-location>

<isw-route-selector route="[[route]]" attr-for-selected="route" selected="{{selectedRoute}}" data="{{data}}">
  <isw-route import="./my-view1.html" route="my-view1" pattern="/"></isw-route>
  <isw-route import="./my-view2.html" route="my-view2" pattern="/clientes"></isw-route>
  <isw-route import="./my-view3.html" route="my-view3" pattern="/clientes/:clienteID"></isw-route>
  <isw-route import="./my-view404.html" route="notfound" pattern="/notfound"></isw-route>
</isw-route-selector>


<iron-pages attr-for-selected="route" selected="[[selectedRoute]]">
  <div route="a">Route A</div>
  <div route="b">Route B</div>
  <div route="c">Route C</div>
  <div route="d">Route D</div>
</iron-pages>
```
