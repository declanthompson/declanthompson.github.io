---
title: "City Park at Night"
subtitle: ""
summary: "For this image, I wanted something evocative. I'd been inspired by the numerous example images of astronauts to create an image set in space. I also wanted to see how well DALL·E could interpret clear prompts for specific items, even when the descriptions of those items is somewhat vague. What distinguishes a city park from any other? I don't know. But the resulting image better be a city park!"
authors: []
tags: []
categories: []
date: 2023-03-09T15:55:58-08:00
lastmod: 2023-03-09T15:55:58-08:00
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  filename: "citypark.png"
  caption: "A view of the moon in late afternoon from a city park, but the moon is actually the Earth, digital art"
  focal_point: "Bottom"
  preview_only: true
  placement: 1

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []

pager: true
show_breadcrumb: true
show_related: true
---

> A view of the moon in late afternoon from a city park, but the moon is actually the Earth, digital art

For this image, I wanted something evocative. I'd been inspired by the numerous example images of astronauts to create an image set in space. I also wanted to see how well DALL·E could interpret clear prompts for specific items, even when the descriptions of those items is somewhat vague. What distinguishes a city park from any other? I don't know. But the resulting image better be a city park!

## Initial results
{{< gallery album="aiart/citypark/initial" >}}
</br>

DALL·E certainly delivered a city park. Again, I'm not sure what that means, but the vibe is definitely right. A lamp post seems to be important. Possibly a fence. Definitely concrete. All the images look to be "digital art". I particularly like the "brush" strokes in the third image.


Some features of the original prompt didn't quite make it. All of these feel much more evening/night than late afternoon. While they all have a moon-like object, only the first image clearly shows this object to be Earth (for some generous sense of "clearly"). The second and third could just as well be the moon, and the object in the fourth image is *definitely* the moon.

I find it interesting that the parks are all deserted. My experience of city parks is that they're over-crowded - especially the sorts of parks depicted here, with large cities in the background. I wonder if the specification that it's "late afternoon" played a role here.

## Expanding the red bench
I was taken by the red bench in the first image DALL·E generated. The contrast in colours was striking. I wanted to see more of the bench! So I asked DALL·E to fill that in using a generation frame. I only preserved the part of the image with the bench in it.

> A red park bench in front of a lonely canal in the city at night, digital art

The "lonely canal" was meant to preserve the mood of the original and keep the consistency of the overall image: a canal explains the drop-off to the right of the bench in the original image. I also switched to "night" to stop any strange effects in the sky. Digital art aimed to keep the original style intact.

{{< gallery album="aiart/citypark/bench" >}}
</br>

The effect of "red" is immediately apparent. DALL·E seems to have been just as enthusiastic about the contrast as I was, resulting in three images with a sudden change in the brightness of the red bench. This makes for a very clear seam. Intriguingly, the seam is not where the images are actually stitched together: it runs diagonally, but the generation frame has a vertical boundary. The easiest place to see the actual seam is in the third image (the one without a bright-red portion on the bench).

I believe this phenomenon where there's something of a change in the style of the image is call "style drifting". Idea for a future image project: an image of cars drifting with the style of the image drifting across it.

The least jarring bench is the one with the same tone of red as in the original image. That bench has water behind it (the canal!) and what looks like a cemetery. I wonder if this cemetery comes from the "lonely" prompt.

## What sort of lamp is that?

I now had quite a wide image, and I wanted to make it square. But, in particular, I wanted to know what the lamp looked like. What shape might it have? Did DALL·E have good ideas?

> The moon low in a calm night sky, with a lamp post silhouetted in the foreground, digital art

It looks pretty much like the moon in the original picture, even if the colours are suggestive of Earth. I worried that specifying "the moon but it's actually the earth" would just confuse things. A *calm* night sky is intended to avoid any billowing clouds or rain. I was interested to see if we'd get any stars by just saying "calm".

{{< gallery album="aiart/citypark/lamp" >}}
</br>

Well, four different types of lamp. I guess the prompt I gave didn't offer much room for manoeuvre. Still, there's some nice variations in the sillhouetted lamp! I really like the very tall pointy one (image 2). The slightly squat third option feels like it fits the setting most though.

## The remaining corner

If you're keeping track, you'll know that I've outpainted the original image to the left and up. That leaves the top left corner unfilled. Now the goal is to fill it. At first I thought I'd try to add to the atmosphere of the image.

> A foreboding night sky above silhouetted tree-tops, digital art

Unfortunately, "foreboding" is strongly associated with bad weather, so DALL·E tried its best to include some clouds. That meant a change in the style of the sky, with a clear seam. So I tried to make sure the colouration would remain consistent:

> A dark night sky above silhouetted tree-tops, digital art

The first four images are "foreboding", the second four are "dark".

{{< gallery album="aiart/citypark/corner" >}}
</br>

They're all pretty boring, but that's what I was expecting. The biggest challenge is finding a seamless outpainting. The 6th image seems to be the best (seams to be?), so that's what I went with.

## The final image

Putting all the pieces together, we have an image of a city park at night.

{{< figure src="citypark.png" >}}
