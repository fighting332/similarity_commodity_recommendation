This project for similarity-based commodity recommendation was built by Xianyao Chen, 
when serving for the e-commerce company (MiX:D, 믹스디 주식화사) in South Korea.

The project first extracts the purchase history data from MySQL database and upload data to Amazon S3 for processing. 
In Amazon SageMaker platform, the similarity among different commodities is computed using Jaccard similarity technique, 
based which the commodities with large similarity are classify as the same category. 
Then, a lookup table is created in the server. Each commodity in the table has a list of similar commodities, 
which are listed by descending order of similarity score. 
For a future purchase, the similar commodities will be recommended to the customer.

[1] Target: Similar commodity recommendation

[2] Background: Based on the SQL database, extract two tables describing commodity information:

A. In input_commodity_information/commodity_item.csv file, cit_ID is commodity ID, cit_name is commodity name.

B. In input_commodity_information/commodity_category_relationship.csv file, cit_ID is commodity ID, cca_ID is categories ID which commodity belongs to.

[3] Techniques:

A. Data pre-procecssing: remove the noise of commodity name.

B. Create a dictitionary <key, value>: key is category ID, value is commodity ID, i.e., all of these commodities have the same category ID.

C. Jaccard similarity: calculate the similarity score for the commodities, and sort commodity IDs in descending order.

[4] Result: For a given commodity ID, output the similar commodity IDs in descending order of similarity score.

In output_recommodation_commodity/recommodation_repository.csv, cit_ID is commodity ID, similar_ID is the similar commodity IDs. 
The list of similar_ID is sorted in descending order of similarity score.
