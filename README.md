# Svelte Container

This is a container component for all of your Svelte content containment needs ✨

## Width

By default, the container will be set to 100% of the width of its parent element. You can change the default value in the variable declaration <code>w</code> in the <code>script</code> tag. You can override the default for each instance of the component like this:

```svelte
<Container --w="90%">
    <p>My width is now 90%</p>
</Container>
```

## Max Width

This component has a selection of boolean props for preset <code>max-width</code>s. You should only add one of these props when using the component, otherwise the cascade will take over and probably mess up your layout.

You can also manually set the <code>max-width</code> with a css property, but note that this will be overridden if you add any of the preset sizes as props too.

Here's some examples:

```svelte
<Container md>
    <p>My max-width is 48rem.</p>
</Container>

<Container lg>
    <p>My max-width is 64rem.</p>
</Container>

<Container -maxW="70rem">
    <p>My max-width is 70rem</p>
</Container>

<Container -maxW="75rem" xl>
    <p>My max-width is 80rem, because a preset value was added.</p>
</Container>
```

## Classes

If you want to add additonal classes to your container, you can do so via the <code>klass</code> prop. The prop is named this way to avoid duplicate attributes and make everything work. Here's an example, assuming <code>.fancy</code> has been declared somewhere else:

```svelte
<Container md klass="fancy">
    <p>I'm a container and I'm fabulous ✨</p>
</Container>
```

## Spacing

This component allows you to automatically vertically space all direct children. It's inspired by the VStack from [Chakra UI](https://chakra-ui.com/), but it uses CSS Grid instead of the fancy combo selector. To use this, you need to add the <code>stack</code> prop, and pass a value for <code>--spacing</code>, like this:

```svelte
<Container lg stack --spacing="1.5rem">
    <p>There's a gap of 1.5rem below me.</p>
    <p>There's a gap of 1.5rem above and below me.</p>
    <p>There's a gap of 1.5rem above me.</p>
</Container>
```
