---
setup: |
  import Counter from '../components/Counter.jsx';
  import ReactComponent from '../components/JSXComponent.jsx';

  const someProps = {
    count: 0,
  };
---

<Counter id="server-only" {...someProps}>
	# Hello, server!
</Counter>

<Counter id="client-idle" {...someProps} client:idle>
	# Hello, client:idle!
</Counter>

<Counter id="client-load" {...someProps} client:load>
	# Hello, client:load!
</Counter>

<Counter id="client-visible" {...someProps} client:visible>
	# Hello, client:visible!
</Counter>

<Counter id="client-media" {...someProps} client:media="(max-width: 50em)">
	# Hello, client:media!
</Counter>

<ReactComponent id="client-only" client:only="react" />