# \<isw-route\>

Router with app-route like API, wrapped in an iron-selectable element that binds the active route.

```html
<app-location route="{{route}}"></app-location>

<isw-route-selector route="[[route]]" attr-for-selected="route" selected="{{selectedRoute}}" data="{{data}}">
  <isw-route route="a" pattern="/route-a"></isw-route>
  <isw-route route="b" pattern="/route-a/route-b"></isw-route>
  <isw-route route="c" pattern="/route-c/:somedata"></isw-route>
  <isw-route route="d" pattern="/route-c/route-d"></isw-route>
</isw-route-selector>


<iron-pages attr-for-selected="route" selected="[[selectedRoute]]">
  <div route="a">Route A</div>
  <div route="b">Route B</div>
  <div route="c">Route C</div>
  <div route="d">Route D</div>
</iron-pages>
```

With the isw-route you are also able to lazy-import, making the import of the files comment when necessary

```html
<link rel="lazy-import" href="my-view1.html">
<link rel="lazy-import" href="my-view2.html">
<link rel="lazy-import" href="my-view3.html">
<link rel="lazy-import" href="my-view404.html">

...

<app-location route="{{route}}"></app-location>

<!-- To import the component you need to enter the full path of the component from the project root folder -->

<isw-route-selector route="[[route]]" attr-for-selected="route" selected="{{selectedRoute}}" data="{{data}}">
  <isw-route import="./src/my-view1.html" route="a" pattern="/route-a"></isw-route>
  <isw-route import="./src/my-view2.html" route="b" pattern="/route-a/route-b"></isw-route>
  <isw-route import="./src/my-view3.html" route="c" pattern="/route-c/:somedata"></isw-route>
  <isw-route import="./src//my-view404.html" route="d" pattern="/route-c/route-d"></isw-route>
</isw-route-selector>


<iron-pages attr-for-selected="route" selected="[[selectedRoute]]">
  <div route="a">Route A</div>
  <div route="b">Route B</div>
  <div route="c">Route C</div>
  <div route="d">Route D</div>
</iron-pages>
