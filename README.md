# Learning and advancing with React

1. [Learning and advancing with React](#learning-and-advancing-with-react)
   1. [Guide](#guide)
      1. [Web Fundamentals](#web-fundamentals)
      2. [React Fundamentals](#react-fundamentals)
      3. [Project Setup](#project-setup)
         1. [Create React App](#create-react-app)
         2. [Babel](#babel)
         3. [Bundler](#bundler)
            1. [Webpack](#webpack)
            2. [Parcel](#parcel)
            3. [Rollup](#rollup)
      4. [Routing](#routing)
      5. [Advanced Component Patterns](#advanced-component-patterns)
         1. [Higher Order Components (HOC)](#higher-order-components-hoc)
         2. [Render Prop Components](#render-prop-components)
         3. [Hooks](#hooks)
         4. [Compound Components](#compound-components)
      6. [State Management](#state-management)
         1. [Local State](#local-state)
         2. [Sharing State](#sharing-state)
         3. [Context](#context)
         4. [Redux](#redux)
         5. [Others](#others)
         6. [Server Side State](#server-side-state)
      7. [Where to go from here](#where-to-go-from-here)
         1. [News](#news)
         2. [TypeScript](#typescript)
         3. [CSS in JS](#css-in-js)
         4. [Testing](#testing)
         5. [React based Frameworks](#react-based-frameworks)

## Guide

There are tons of tutorials out there. Some are great, some of them aren't. If you are new to [React](https://reactjs.org/) it can be a bit overwhelming where to start and what really to focus on at first. Therefore I set up this little guide.

There are also alternative guides like [Kent C. Dodds'](https://kentcdodds.com/) [How to React](https://kentcdodds.com/blog/how-to-react) and [The Complete Introduction to React](https://jscomplete.com/learn/complete-intro-react#top).

But here comes my proposal for you:

1. Before diving into React it might be helpful to check your exisiting skills regarding the [Web Fundamentals](#web-fundamentals), like HTML, CSS and JavaScript.

2. After that you should learn [React Fundamentals](#react-fundamentals), strapped of all the additional complexity, that you will encounter when setting up your own React projects.

3. Once you have a basic understanding of the API of React, you can focus on different, connected topics like [Project Setup](#project-setup), [Routing](#routing), more [Advanced Component Patterns](#advanced-component-patterns) and [State Management](#state-management).

4. The beauty (and ugly) of React is it's openess. It is not a complete framework. It does mainly one thing for you and that is build up the Browsers DOM based on the components you wrote and the data you pour into them. You will have the freedom and responsibility to choose from endless options. So I'll give you a few ideas of [Where to go from here](#where-to-go-from-here).

### Web Fundamentals

Working with Web Applications, you'll often find yourself on either [Stack Overflow](https://stackoverflow.com/) or the great [Mozilla Developer Netweork (MDN)](https://developer.mozilla.org/en-US/) to find answers. The MDN hosts a very informative documentation on [anything related to the Web](https://developer.mozilla.org/en-US/docs/Web), like the browser APIs, and it's technologies.

If you are unfamiliar with Web Fundamentals like HTML, CSS and JavaScript, you should start at [Learn web development](https://developer.mozilla.org/en-US/docs/Learn). If you have some knowledge in those technologies already, you should refresh your JavaScript knowledge with [A re-introduction to JavaScript (JS tutorial)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/A_re-introduction_to_JavaScript) and [ES6 for beginners](https://hackernoon.com/es6-for-beginners-f98120b57414).

### React Fundamentals

After being done with the [Web Fundamentals](#web-fundamentals), you can start learning React. My advise, start with the [Main Concepts](https://reactjs.org/docs/hello-world.html), following by the [Tutorial](https://reactjs.org/tutorial/tutorial.html) of the [React Website](https://reactjs.org/).

You will not have to set up a local project - My advise: Leave that for later when you feel comfortable with JavaScript and React. Use the provided CodePen links to try out what is presented to you.

### Project Setup

I am not going to dive to much into the depth of [webpack](https://webpack.js.org/), [Babel](https://babeljs.io/) and such tools. Neither am I a decorated expert with those tools, nor is there a need. There is an almost unlimited amount of resources regarding JavaScript project setups and toolchains.

I would advise you to start [here](https://reactjs.org/docs/create-a-new-react-app.html), in case you are completely new to the tools mentioned here.

Here is a little overview:

#### [Create React App](https://create-react-app.dev/docs/getting-started/)

Create React App is a comfortable environment for learning React, and is the best way to start building a new [single-page](https://reactjs.org/docs/glossary.html#single-page-application) application in React. It provides a preconfigured setup for you to get started and comes with tools such as [Babel](#babel), [webpack](#webpack) and others.

#### [Babel](https://babeljs.io/docs/en/index.html)

Babel is a toolchain that is mainly used to convert ECMAScript 2015+ code into a backwards compatible version of JavaScript in current and older browsers or environments.

#### Bundler

Because there is more than one bundler out there, I listed the three most common ones. While [webpack](#webpack) ist the most popular one and the veteran of the group, [Parcel](#parcel) and [Rollup](#rollup) are two interesting alternatives.

You'll find multiple comparisons of those tools, here is [one from 2020](https://blog.logrocket.com/benchmarking-bundlers-2020-rollup-parcel-webpack/).

The official docs of those tools will all provide a getting started with React section.

##### [Webpack](https://webpack.js.org/concepts/)

At its core, webpack is a static module bundler for modern JavaScript applications. When webpack processes your application, it internally builds a [dependency graph](https://webpack.js.org/concepts/dependency-graph/) which maps every module your project needs and generates one or more bundles.

##### [Parcel](https://parceljs.org/getting_started.html)

Is another blazing fast, zero configuration web application bundler and an alternative to [webpack](#webpack).

##### [Rollup](https://rollupjs.org/guide/en/)

Rollup is yet another module bundler for JavaScript which compiles small pieces of code into something larger and more complex, such as a library or application.

### Routing

Similar to what a router would do at the backend, deciding which content to return to the user based on the requested URL, a router in React decides which React component to render based on the URL in the browser. The difference to traditional [server-side rendered websites](https://developer.mozilla.org/en-US/docs/Learn/Server-side) is, that routing on the client side doesn't result in a reload of the browser. Which makes it potentially faster and doesn't destroy local state in the web application.

The most popular and common choice for client side routing in React is [React Router](https://reactrouter.com/web/guides/quick-start). The [official docs of React Router](https://reactrouter.com/web/guides/quick-start) are very sufficient. If you are looking for another getting started tutorial, [here](https://www.freecodecamp.org/news/a-complete-beginners-guide-to-react-router-include-router-hooks/) is a pretty nice and complete one.

### Advanced Component Patterns

Working as a software developer you'll see common, repeating issues or challenges to occur when working with any technology. [Design Patterns](https://refactoring.guru/design-patterns/what-is-pattern) are solutions to those aforementioned problems.

Because React applications are component based, a lot of common React design patterns are focused on how to write or structure your components. The following patterns are very common in the React ecosystem and should be part of your React foundation.

#### Higher Order Components (HOC)

Main usage: Composing of functionality

> A higher-order component (HOC) is an advanced technique in React for reusing component logic. HOCs are not part of the React API, per se. They are a pattern that emerges from React’s compositional nature.
>
> Concretely, a higher-order component is a function that takes a component and returns a new component.
>
> ```js
> const EnhancedComponent = higherOrderComponent(WrappedComponent);
> ```

_(Source: https://reactjs.org/docs/higher-order-components.html)_

#### Render Prop Components

Main usage: Composing of functionality

> The term “render prop” refers to a technique for sharing code between React components using a prop whose value is a > function.
>
> A component with a render prop takes a function that returns a React element and calls it instead of implementing its own render logic.
>
> ```javascript
> <DataProvider render={(data) => <h1>Hello {data.target}</h1>} />
> ```

_(Source: https://reactjs.org/docs/render-props.html)_

You can make it even more readably by using the [`children` property](https://reactjs.org/docs/introducing-jsx.html#specifying-children-with-jsx) instead of a custom one.

```javascript
<DataProvider>{(data) => <h1>Hello {data.target}</h1>}</DataProvider>
```

Render Prop Components solve similar problems as [HOCs](#higher-order-components-hoc), but are more [flexible in usage](https://gist.github.com/heygrady/f9bf3b6dd93fe3d87ba87430fd3c20d5). The downside is, that Render Prop Components, which are often non rendering components, introduce more components to the React component tree, which means more work for React.

#### Hooks

If you read the [Render Prop Components](#render-prop-components) section, you might remember that they are a powerful component pattern but tend to introduce more components to the tree than necessary. After all, we usually don't want to render anything with Render Props, we just want to distribute reusable functionality in a flexible way.

React [Hooks](https://reactjs.org/docs/hooks-intro.html) to the rescue!

Hooks are not a component pattern per se but a relatively new (since React 16.8) member of the React API. React comes with a lot of [useful standard Hooks](https://reactjs.org/docs/hooks-reference.html) but gives you the ability to [build your own](https://reactjs.org/docs/hooks-custom.html).

I'm a big fan of Hooks!

#### Compound Components

[Compound Components](https://dev.to/alexi_be3/react-component-patterns-49ho#flexible-compound-components) let you create a relation between two or more components, to have state or behavior shared.

They are very helpful for building components with a nested structure, such as lists, dropdowns, tables and many more. It lets you transform code like this

```javascript
const items = [
  { label: "Item 1", disabled: false, onClick: () => {...} },
  { label: "Item 2", disabled: true },
  ...
]

<Dropdown items={items} />
```

into code like this

```javascript
<Dropdown>
  <Dropdown.Item label="Item 1" onClick={() => {...}} />
  <Dropdown.Item label="Item 2" disabled />
</Dropdown>
```

Why is version 2 better than version 1 you ask?

When you have worked with more complex components, that include some logic to decide what happens, you usually end up creating a lot of properties to put it all together. Look at the example above, the `items` property array knows three values already: `label`, `disabled`, `onClick`. Now imagine you want to add pictures, maybe decide whether to put it left or right, change the background or font color, or present a totally different layout. You'll end up with an ugly API that creates horrible conditional code in your component and will be a nightmare to use and maintain soon after.

With Compound Components you can split up concerns (always a good idea). The wrapping component renders the wrapped components into a specific layout, maybe gives them some shared configuration or state and that's it. Each of the wrapped components takes care of their own rendering, which makes it very flexible.

### State Management

While React focuses on the rendering part of a single-page application, it still provides some useful tools to manage state. I would always advise to look for the React API first and only migrate to more complex state management solutions, when necessary.

So let's take a look at the different React APIs for managing state.

#### Local State

The simplest way to manage state, is when it lives right inside your component. I will be using [Hooks](#hooks) based examples. But you can implement all of those solutions with [React Class Components](https://reactjs.org/docs/state-and-lifecycle.html#adding-local-state-to-a-class) too.

Adding local state to a component is very easy using the [`useState` Hook](https://reactjs.org/docs/hooks-state.html).

```javascript
import React, { useState } from "react";

function Example() {
  // Declare a new state variable, which we'll call "count"
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>Click me</button>
    </div>
  );
}
```

#### Sharing State

Now we have a bunch of components with their own local state and we are happy. Nothing stand in our way. Our components are reusable, composable and can easily be shared.

Let's put them in a dashboard for example. Let's make it really user friendly. We'll have a table of statistics, render it in fancy diagram and reduce all the data points to a single benchmark value to give imediate feedback to the user of what the current status is in nifty traffic light component - awesome!

But wait. All three components table, diagram and traffic light are based on the same values. And if we want to add filtering the data for example, an action in the table component should update the other components with the filtered data, right?

Okay, so how do we share data?

Simple: We [lift up the state](https://reactjs.org/docs/lifting-state-up.html) to closest common ancestor of the three components. Now we can pass down the data to all components via the props - yeah, problem solved!

#### Context

Let's recap from [Sharing State](#sharing-state):

> ...yeah, problem solved!

So what the heck is [React Context](https://reactjs.org/docs/context.html) than?

Well, imagine you have a lot of components and a lot of state to share and you want to use [Events](https://reactjs.org/docs/handling-events.html) for inbetween component communication. It all works with lifting up the state. But you most likely will have a deeply nested component tree at some point and solving everything with lifting state and passing down props will be painful. Trust me! You'll have to pass data and callbacks from component A through B, C, D, E, F, just for it to finally arrive at component G - yuck!

So [`Context`](https://reactjs.org/docs/context.html) lets you define values and [provide](https://reactjs.org/docs/context.html#contextprovider) them down the whole component tree. Only components that are interested in the values can consume them with the [`useContext` Hook](https://reactjs.org/docs/hooks-reference.html#usecontext).

#### Redux

[Redux](https://redux.js.org/introduction/getting-started) is one of the most populare state management libraries, not just for React. In React it is based on [React Context](#context) and enables the developer to share state across components.

The most benefit from working with Redux will come from the [concepts](https://redux.js.org/introduction/core-concepts) ([Store](https://redux.js.org/understanding/thinking-in-redux/glossary#store), [Reducers](https://redux.js.org/understanding/thinking-in-redux/glossary#reducer) and [Actions](https://redux.js.org/understanding/thinking-in-redux/glossary#action)), [principles](https://redux.js.org/understanding/thinking-in-redux/three-principles) and the huge [ecosystem](https://redux.js.org/introduction/ecosystem) it provides with a wide variaty of [middlewares](https://redux.js.org/introduction/ecosystem#middleware).

There are many [tutorials and videos](https://redux.js.org/introduction/learning-resources) to help you getting started with redux.

Here is a diagram representing the flow of state in redux.

![Redux State Flow](https://i.stack.imgur.com/JYrQR.png)

#### Others

- [Recoil](https://recoiljs.org/) - A state management library for React
- [MobX](https://mobx.js.org/README.html) - Simple, scalable state management

#### Server Side State

Especially with technologies like [GraphQL](https://graphql.org/) or [PouchDB](https://pouchdb.com/), that include a practical caching solution on the client side, using server side state based solutions becomes more interesting.

### Where to go from here

So what next you're asking? Well with React it never really ends... hopefully.

#### News

There are some places, like the [official React Blog](https://reactjs.org/blog) that you should definitely take a look at once in a while.

Other good blogs I like to follow are from [Kent C. Dodds](https://kentcdodds.com/blog/) - He used to work for PayPal and releases all kinds of goodies. He is a fulltime educator now, which unfortunately resulted in the decline of his free material. Still worth it to check out - and [Mark Erikson](https://blog.isquaredsoftware.com/) - A Redux maintainer.

Besides that there is [daily.dev](https://daily.dev/) which gives you all kinds of development oriented articles. It comes with a really nice browser extension for [Chrome](https://chrome.google.com/webstore/detail/dailydev-news-for-busy-de/jlmpjdjjbgclbocgajdjefcidcncaied) and [Firefox](https://addons.mozilla.org/en-US/firefox/addon/daily/) - my secret tip!

I also started organising some interesting or constantly occurring development/IT related topics in a little [GitHub repo](https://fea17e86.github.io/dev-howtos), it also contains some [React articles](https://fea17e86.github.io/dev-howtos/?selectedTags=react).

#### TypeScript

_todo... Why, Setup, Docs/Articles/Tutorials_

#### CSS in JS

_todo... CSS Modules, Styled Components_

#### Testing

_todo... Jest, React Testing Library, Cypress.io_

#### React based Frameworks

_todo... Gatsby, Next_
