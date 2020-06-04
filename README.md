### Convolutional Neural Networks by deeplearning.ai in PyTorch


Course 4 of the [Deep Learning specialization](https://www.coursera.org/specializations/deep-learning) but with programming assignments done in PyTorch since the original ones are required to be done in Keras/Tensorflow (the old, bad version) and personally I prefer PyTorch way more than TF & Keras.

I might try to make these notebooks into individual programming assignments of each week for people who wish to earn credit (certificate) even after submitting code in PyTorch (this would be similar to what *u/dibgerge* did with his [Python programming assignments](https://github.com/dibgerge/ml-coursera-python-assignments) of [Ng's legendary ML Course](https://www.coursera.org/learn/machine-learning)).
The notebooks would require a `token` from Coursera to allow submission and grading locally. I'll (maybe) also restructure instructions to follow pytorch and this is still *WIP*.

#### Requirements
All packages that were in my `env` while doing this are in [requirements.txt](requirements.txt).

You just need to have `PyTorch >= 1.1` to be able to run these though.


#### Files
1. **Week 1:Foundations of Convolutional Neural Networks**
   - Learnt about convolution operation, edge-detection using filters, padding, stride, pooling (max/avg), same/valid convolutions.
   - Used the *theory* to build a convolutional model from scratch in the first programming assignment: [Convolutional Model - Building](Week%201:Foundations%20of%20Convolutional%20Neural%20Networks/Convolutional%20Model%20-%20Building.ipynb)
   - Apply the convolutional model in the second programming assignment: [Convolution Model - Application](Week%201:Foundations%20of%20Convolutional%20Neural%20Networks/Convolution%20Model%20-%20Application.ipynb): to detect handsign numbers.
2. **Week 2:Deep convolutional models - Case Studies**
   - Studied network architectures of revolutionary CV papers like LeNet, VGGNet, ResNet, AlexNet and InceptionNet
   - I personally read the respective and tried to implement them in pytorch (*eta son*)
   - **Imp. Questions for further reading/revision**: Why Residual connections work ? How Network-in-network (1x1 convolution) decreases compute cost ? How the inception module prevents overfitting by automatically having a regularizing effect ?
   - Programming exercise focused on creating ResNet50 from scratch (yes, along with keeping track of dims in each conv layer): [ResNet](Week%202:Deep%20convolutional%20models%20-%20Case%20Studies/ResNet.ipynb)
   - There was another ungraded *Keras* tutorial notebook (*smiling/!smiling*) which I don't know why I did in PyTorch (it was fun though...) --> [(Ungraded) Not Keras but pytorch practice](Week%202:Deep%20convolutional%20models%20-%20Case%20Studies/(Ungraded)%20Not%20Keras%20but%20pytorch%20practice.ipynb)
3. **Week 3: Object Detection**
   - *Cool part of computer vision* : object detection and classification, something that everyone has seen either on medium posts or on linkedin smh
   - *tough* concepts ngl, sliding windows (convolutional style), region proposals and bouding box prediction to name a few. IoU and non-max suppression were already in the pytorch package though
   - **YOLO!!!**, *epicest* paper I ever read. It was very hard to understand comprehend how exactly bounding box prediction were being leart in here. Took several forum searches to understand.
   - Programming exercise wanted us to code the various functions required for YOLO and then bring them all together.See one of the outputs that I saved [here](Week%203:%20Object%20Detection/out/test.jpg)
   - Lastly, I really wanted to actually try out the official YOLOv3 model in PyTorch [from here](https://github.com/eriklindernoren/PyTorch-YOLOv3) so I did and got some really amazing results. 
4. **Week 4:Face recognition & Neural style transfer**
    - *CNNs actually being used to do **cool** stuff here*
    - First part focused on the problem of Face Recognition/Verification (they are very different smh). Siamese networks were really interesting to learn. It is difficult to believe how they can actually do so good. *Maybe their paper explains it better hmmmm...*
    - Assignment here though: [Face Recognition - pytorch](Week%204:Face%20recognition%20&%20Neural%20style%20transfer/Face%20Recognition/Face%20Recognition%20-%20pytorch.ipynb). Weights for `inception_module_pytorch.py` in multiple `csv`s are courtesy of [*u/fukranu*](https://github.com/furkanu/) since I couldn't map the pretrained weights to my own inceptionNet implementation.
    - Second part was all about creating your own art with Neural Art Transfer. Honestly, it's very naive at its heart. It's all just taken care by the style and content cost. Hyperparameter tuning was essential to obtain good results.
    - Below is a (bad-looking) art I generated hastily.
    ![](Week%204:Face%20recognition%20&%20Neural%20style%20transfer/Neural%20Style%20Transfer/output/generated_image.jpg) 
    This is Picaso's Starry Night applied to the Louvre.
    The better one is [here](Week%204:Face%20recognition%20&%20Neural%20style%20transfer/Neural%20Style%20Transfer/output/gen_2.png)
    - Assignment here though: [Art-Generation-w-Neural-Style-Transfer](Week%204:Face%20recognition%20&%20Neural%20style%20transfer/Neural%20Style%20Transfer/Art-Generation-w-Neural-Style-Transfer.ipynb)
  
---

Thank you to the awesome people at pytorch forums and the pytorch docs. I've said it before and will say it again. PyTorch docs >>>>>>>>>> TF docs *(also Keras suck)*
