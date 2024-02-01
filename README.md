# Computing Cost
The term 'cost' in this assignment might be a little confusing since the data is housing cost. Here, cost is a measure how well our model is predicting the target price of the house. The term 'price' is used for housing data.

The equation for cost with one variable is:
𝐽(𝑤,𝑏)=12𝑚∑𝑖=0𝑚−1(𝑓𝑤,𝑏(𝑥(𝑖))−𝑦(𝑖))2(1)
where
𝑓𝑤,𝑏(𝑥(𝑖))=𝑤𝑥(𝑖)+𝑏(2)
𝑓𝑤,𝑏(𝑥(𝑖))
  is our prediction for example  𝑖
  using parameters  𝑤,𝑏</br>
 
(𝑓𝑤,𝑏(𝑥(𝑖))−𝑦(𝑖))2
  is the squared difference between the target value and the prediction.</br>
These differences are summed over all the  𝑚
  examples and divided by 2m to produce the cost,  𝐽(𝑤,𝑏).</br>
 








### Note, in lecture summation ranges are typically from 1 to m, while code will be from 0 to m-1.

The code below calculates cost by looping over each example. In each loop:

f_wb, a prediction is calculated
the difference between the target and the prediction is calculated and squared.
this is added to the total cost.

</br>

### Cost Function Intuition


![C1_W1_Lab02_GoalOfRegression](https://github.com/ProjectHopper/CostFunction_ML_Stanford/assets/139052598/085d827a-b873-48cb-9d47-dc8fc1256c6f)
</br>
find a model  𝑓𝑤,𝑏(𝑥)=𝑤𝑥+𝑏
 , with parameters  𝑤,𝑏
 , which will accurately predict house values given an input  𝑥
 . The cost is a measure of how accurate the model is on the training data.
</br>
The cost equation (1) above shows that if  𝑤
  and  𝑏
  can be selected such that the predictions  𝑓𝑤,𝑏(𝑥)
  match the target data  𝑦
 , the  (𝑓𝑤,𝑏(𝑥(𝑖))−𝑦(𝑖))2
  term will be zero and the cost minimized. 
  </br>
  ## Cost Function Visualization- 3D
  see how cost varies with respect to both w and b by plotting in 3D or using a contour plot.
It is worth noting that some of the plotting in this course can become quite involved. The plotting routines are provided and while it can be instructive to read through the code to become familiar with the methods, it is not needed to complete the course successfully. The routines are in lab_utils_uni.py in the local directory.

![Screenshot 2024-01-31 205752](https://github.com/ProjectHopper/CostFunction_ML_Stanford/assets/139052598/6086e785-ca78-449c-904d-375acc38c42c)
</br>
## Convex Cost surface
The fact that the cost function squares the loss ensures that the 'error surface' is convex like a soup bowl. It will always have a minimum that can be reached by following the gradient in all dimensions. In the previous plot, because the  𝑤
  and  𝑏
  dimensions scale differently, this is not easy to recognize. The following plot, where  𝑤
  and  𝑏
  are symmetric, was shown in lecture:</br>
  soup_bowl()
  
![Screenshot 2024-01-31 210013](https://github.com/ProjectHopper/CostFunction_ML_Stanford/assets/139052598/39ed2d60-832a-462e-af71-4d4b3ca6f1fc)
</br>

![Screenshot 2024-01-31 210127](https://github.com/ProjectHopper/CostFunction_ML_Stanford/assets/139052598/5945a78a-b3c1-4501-b794-a143a727d96b)
