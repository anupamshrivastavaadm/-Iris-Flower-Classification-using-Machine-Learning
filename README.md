# Iris Flower Classification using Machine Learning

Step 1 – Load the data:

Importing the libraries

![image](https://user-images.githubusercontent.com/118778677/225950602-a238e42a-e661-4517-8801-a8cc27cbb7d0.png)

First, we’ve imported some necessary packages for the project.

Numpy will be used for any computational operations. We’ll use Matplotlib and seaborn for data visualization. Pandas help to load data from various sources like local storage, database, excel file, CSV file, etc.

![image](https://user-images.githubusercontent.com/118778677/225950655-c62b058c-84de-467a-97d5-10cc68aab042.png)

Next, we load the data using pd.read_csv() and set the column name as per the iris data information. Pd.read_csv reads CSV files. CSV stands for comma separated value. df.head() only shows the first 5 rows from the data set table.

Step 2 – Analyze and visualize the dataset:

![image](https://user-images.githubusercontent.com/118778677/225950718-b7f30a81-0b30-4585-ba4f-b3eb20d8012d.png)

From this description, we can see all the descriptions about the data, like average length and width, minimum value, maximum value, the 25%, 50%, and 75% distribution value, etc.

Let’s visualize the dataset.

To visualize the whole dataset we used the seaborn pair plot method. It plots the whole dataset’s information.

![image](https://user-images.githubusercontent.com/118778677/225950834-723fa157-d810-4ac1-a69a-16e384317785.png)

From this visualization, we can tell that iris-setosa is well separated from the other two flowers. And iris virginica is the longest flower and iris setosa is the shortest.

Np.average calculates the average from an array. Here we used two for loops inside a list. This is known as list comprehension. List comprehension helps to reduce the number of lines of code. The Y_Data is a 1D array, but we have 4 features for every 3 classes. So we reshaped Y_Data to a (4, 3) shaped array. Then we change the axis of the reshaped matrix.

We used matplotlib to show the averages in a bar plot.

![image](https://user-images.githubusercontent.com/118778677/225950983-59d266d3-0998-4b23-8452-ebe236d598b9.png)

Step 3 – Model training:

![image](https://user-images.githubusercontent.com/118778677/225951175-477549df-fe75-4096-a9b7-ca4d5c601ae7.png)

Here we imported a support vector classifier from the scikit-learn support vector machine. Then, we created an object and named it svn. After that, we feed the training dataset into the algorithm by using the svn.fit() method.

Step 4 – Model Evaluation:
Now we predict the classes from the test dataset using our trained model. Then we check the accuracy score of the predicted classes. accuracy_score() takes true values and predicted values and returns the percentage of accuracy.

The accuracy is above 96%.

Now let’s see the detailed classification report based on the test dataset.

![image](https://user-images.githubusercontent.com/118778677/225951330-c1eed473-c9af-49f5-b612-a3da32192e34.png)

The classification report gives a detailed report of the prediction. Precision defines the ratio of true positives to the sum of true positive and false positives. Recall defines the ratio of true positive to the sum of true positive and false negative. F1-score is the mean of precision and recall value. Support is the number of actual occurrences of the class in the specified dataset.

Step 5 – Testing the model:
Here we take some random values based on the average plot to see if the model can predict accurately.

Prediction of Species: ['Iris-setosa' 'Iris-versicolor' 'Iris-virginica']

It looks like the model is predicting correctly because the setosa is shortest and virginica is the longest and versicolor is in between these two.

array(['Iris-setosa', 'Iris-versicolor', 'Iris-virginica'], dtype=object)
We can save the model using pickle format. And again we can load the model in any other program using pickle and use it using model.predict to predict the iris data.

In this project, we learned to train our own supervised machine learning model using Iris Flower Classification Project with Machine Learning. Through this project, we learned about machine learning, data analysis, data visualization, model creation, etc.
