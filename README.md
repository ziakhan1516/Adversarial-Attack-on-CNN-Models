![image](https://github.com/user-attachments/assets/29e4ea21-5185-4194-b0f7-20bf21880b0d)
Fast Gradient Sign Method (FGSM) Attack on CNNs
The Fast Gradient Sign Method (FGSM) is a popular adversarial attack technique used to fool Convolutional Neural Networks (CNNs). Introduced by Ian Goodfellow and colleagues in 2014, FGSM aims to generate adversarial examples by adding small, carefully calculated perturbations to the input data, causing the CNN to make incorrect predictions.

How FGSM Works:

FGSM operates by exploiting the gradients of the loss function with respect to the input data. The key idea is to tweak the input slightly in the direction that increases the loss, thereby maximizing the model's prediction error. The perturbation is computed as follows:

Adversarial Example
=
𝑋
+
𝜖
⋅
sign
(
∇
𝑋
𝐽
(
𝑋
,
𝑦
true
)
)
Adversarial Example=X+ϵ⋅sign(∇ 
X
​
 J(X,y 
true
​
 ))

𝑋
X: The original input image.
𝜖
ϵ: A small constant controlling the magnitude of the perturbation.
∇
𝑋
𝐽
(
𝑋
,
𝑦
true
)
∇ 
X
​
 J(X,y 
true
​
 ): The gradient of the loss function with respect to the input, indicating how to adjust the input to increase the loss.
sign
(
)
sign(): The sign function, which gives the direction of the perturbation.
Effect on CNNs:

FGSM attacks are effective because CNNs, despite their robustness to some variations in input, can be highly sensitive to small, adversarial perturbations. Even minimal changes to the input image, imperceptible to humans, can cause the CNN to misclassify the image entirely. This vulnerability exposes the need for developing more robust models and effective defenses against adversarial attacks in deep learning systems.
