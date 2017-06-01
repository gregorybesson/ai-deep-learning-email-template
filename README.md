# ai-deep-learning-email-template
This is my first attempt at creating an AI Coder


# The dataset
## Source
I've not found a dataset of jpg + source code of mails. SO I have to create one.
My feeling is that I'd need around 20k samples to train my AI. For now, I'll begin with a dataset of 1200 samples...

Sources:
- http://reallygoodemails.com/ (around 1000 mails)
- https://app.getresponse.com (500 templates which I could modify slightly)
- https://codepen.io/search/pens/?depth=everything&limit=all&order=popularity&page=5&q=email+template&show_forks=false (around 1000 mails)
- https://freshmail.com/newsletter-templates/ (around 130)
- mailchimp ...

## Preparation
I want my AI to code the mail based on an image. And I want to simplify as much as possible the lannguage used. 
I will remove:
- styles
- colors
- replace img src with void.png
- remove img alt content

from the templates so that I only keep the html structure of the mails.

As I don't need colors, I'll turn the images into black and white.


## The architecture
Based on that: https://github.com/tensorflow/models/tree/master/im2txt
and that: https://weiminwang.blog/2017/03/20/using-tensorflow-to-build-image-to-text-deep-learning-application/

My first attempt won't include GAN usage but if the result is promising, I'll switch to a GAN to improve its efficiency.

