# Image_encryption_algorithm

With the growing exchange of images over the internet, securing visual data has become a critical challenge. Traditional image encryption techniques rely on Pseudo Random Number Generators (PRNGs), which, while efficient, are deterministic and can be compromised if their seed entropy is low.
This project explores the use of a True Random Number Generator (TRNG) to improve the unpredictability and robustness of image encryption, making it significantly more resistant to attacks.

## 🎯 Objectives

- To enhance image encryption security using true randomness.
- To compare the performance and security of TRNG-based and PRNG-based encryption.
- To validate randomness using NIST SP 800-90B standards.
- To evaluate image encryption quality using NPCR, UACI, Entropy, and Correlation Coefficient metrics.

## 💡 Motivation

Conventional PRNGs are algorithmically generated and therefore reproducible. A TRNG, on the other hand, derives randomness from physical entropy sources (e.g., thermal noise, system jitter, or sensor noise), resulting in non-deterministic and high-entropy random numbers, ideal for cryptographic applications such as image security.

## 🔬 Methodology

- Entropy Source Collection: Capture true randomness using hardware or software-based physical noise.
- Randomness Conditioning: Apply statistical conditioning (as per NIST standards) to remove bias.
- Key Generation: Generate encryption keys using TRNG output.
- Encryption Algorithm: Apply XOR-based or diffusion–confusion encryption schemes on the image.
- Decryption: Reconstruct the image using the same TRNG-generated key sequence.
- Performance Analysis: Evaluate results using NPCR, UACI, histogram analysis, and correlation plots.

## 🧰 Tech Stack

- Languages: Python
- Libraries: NumPy, OpenCV, Matplotlib, Secrets, Random, PIL
- Standards Used: NIST SP 800-90B (Entropy validation)
- Hardware (optional): System jitter or microphone noise source for TRNG

## 🧪 Experimental Results

- High NPCR (>99%) and UACI (>33%) values prove strong diffusion.
- Low correlation between adjacent pixels confirms randomness.
- Entropy values close to 8 indicate near-perfect randomness.
