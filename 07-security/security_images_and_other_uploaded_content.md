# How are my uploads secured?

> [← Help Index](../00-index.md) · Category: [Security](./index.md) · [Source ↗](https://www.amplenote.com/help/security_images_and_other_uploaded_content)

## Image & Video Content

Images and videos are protected using what is effectively a very long password. The protection mechanism combines two 122-bit values (v4 UUIDs), with one being a cryptographically secure random number, creating 2^122 possible image addresses.

The article illustrates the impracticality of brute-force attacks by noting that even if a state actor could check 1 million URLs per second, they'd need 5,531,535,562,983,420,195,188,543 years to successfully guess a single image address.

![Illustration of the vast Amplenote image and video URL address space](https://images.amplenote.com/815c831c-c9fd-11eb-893a-4e6fce92bd30/2dbc6442-af23-4578-8ad2-605511ea4ff8.png)

However, the more salient risk to this form of protection is leaking—if someone shares an image URL elsewhere, it could be discovered more easily than through brute force.

Amplenote notes they're considering encrypted images for vault notes to provide additional security layers.

## PDF Content

PDFs require account authentication. When accessed, Amplenote creates a short-term access token (works for around 15 minutes) that allows your account to access the PDF.

## Encrypted at Rest

Both file types are encrypted at rest on AWS, though the article suggests the attack vector that protects against is possibly the most unlikely one.
