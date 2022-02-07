---
template: blog-post
title: Cascade Layers from an Amateur
slug: /cascade-layers
date: 2022-02-06 21:04
description: Cascade Layers from an Amateur
featuredImage: /assets/cascade-layers.png
---
Today’s topic is the cascade layers, this is a recent addition to CSS. As a current student learning all about web development I feel like its pretty important that I learn about the newest developments in CSS. I’m going to discuss the Cascade Layers, what they are, how to use them, and show examples. Do keep in mind that I am still learning, so if I get anything wrong feel free to go to my contact me page and send me a message.

# What are Cascade Layers?

Cascade Layers is a CSS feature led by Miriam Suzanne; with this feature you can split your CSS into several layers with the `@layer` at-rule. Within the Cascade, the position of the Layers section allows developers to have more control over the cascade. You will be able to create specificity-based layers to order your CSS, as opposed to relying on the selector specificity and the `!important` rule.

# Basic use of @layer

This [video](https://www.youtube.com/watch?v=ilrPpSQJb3U&ab_channel=UnaKravets) by Una Kravets was great for me to watch since she is able to simply and thoroughly explain how to utilize the `@layer` at-rule. While taking some inspiration from her video, I will explain how to use the `@layer` at-rule.

### take a look at this CSS and tell me which color the text is going to be.

##### HTML:

![CSS](/assets/code-1.png "CSS")

##### CSS:

![HTML](/assets/html1.png "HTML")

##### Original:

![Code output](/assets/orig-output.png "output before")

#### If you guessed pink, you would be correct!

![Image says Cascade, then below has pink letters](/assets/output.png "output after")

While the class element selector is higher specificity within selectors, a new layer’s specificity will trump it. This can be helpful to fully control the organization of your coding. Now let’s say I do want the .purple class element to be purple, there are 2 ways I could go about this. First I could move the layers around to change the layer specificity, as shown in example 1. Another way I could fix this is by setting the order of all the layers. This basically will set the layer specificity with out having move around all the `@layer` 's in your code. You would want to put your layer of least ‘priority’ first, and then all the way up to most ‘priority’ for last layer. This is shown in Example 2.

##### Example 1:

![Example code 1](/assets/example-1.png "Example code 1")

##### Example 2:

![Example code 2](/assets/example-2.png "Example code 2")

# Smaller tips

So, after explaining the basic use of `@layer`, here are some other rules of the Cascade Layers. Layers are sorted in the order that they are declared. So, if there were a total of 3 layers, the natural layer order would be chronological from the first layer documented all the way to the third one. When re-using the name of a layer, the styles will be added to the already existing layer. This allows the layer order to remain the same. This is a great tool for developers since you will be able to set the layer order upfront and add all the CSS to it later. Naming a layer is also optional, however an unnamed layer cannot be added to later in the CSS.

You can even nestle layers inside other layers, this will create somewhat of a subcategory within a layer. Now let’s say you wanted to go back and add some style to that layer within a layer, how would you do that? Well let’s say there’s a layer named layout nestled within a layer named framework. In order to add to the layer labeled layout I would need to type `@layer framework.layout {}`. The last thing I want to talk about is the use of !important and Cascade Layers. The inversion-rule is also applied to declarations in the cascade layers with `!important`.

# My Takeaway and Credits

With my small experience in coding, I can already tell that Cascade Layers are going to help me in the long run. It was a little difficult to find a lot of sources on this topic since it is so new, but I hope that I was able to explain it well to you. I want to give a big thank you to my sources for helping me put together all this information. I first found [The Future of CSS: Cascade Layers (CSS @layer)](https://www.bram.us/2021/09/15/the-future-of-css-cascade-layers-css-at-layer/#cascade-layers--create) by Bramus on his blog, it gave me a great base for all my learning. I then followed up with this video named [CSS Cascade Layers: An overview of the new @layer and layer() CSS primitives](https://www.youtube.com/watch?v=ilrPpSQJb3U&ab_channel=UnaKravets) by Una Kravets on YouTube. When I say that she caused my breakthrough with understanding the `@layer` at-rule I am not over exaggerating. The [codepen](https://codepen.io/web-dot-dev/pen/LYzqPEp) she linked was also very fun to play around with, I would recommend to try this codepen on google chrome canary. I followed up all my research with one last article from smashing magazine called [Getting Started With CSS Cascade Layers](https://www.smashingmagazine.com/2022/01/introduction-css-cascade-layers/) by Stephine Eckles, this was also a very detailed guide.