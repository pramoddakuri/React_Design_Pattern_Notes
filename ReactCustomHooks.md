<h2>React Custom Hooks</h2>

<h4>What will learn</h4>
<ol>
  <li>Why Hooks</li>
  <li>What is a Hook in React</li>
  <li>Built in Hooks Overview</li>
  <li>Rules of Hook</li>
  <li>Custom Hokoks Pattern</li>
  <li>Real-world Examples</li>
  <li>Use cases and ideas</li>
  <li>Pitfalls</li>
</ol>

<h3>Why Hooks</h3>

<p>React Hooks were introduced in React 16.8 (February 2019). Before that, React did not have Hooks. The primary way to share reusable logic across components was through Higher-Order Components (HOCs), Render Props, and earlier, Mixins (in createClass, later deprecated).</p>
<h5>What existed before Hooks?</h5>
<p>1) Class components + lifecycle methods
Reusable logic was often implemented inside class components using lifecycle methods (componentDidMount, componentDidUpdate, componentWillUnmount) and then abstracted via patterns like HOCs or Render Props.</p>

```jsx

class UserList extends React.Component {
  state = { users: [] };

  componentDidMount() {
    fetch("/api/users").then(res => res.json()).then(users => this.setState({ users }));
  }

  render() {
    return <List data={this.state.users} />;
  }
}
```

<p>2) Higher-Order Components (HOCs)
A HOC is a function that takes a component and returns a new component, injecting props or behavior.</p>
