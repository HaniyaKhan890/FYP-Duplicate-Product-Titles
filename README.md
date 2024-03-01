# Detecting Duplicate Product Titles in Foodpanda's Product Catalog 

## Approach:

Our strategy for identifying duplicate product titles involves using a similarity algorithm called jaccard_similarity that gives a measure of similarity between two sets. It is defined as the size of the intersection of the sets divided by the size of the union of the sets. 

### 1. Title Cleaning:

The initial step focuses on refining titles to ensure that maximum amount of duplicate titles can be detected. This involves various transformations to enhance the quality and relevance of the data. By cleaning the titles, we aim to provide a solid foundation for the subsequent stages of the process.

#### 1.1 Cleaning Data for Specific Categories:

To clean the data, we thoroughly examined the datasets within the specific domains of Snacks & Confectionery and Baby Care. We encountered distinct issues in each category and the cleaning procedures varied between these categories as they had different kinds of products. 

To clean the data for each category, navigate to the following path:
`<Duplicate Titles categoryName><categoryName>_dataCleaning.ipynb`
Run all cells in the notebook, and the result will provide an excel file ready for use in detecting duplicate product titles.

#### 1.2 Detecting Duplicate Product Titles

After cleaning the data from both categories, we used jaccard similarity for sets of tokens to figure out how similar 2 products were. Then we iterated over similar pairs to find duplicates. To get a good accuracy, we set a similarity threshold for considering products as duplicates high at 0.80 so we got good accuracy. Then we stored similar products agaisnt their respective mastercodes. This will be done using the cleaned file of product titles that we got as an output using 1.1, and to get the duplicate titles we will go to 
`<Duplicate Titles categoryName><categoryName>_duplicateProductNames.ipynb`. After entering this file we will run all the cells to get the final output in an Excel file. 

## Results:

The final output will be an excel file with 2 columns. The first column will include the mastercodes of the similar products in this format: {mastercode1, mastercode2} and the next column will conntain the duplicate product in the format {dairy milk 200g, dairy milk chocolate 200g}. 


