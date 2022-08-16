<!-- ## Propagation of Uncertainties

Prof. Gerbode explains how to propagate uncertainties from a measured quantity to a calculated value:

[![Click on the link to get to the video](images/uncertainty-propagation-video-preview.png)](https://drive.google.com/file/d/1ilJNsVSgB_asmDdfjQwoyRdhedsSjaWO/view?usp=sharing) -->

-----------

## Extra practice
If we have a cone with radius $$r=2.4 \pm0.3\,\textrm{cm}$$ and a height $$h=10.2\pm0.4\,\textrm{cm}$$, what is the volume of the cone? (Hint: $$V_\mathrm{cone}=\frac{1}{3}\pi r^2 h$$)

<details>
<summary markdown='span'> (try it first, then click to expand/collapse) Solution: 
</summary>

The volume of the cone is $$ V_\mathrm{cone}=\frac{1}{3} \pi r^2 h= 61.49376 \textrm{cm}^3 $$. But what is the uncertainty?

$$ \delta V_\mathrm{cone} = \sqrt{({\delta r}\frac {\partial V_{cone}}{\partial r})^2 +({\delta h}\frac {\partial V_{cone}}{\partial h})^2 }$$

$$ = \sqrt{({\delta r} * \frac{1}{3} 2\pi r h)^2+({\delta h} * \frac{1}{3} \pi r^2)^2}$$
$$ =\sqrt{(15.37344\, \mathrm{cm}^3)^2+ (2.41152\, \mathrm{cm}^3)^2}= 15.56\, \textrm{cm}^3 $$

Therefore $$ V_\mathrm{cone}=(61 \pm 16)\,\textrm{cm}^3 $$.


Bonus: Which measurement’s uncertainty was dominant in our uncertainty in the volume of the cone, $$ r $$ or $$ h $$? 

<details>
<summary markdown='span'> (try it first, then click to expand/collapse) Solution: 
</summary>

Since the uncertainty in the volume of the cone due to the uncertainty in the radius is much larger than that from the height ( $$ 15.5\,\textrm{cm}^3 \gg 2.41\, \textrm{cm}^3 $$ ) we should refine our experimental procedure to be much more careful and precise in our radius measurement since this is limiting our knowledge of the cone’s volume.

</details>
 
 ----------

</details>
