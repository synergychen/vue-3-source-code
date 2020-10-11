# Read Vue 3 Source Code

This is the repository to document what and how I learn Vue 3 source code.

## Progress

This is a list of topics from [Vue 3](https://github.com/vuejs/vue-next/tree/master/packages) that will be covered in this repo, and more topics will be added later.

Once a topic is covered in this list, it will be checked and showed as a link.

- [ ] reactivity
  - [ ] computed
  - [ ] effect
  - [ ] reactive
  - [ ] ref
- [ ] runtime-core
  - [ ] apiCreateApp
  - [ ] h
  - [ ] renderer
  - [ ] vnode
- [ ] runtime-dom
  - [ ] vModel
  - [ ] vOn
  - [ ] vShow
  - [ ] nodeOpts
- [ ] compiler-core
- [ ] compiler-dom

## How to Read Source Code

The best way to read source code is to **run tests and debug** yourself. It only takes **3 minutes and 3 steps** to have everything setup and run.

### Step 1: Clone Vue Repo

Clone [Vue 3](https://github.com/vuejs/vue-next) source code to your local.

```
git clone https://github.com/vuejs/vue-next.git
```

### Step 2: Install Dependencies

Use `yarn` to install dependencies before you could run tests and start debugging.

```bash
#  Run yarn in vue-next repo
# `brew install yarn` if you don't have it installed or go to https://classic.yarnpkg.com/en/docs/install#mac-stable for more instructions.
yarn install
```

### Step 3: Run Test and Start Debugging

If we are interested in for example, how `reactivity` works, which is covered by `packages/reactivity/__tests__/reactive.spec.ts`, you could:

**Option 1: VSCode (Recommend)**

Add a breakpoint at the target line in VSCode and click `Debug`:

![debug](assets/images/debug.png)

This is more interactive than running from command line and could save you a lot of time.

**Option 2: Command Line**

Run:

```bash
# Use reactivity.spec.ts as an example
npm run test packages/reactivity/__tests__/reactive.spec.ts
```
