# Finding Similarities in Media Contents

## Motivations

The intention of this project \(repo\) is to showcase typical business use-cases, as well as practical guides in leveraging different techniques to sample media from its original form \(images, videos\) before searching/identifying similar contents.

## Background

There are several ways to detect differences / similarities of images and videos, and the answer kind of depends whom you ask: a Computer or a Human.

![](.gitbook/assets/image.png)

Typically, a computer is great at detecting every single bit of differences - literally.  As a result, comparing the binary representation of two images will merely highlight the exact 'same-ness' or not \(that there are some differences, even if it's one pixel difference between them\).  Such method is done by creating a "fingerprint" via hashing methods such as MD5 or SHA-256.

**Syntactic** matching is akin to a human finding copies of the original, or grouping several media assets together due to their similarities without extracting meaning from them.  For example, "for copy-detection use cases, ... \[one\] simply want to see if two images are essentially the same, having available neither prior information about the images, nor their context."1

The advantage \(compare to Semantic - below\) is the ability in identifying media that "share minimum adversariality"; for example, when image quality is reduced, JPEG converted to PNG format.

A Syntactic hasher popular in the community includes Perceptual Hashing \(pHash\), which what PDQ largely leveraged.  Other hashing concepts include aHash, dHash, and GIST.  These hasher simply compare similarity of images without extracting meaning from them.

**Semantic** matching is usually in form of an "algorithm in detecting features within images, e.g., determining that a given image is a picture of a tree."1  The "cost" of this approach are models training and an a-priori knowledge of the feature set to be recognized.

Semantic hasher usually comes in form of a machine-learning or deep-learning model.



## References

1. The TMK+PDQF Video Hashing Algorithm and the PDQ Image Hashing Algorithm [https://github.com/facebook/ThreatExchange/blob/master/hashing/hashing.pdf](https://github.com/facebook/ThreatExchange/blob/master/hashing/hashing.pdf)







