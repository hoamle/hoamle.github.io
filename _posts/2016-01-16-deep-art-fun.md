---
layout: post
title: "Deep Art fun"
date: 2016-01-16
tag: [arts, AI, general-audience,]
---
Last weekend I finally had the time to take some of personal photos and *\"paint\"* them in Van Gogh and other artist styles. The \"painting\" part was actually done automatically by [**DeepArt algorithm**](#deepart){% sidenote "sn-id-artomatix" "It's worth to note that [Artomatix](//artomatix.com/) - an Irish startup - had introduced a [similar work](//youtu.be/un9lSayNOIY?t=51) under the name \"Texture Painting\" several months before DeepArt algorithm was published." %} - an inspiring application from Deep learning research. In short, the algorithm takes your source photo - hereby referred as ***content-image*** - and a reference style - called ***style-image*** - as the inputs and produces your source photo in that style. 

## Demo
I used [jcjohnson's implementation](//github.com/jcjohnson/neural-style) of DeepArt algorithm for this demo. 

Here we have the content-image on the top-left, the style-image is an artwork by artist Leonid Afremov on the top-right, and the photo generated in Afremov\'s style at the bottom.

{% assign img_root =  "//raw.githubusercontent.com/hoamle/neural-style-example/master" %}


<div class="img_row" style="width: unset; height: 200px; padding: unset; margin: unset">
    <img class="col" style="width: 50%" src="{{ img_root }}/content-imgs/exeter.jpg"/>
    <img class="col" style="width: 50%" src="{{ img_root }}/style-imgs/Afremov2.jpg"/>
    
</div>
<img src="{{ img_root }}/visually-appealing/exeter-afremov2.png">

The machine did not "paint" the picture out of the blue, it\'s an iterative process. In short, it starts with a blank (noisy) canvas and tries to learn prominent features in both content-image and style-image(s) and present them on the final product. That learning process is mathematically expressed as optimization process of a function representing the combined *similarity* between the output and the inputs. Optimizing such function requires an algorithm which goes through series of iterative update, visualized as followed.

<img src="{{ img_root }}/exeter_afremov2.gif">

## More images
{% marginnote 'mn-hardware' '*Technical bit:* Images were produced by NIN model + Adam optimization. If hardware constrainst is not a problem, visual results should be *considerably **improved***  by using VGG-19 model + L-BFGS optimization.' %}
**Note:** Due to hardware constrainst, most of images below were generated from *poor-man* configs, thus did not yield the best possible quality. I will be sporadically updating results in near future.

**Style image**: by [@creativemints](//www.behance.net/gallery/13033419/Selected-Artworks-2013-Oil-Acrylic-Watercolor)

<div class="img_row" style="width: unset; height: 200px; padding: unset; margin: unset">
    <img class="col" style="width: 50%" src="{{ img_root }}/content-imgs/potr.jpg"/>
    <img class="col" style="width: 50%" src="{{ img_root }}/style-imgs/lostquilt_at_pinterest.jpg"/>
    
</div>
<img src="{{ site.github.url }}/assets/img/lostquilt.png"> 

**Style image**: by Leonid Afremov
<div class="img_row" style="width: unset; height: 200px; padding: unset; margin: unset">
    <img class="col" style="width: 50%" src="{{ img_root }}/content-imgs/pedals.jpg"/>
    <img class="col" style="width: 50%" src="{{ img_root }}/style-imgs/Afremov4.jpg"/>
    
</div>
<img src="{{ img_root }}/visually-appealing/pedals-afremov4.png">

**Style image**: Van Gogh\'s Starry Night 
<div class="img_row" style="width: unset; height: 200px; padding: unset; margin: unset">
    <img class="col" style="width: 50%" src="{{ img_root }}/content-imgs/exe_quay.jpg"/>
    <img class="col" style="width: 50%" src="{{ img_root }}/style-imgs/starry_night.jpg"/>
    
</div>
<img src="{{ img_root }}/visually-appealing/exe_quay-starrynight.png">

**Style image**: Van Gogh\'s Wheat Field with Crows
<div class="img_row" style="width: unset; height: 200px; padding: unset; margin: unset">
    <img class="col" style="width: 50%" src="{{ img_root }}/content-imgs/camb.jpg"/>
    <img class="col" style="width: 50%" src="{{ img_root }}/style-imgs/vangogh_Wheat_Field_with_Crows.jpg"/>
    
</div>
<img src="{{ img_root }}/visually-appealing/camb-vangogh_wheatfield.png">

## Observation
**Size matters**. The higher the output image resolution, the more details in the content-image can be explicitly expressed by the indicated style. However, memory is a *big* trade-off. Default output image size (max. 512px-wide) on an NIN took as small as 5-600MB, but a 784px image devours 3 times as much! 

**For visual appeal**, an **expressive** style and/or **resemblance** between content-style image pair is the key:
   * *\"Expressive\"* in this context is about texture i.e. discernible patterns in colors, strokes, blobs. Example work: Leonid Afremov\'s painting, The Scream, Monet\'s water lilies,... Experimentation with realism pieces by the old masters, e.g. Jean Leon Gerome, as style-images usually yields unsatisfiying results. 
   * Although not always, content- and style-images of similar semantics pair well with each other. For example, a landscape picture should play along well with Starry Night or Wheat Field and the Crows; a portrait and one of Picasso\'s self-portraits also make a nice combination. 

Last but not least, me drooling over a Titan X with gigantic memory

## Hardware setup
The main work-horse is a humble 2GB nVidia GTX 660 GPU{% sidenote 'sn-gpu' 'i.e. common video graphic card for gaming' %} plugged in a dated LGA 775 desktop. <del>Each image was generated in ~90 seconds (for a 512px-image) or 2-3 mins (for a 784px-image)</del>{% sidenote "sn-id-advances" "*Learning-based approaches* e.g. [fast-neural-style](//github.com/jcjohnson/fast-neural-style) have largely reduce generation time down to just *a few seconds*" %}. GPU(s) with generous memory is desirable.

It\'s *much* faster to run DeepArt algorithm on GPU(s) instead of common CPUs. Even a modern i7 K-series can take upto hour to train and generate 1 image of above sizes. However, running on CPU can take advantages of *abundant* host memory (easily >8GB on a single machine), not to mention the possibility to be accompanied with a coprocessor (eg: Xeon Phi), or running on distributed platform.

## <a name="refs">References</a>
1. <a name="deepart">[A Neural Algorithm of Artistic Style](//arxiv.org/abs/1508.06576) (Gatys et al, 2015) i.e. DeepArt algorithm. The name "DeepArt" is adopted from the authors' commercial website [deepart.io](//deepart.io/)
</a>
