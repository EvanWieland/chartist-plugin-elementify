# chartist-plugin-elementify

This is just a simple Chartist.js Plugin that appends an element(s) to any Chartist.js chart. It's really easy to use. For example:

```
new Chartist.Line('.ct-chart', {
  labels: ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday'],
  series: [
    [12, 9, 7, 8, 5],
    [2, 1, 3.5, 7, 3],
    [1, 3, 4, 5, 6]
  ]
}, {
  fullWidth: true,
  plugins  : [
    Chartist.plugins.elementify({
      items: [{
          content: '<h3>Score: 12pts.</h3>',
          position: 'bottom',
          offsetY : 10,
          offsetX: -2
      },
      {
          content: '<h3>Lives: 3</h3>',
          position: 'bottom',
          offsetY : 15,
          offsetX: -5
      }]
    })
  ]
});
```

Most of the code used is copied from Moxx's https://github.com/moxx/chartist-plugin-fill-donut. It's basically the same functionality except it isn't restricted to only pie charts. 
