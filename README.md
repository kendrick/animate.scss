# Animate.scss

This is a port of Dan Eden's [Animate.css](http://daneden.github.io/animate.css/) for SASS.

## Doesn't this already exist somewhere else?

Yes, there are plenty of other ports of this library, but many of them aren't very active projects.

Also, I was looking for something a little more flexible. By leveraging SASS mixins, this version only outputs the CSS you actually need.

## Installing
The default import includes all animations.

```
@import "animate.scss";
```

_Everything_ in this library is a mixin, so your built CSS will only include animations that are actually used. No need to comment out `@import` statements.

## Usage

Once you've imported the library, you can start include the animations directly in your CSS selectors.

```
.your-class-name {
  @include bounceIn();
}
```

The mixin includes configurable options to customize the `delay`, `count` `duration`, `function` and `fill-mode` of your animations.

```
.your-class-name {
  @include bounceIn(
    $duration: 1s,
    $count: 2,
    $delay: .2s,
    $function: ease,
    $fill: both
  );
}
```

### Keyframes

No need to include any keyframes! Each animation automatically imports its own. To avoid duplication, only the first selector of a given animation type will import keyframes for that animation.

## Licenses

Animate.css and Animate.scss are both licensed under the MIT license. (http://opensource.org/licenses/MIT)

## Contributing

Feel free to submit a pull request. I'm open to animations not included in Animate.css. If you're going to submit a pull request, please match the formatting (naming convention and file structure) and include a demo of your submission on [CodePen](http://www.codepen.io).

Thanks!
