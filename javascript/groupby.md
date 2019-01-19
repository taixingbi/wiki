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

### lib 

    var result = _(data).groupBy(x => x.color)

