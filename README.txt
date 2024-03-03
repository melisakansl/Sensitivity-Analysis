Here are the questions that I solved in my code:

You are the head executive of the logistics department of a company.
You have some manufacturing plants producing your product with some capacities.
You need to send your products from plants to x many retailers which each has some demand quantity that you need to satisfy. 
You can send your product directly to retailers or send over distributors. 
Sending one product to a retailer or distributor has a cost. 
Also, you need to cover the transportation cost of distributors to retailers as well.
Your objective is to satisfy all the demand with the least cost.
All related data are provided at the end of this document.

Use Python and Pulp Package for the questions below. You are expected to upload one Notebook File(.ipynb) of your answers. 
Make sure your notebook contains all the code blocks with outputs, descriptive comments and your verbal answers to questions as markdown blocks.
Don't forget that this is an individual assignment. Each of you has unique data for the problem, use the dataset assigned to you.
If any resemblence between two submissions is caught, not only that you will not get any grades 
for your submission but legal action will be taken against both of you for plagiarism.

Question 1. Formulate this problem as an LP in Pulp. Name your decision variables and constraints clearly.
Output the model formulation (objective function and the constraints), Solve the model, 
then output the optimal solution, the basic variables and the total cost.

Question 2. Answer these questions according to the results of question 1 and seperately for each task. 
Firsly argue your expectations with reasoning using economic interpretation of the results without resolving the LP,
then reformulate a seperate model and solve it, inspect the total cost and confirm your expectations.
Do not forget to update the data for each task. Note that the naming of plants, distributors and retailers start with 0.

    Question 2.a. The capacity of plant 3 increases by one unit.
    What is the expected change in the total cost? Confirm your expectations with resolving the LP.

    Question 2.b. The capacity of plant 0 increases by one unit.
    What is the expected change in the total cost? Confirm your expectations with resolving the LP.

    Question 2.c. The demand of retailer 0 increases by one unit.
    What is the expected change in the total cost? Confirm your expectations with resolving the LP.

    Question 2.d. The cost of sending one unit from distributor 2 to retailer 2 decreases by one.
    Do you expect a change in the basis? What is the expected change in the cost? Confirm your expectations with resolving the LP.

    Question 2.e. The cost of sending one unit from distributor 2 to retailer 3 decreases by one.
    Do you expect a change in the basis? What is the expected change in the cost? Confirm your expectations with resolving the LP.

    Question 2.f. What if the decrease in Question 2.e. was 2?
    Do you expect a change in the basis? What is the change in the cost? Confirm your expectations with resolving the LP.

Question 3. Say that Plant 0 cannot ship to distributor 0 and distributor 0 cannot ship to retailer 0.
Do you think that the total cost will increase or decrease in this case? Explain.
Model the LP and Solve regarding this. Output the basic variables and the optimal cost.

Question 4. Say that the demand of retailer 0 increases.
For how much increase do you think that you will be able to satisfy the demand?
For how much increase you will lose sales?

Hints:
    - You are formulating and solving an LP. Don't formulate for the transportation simplex.
Don't use theta for the transhipment nodes and don't introduce dummy supply/demand.   
    - You will need three sets of decision variables. You can name them X_p_d, X_p_r, X_d_r.
    - Plant, distributor and retailer naming start with 0. This is consistent with Python indices.
Mind this on solving your questions.
    - You can use the makeDict() function of Pulp to prepare data for the LP Models

Data for the Student No: 2020402156
no_of_plants = 4
no_of_distributors = 3
no_of_retailers = 4
c_p_d_l = [
[15, 25, 14],
[20, 18, 11],
[14, 12, 21],
[26, 15, 28]]
c_p_r_l = [
[68, 46, 35, 58],
[57, 69, 58, 60],
[60, 69, 36, 61],
[54, 40, 49, 35]]
c_d_r_l = [
[12, 18, 17, 15],
[16, 13, 13, 10],
[15, 13, 11, 11]]
plant_capacities = [137, 266, 104, 364]
demand_quantities = [296, 211, 104, 117]
