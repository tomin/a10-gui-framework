# Installation

### Framework Prerequisites

* **NodeJS**: **v9.3.0** or **higher**
* **NPM**: The package manager for javascript. We highly recommend that you use NPM.
* **TypeScript, ts-node, and Storybook CLI**: Please install them by `NPM`:
* **For Windows OS**: Please install windows-build-tools by `npm install --global --production windows-build-tools`.

```bash
$ npm i -g typescript ts-node @storybook/cli
```

#### Technical stacks used

* **React**: A JavaScript library for building user interfaces
* **Redux**: A predictable state container for JavaScript apps
* **RxJS**: A library for reactive functional programming using Observables, to make it easier to compose asynchronous or callback-based code
* **Webpack**: A module bundler
* **Antd**: A UI "Design Language"
* **Immutable**: Immutable collections for JavaScript
* _React-intl_: Localization solution

### Installation

```bash
$ npm i -S git+https://git.a10networks.com:8443/scm/guinext/a10-gui-framework.git
```

### Using a10-gui-framework with UGF-Generator

Code Generator `generator-ugf` is able to create a `project`, `component`, or`container` with standard folder and code structure.

#### Installation

1. Install Yeoman

```bash
npm i -g yo
```

1. Install UGF Generator

```bash
git clone https://git.a10networks.com:8443/scm/guinext/generator-ugf.git
cd generator-ugf
npm link
```

#### Generate a project

```bash
mkdir my-new-project && cd  my-new-project
# Run generator-ugf
yo ugf
```

#### Generate a component

```bash
yo ugf:component your/component/path
```

#### Generate a container

```bash
yo ugf:container your/container/path
```

### Quick start for using a10-gui-framework

```typescript
// approot/index.ts
import React from 'react'
import ReactDOM from 'react-dom'
import { A10Provider, A10Router } from 'a10-gui-framework'

import CONFIG from 'approot/configs/global'
import middlewares from 'approot/redux/middlewares'
import reducers from 'approot/redux/reducers'
import APP from 'approot/containers/App'

const initState = {}
ReactDOM.render(
  <A10Provider
    CONFIG={CONFIG}
    middlewares={middlewares}
    reducers={reducers}
    initState={initState}
  >
    <A10Router.Browser>
      <APP />
    </A10Router.Browser>
  </A10Provider>,
  document.getElementById('root'),
)
```

### 

\`\`

