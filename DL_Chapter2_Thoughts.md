# Deep Learning for Coder's Chapter 2 Thoughts
## Deploying a Deep Learning Model to Production
### Data Considerations
- The data that you might have trained on initially will not include things you might see in production.
- This can create issues where your model is unprepared to handle possible input it recieves in the production environment. **Out-of-domain-data**
- Another issue that you can run through when trying to deploy your model to a production environment is domain shift. If you train your model on customer data, but that customer's preferences begin to shift, your model will be operating on stale/old data. Questions like when do you refresh data and how often do you retrain the model will be important factors when trying to bring a model to productions
## Path to production for Models
- fully supervised
  - run the model alongside human supervision and figure out when it fails
- partial domain testing
  - run the model on some of your scope and analyze the data points that change
  - make sure that before you deploy your model on the constrained scope that you know what to look for
- gradual expansion of scope