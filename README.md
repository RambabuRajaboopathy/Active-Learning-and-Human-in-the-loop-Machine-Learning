# Active-Learning-and-Human-in-the-loop-Machine-Learning
The Project show cases the Active Learning for deep learning and Human in the Loop Machine Learning. This work was carried out Fraunhofer Institute for Integrated Circuits IIS, Division Engineering of Adaptive Systems EAS located in Dresden


# Use case:
The uncertainty in deep learning models is divided into aleotric and epsitemic uncertainities, the uncertainty metric is not taken into account and it is hard to interpret the models prediction. The main goal of the Active Learning algorithm is to iteratively seek the most informative samples points and add it to the training dataset. 
Steps in Active Learning is described in the follwing figure 
![Active Learning](https://user-images.githubusercontent.com/74974473/216408405-cf2b545b-9542-4334-8fd6-bb640905da17.PNG)


## Confidentiality Agreement
Owing to the confidentiality agreement and NDA the necessary scripts and resuts are not enclosed in the repository. But to summarise the overall work a Mermaid diagrams is desribed below.

<div class="center">

```mermaid
graph TD


  subgraph "Trained Deep Learning model"
    A["Add uncertainty objects to validate model evaluation"]--> |create_uncertain_Labels_for_LabelStudio.py| B[The pre annotated regions ate imported to Label Studio]
    B-->|import_uncertain_labeles_to_LabelStudio.py|C[Perform Manual annotation in Label Studio to correct the uncertain objects]
    C-->D[Add the new annotated K points to the existing dataset]
    D-->|Transfer_Learning_Model.py|E[Retrain Deep Learning model on specified class labels]

    
end
```

</div>

