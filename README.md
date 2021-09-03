# similarity_commodity_recommendation
 This project of similarity commodity recommendation was finished by Xianyao Chen, who worked for E-commerce company (MIX:D,  믹스디) of Sourth Korea in 2021.
 
 [1] Target: Input commomdity id, output the similarity commodity id with descending score of similarity.
 
 [2] Background: Based on the SQL database, extract two tables describing commodity information:
 
 A. In input_commodity_information/commodity_item.csv file, cit_id is commodity id, cit_name is commodity name.
 
 B. In input_commodity_information/commodity_category_relationship.csv file, cit_id is commodity id, cca_id is categories id which commodity belongs to.
 
 [3] Techniques:
 
 A. Data pre-procecssing: remove the noise of commodity name.
 
 B. Make a dict: key is category id, value is commodity id. All of the commodity id have the same category id.
 
 C. Jaccard similarity: calculate the similarity of commodity name. 
 
 [4] Result: Given the input commodity id, output similarity commodity id with descending score of similarity  
 
 In output_recommodation_commodity/recommodation_repository.csv, cit_id is commodity id, cca_id is the similar commodity id. The list of similar_id is sorted by descending score of similarity.
 
