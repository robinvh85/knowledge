# Reactjs

## Render process

- There are three step:
  - Triggering a render
  - Rendering the component
  - Committing to the DOM

### Step 1: Trigger a render
- There are two reasons for a component to render:
  - It’s the component’s initial render.
    - When your app starts, you need to trigger the initial render. Frameworks and sandboxes sometimes hide this code, but it’s done by calling `createRoot` with the target DOM node, and then calling its render method with your components
  - The component’s (or one of its ancestors’) state has been updated. (Called re-render)
    - Once the component has been initially rendered, you can trigger further renders by updating its state with the set function. Updating your component’s state automatically queues a render.

### Step 2: React renders your components
- After you trigger a render, React calls your components to figure out what to display on screen.
- This process is recursive: if the updated component returns some other component, React will render that component next, and if that component also returns something, it will render that component next, and so on. The process will continue until there are no more nested components and React knows exactly what should be displayed on screen.

### Step 3: React commits changes to the DOM
- After rendering (calling) your components, React will modify the DOM. 
- For the initial render, React will use the appendChild() DOM API to put all the DOM nodes it has created on screen.
- For re-renders, React will apply the minimal necessary operations (calculated while rendering!) to make the DOM match the latest rendering output.
- React only changes the DOM nodes if there’s a difference between renders

### Browser paint
- After rendering is done and React updated the DOM, the browser will repaint the screen. Although this process is known as “browser rendering”.

### Reference
- https://beta.reactjs.org/learn/render-and-commit