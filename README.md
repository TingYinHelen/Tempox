### usage
```javascript
import Tempo from 'tempo'
import Tempox from 'tempox'

Tempo.use(Tempox)
const store = new Tempox({
  state: {
    foo: 'foo',
    bar: 'bar',
  }
  getter: {
    full: state => {
      return `${state.foo} ${state.bar}`
    }
  }
})
new Tempo({
  el: '#app',
  store,
  render(h) {
    return h(App)
  }
})
```