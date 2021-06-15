+++
title = "Draw bounding boxes"
weight = 530
chapter = true
pre = "3. "
+++

# Draw bounding boxes

1. Click on **Start Labeling** on the top right of the dataset console.

![Start Labeling](/start-labeling.png?classes=border)

2. The console will activate _Labeling mode_. Click on **Add labels** on the left.

![Add Labels](/add-labels.png?classes=border)

3. In the pop-up that appears, choose the **Add labels** option and enter your labels one-by-one, each time pressing **Add label** to append it to the list. Once you have done putting in all your labels, click on **Save**.

![Add Label](/add-label.png?classes=border&width=30pc)

> We have 5 types of coins occuring in our images dataset, so we have added a label for each coin type above.

4. Select all images in your dataset and click on **Draw bounding box**.

![Select Images](/select-images.png?classes=border)

5. In the Rekognition labeling UI, select a label on the right and draw a box around where the corresponding object appears in the image. Do this for all objects occuring in the image.

![Labeling](/labeling.gif?classes=border)

> Boxes can be drawn in the Rekognition Custom Labels UI by clicking anywhere on the image and dragging around the mouse cursor.

6. Once all objects in the image have been labeled, click on **Next** on the top right.

![Labeled Image](/labeled-image.png?classes=border)

Repeat this procedure for all images in the dataset and click on **Done** after labeling the last image.

7. Click on **Save changes**, then hit **Exit** to deactive _Labeling mode_.

![Labeled Images](/labeled-images.png?classes=border)

---

> Your dataset is now labeled and ready to train a Machine Learning model.
