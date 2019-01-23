### groupby
---
### js

    Array.prototype.groupBy = function(prop) {
      return this.reduce(function(groups, item) {
        const val = item[prop]
        groups[val] = groups[val] || []
        groups[val].push(item)
        return groups
      }, {})
    }  
    
    var groupBy = function(xs, key) {
      return xs.reduce(function(groups, item) {
        (groups[ item[key] ] = groups[ item[key] ] || []).push(item);
        return groups;
      }, {});
    };

    console.log(groupBy(['one', 'two', 'three'], 'length'));

    // => {3: ["one", "two"], 5: ["three"]}

