# Object-Detection-Marine-Animals

![Presentación1](https://github.com/JavierdiazS/Object-Detection-Marine-Animals/assets/75210642/d7983876-9b31-44f9-96c0-eab70e9ce2fb)

- [Summary](#summary)
- [Repo structure](#repo-structure)
- [Results](#results)

## Summary

Classification, Localization, and Tracking System for Three Species of Animals (Manta Ray, Shark, Sea Turtle) in the Caribbean Sea. This project holds significance in:

* Threat of Extinction: The three mentioned species face serious threats of extinction in the Caribbean Sea. Overfishing, habitat degradation, pollution, and climate change are severely impacting their populations.

* Ecological Importance: These species play critical roles in the Caribbean marine ecosystem. Sharks, for instance, are apex predators that regulate the populations of other species, while sea turtles contribute to coral reef health by maintaining balance in algae populations. The loss of these species could have a cascading impact throughout the ecosystem.

* Scientific Support: Data collection through automated detection can assist scientists in gaining a better understanding of population trends and behavioral patterns of these species in the Caribbean. Such data is essential for the development of effective conservation strategies.

This system is designed to monitor the quantity of species passing through specific strategic points and to determine the hours with the highest activity of these species.

First Test (Pre-trained MobileNet Model):

  * We have 186 images (70% Training, 30% Testing).

**(I will update the project with an effective training cycle to dynamically generate a database and train multiple models).**

## Repo structure

After obtaining the data and labeling them with their respective bounding boxes, the following are created:

The project has the following structure:
- `dataset_distribution`: `.ipynb`
    - We unzip the folder of images.
    - We split the data into training (70%) and test (30%).
    - We compress the final data.
- `json-tfrecord`: `.ipynb`
    - We unzip the `.zip` file containing the selected images.
    - We convert the train and test `.json` files to CSV.
    - We convert the CSV files for train and test to TFRecord.
- `training_models`:`.ipynb`
    - We create the LabelMap, which is a configuration file containing the classes to be trained along with their IDs.
    - We install Object Detection libraries.
    - We clone and unzip the pre-trained models, in this case, SSD + MobileNetV2.
    - We use the TFRecords for Training and Test and configure the pipeline.config file, which contains the entire training cycle needed to fine-tune the model (including image balancing and data augmentation).
    - We train the model, and finally, we evaluate and optimize it using TensorBoard.
 
 ## Results 
 
 (First Proof with SSD + MobileNetV2)

![graficas](https://github.com/JavierdiazS/Object-Detection-Marine-Animals/assets/75210642/a62cf6b2-df5f-4cac-9937-e5d7b42c8d5c)


## Contributing

Feel free to use it if you want to contribute directly to the code base.

## License

It is released under the MIT license. See the [LICENSE](/LICENSE) file for details.


