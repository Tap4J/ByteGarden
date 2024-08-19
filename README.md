# ByteGarden
Assignment for ByteGarden

## Guidelines
**Install Libraries from Requirements Using pip**
1. Open your terminal (macOS/Linux) or command prompt (Windows).
2. Navigate to the directory where you have downloaded/cloned the repository.
    ```sh
    cd path/to/your/project
    ```
3. (Optional) Create and activate a virtual environment:
      ```sh
      python3 -m venv env
      source venv/bin/activate
      ```
5. Install the required libraries using `pip`:

    ```sh
    pip install -r requirements.txt
    ```
**Run Jupyter Lab with the Notebook and Data**

To run the Jupyter Notebook with all the data in the GitHub repository, follow these steps:

1. Ensure you are still in the project directory.
2. Start Jupyter Lab:

    ```sh
    jupyter lab
    ```
3. A new tab will open in your default web browser, displaying the Jupyter Lab interface.
4. In Jupyter Lab, navigate to the directory where the notebook file (`.ipynb`) is located.
5. Open the notebook file to begin working with it.


## Assignment Tasks
- **SQL queries (approx. 30 minutes):**
  Work with last month of transactions available in the dataset.
  1. List all customers who made more purchases within 1 week from their first purchase.
  2. Retrieve the top 3 products based on sales quantity.
  3. Calculate the total revenue generated from each product category.
- **Data analysis (approx. 60 minutes):**
  1. Identify trends and patterns:
  ○ Use the data to generate at least two insights that could help improve sales,
  customer retention or analyze product performance, store productivity, etc.
  2. Create visualizations to support your findings:
  ○ Use any tool or library you prefer (e.g., Excel, Python, R, Tableau) to create
  visualizations that support your insights.
- **AI integration (approx. 30 minutes):**
  1. Propose a way to use AI to enhance the business:
  ○ Suggest an AI-based solution, such as a recommendation system for products,
  customer segmentation for targeted marketing, or predictive analytics for
  inventory management.
  
  2. Outline the steps to implement the proposed AI solution:
  ○ Describe the approach and outline the steps required to implement your
  proposed AI solution.

## Assignment explanation

### SQL queries
1. **List all customers who made more purchases within 1 week from their first purchase.**
   - Last month when the purchase was done was 1.1.2003-1.2.2003
   - Customers have missing data
   - Customers are spread arround the world
2. **Retrieve the top 3 products based on sales quantity.**
   - The most popular products were (ranked by the quantity order):
     - **barprianticallybarought** with total of: 32934
     - **ationablebarcallyationpri** with total of: 29873
     - **oughtn stbarantiantiought** with total of: 29813
3. **Calculate the total revenue generated from each product category.**
   - There is a lot of missing data either category_id or category_name
   - Additional cleaning can be introduced, to divide null values (from category_id) to distribute the values to correct categories (using for example names)
   - It seems that categories **Jewelry, Shoes and Electronics** generate the most revenue. **Note**: *Additional cleaning and grouping may reorder the results*
    

### Data analysis
1. **Identify trends and patterns:**
  ○ Use the data to generate at least two insights that could help improve sales,
  customer retention or analyze product performance, store productivity, etc.
    - **Assumptions**: My assumptions from third task SQL queries are confirmed. After cleaning the dataset the order of products stays the same. Using SQL scripts from previous tasks  I combined table and created data.csv which I would load and perform data analysis
2. **Create visualizations to support your findings:**
  ○ Use any tool or library you prefer (e.g., Excel, Python, R, Tableau) to create visualizations that support your insights.
  - **Total revenue week vs month**
       - I calculated total_revenue and now I'm going to visualize this Data
       - First graph will show total revenue by product category for week. Meaning, for customers that purchased another product within a week and I will try to find out in which category they spend the most.
       - The second graph shows which category generated the most for the last month of transactions for all the customers (I'm using a cleaned dataframe)
    - **A little surprise. Home category is the most popular among returning customers. However, Jewelry is all month winner category in total revenue.**
      - *Note: I suggest to to evaluate the graph by the collors, where the brighter color means higher revenue and the darker color lower revenue. (Also notice that y axis is a different number in total revenue)*
       
  - **Top 10 products by Total Profit**
    - So most favourite product is from Women category. It seems to be that this category was very profitable last month. It is closely followed by men adn children category
      -  *Note: This can be a good indication for launching a marketing campaign. Probably this category has a relation to time, season or events occurring during this period of year*


### AI based solutions

1. **Propose a way to use AI to enhance the business:**
○ Suggest an AI-based solution, such as a recommendation system for products,
customer segmentation for targeted marketing, or predictive analytics for
inventory management.

2. **Outline the steps to implement the proposed AI solution:**
○ Describe the approach and outline the steps required to implement your
proposed AI solution.

**Based on the data analysis which I have done, I would suggest the development of a product recommendation system. AI could help to increase sales and customer satisfaction by recommending products that are actually providing additional value to customers.**

**Steps to implement the solution (theoretically):**

1. Collect data from the web. Mostly user interactions, purchase history, browsing patterns, product reviews and demographic + metadata
2. Cleaning the data to remove inconsistencies, duplicates and missing values.
3. Analyze data. Find the patterns. How are customers browsing? What are they purchasing? Is there anything influencing their behaviour (seasonality, weather)
4. Identify top products and products with cross sell opportunities
5. Select the model and evaluate it. How is the model performing? How precisely is the model recommending products?
6. Execute A/B testing, model vs simple recommendation of product from similar category. What is performing better?
7. Asses and improve.
   





