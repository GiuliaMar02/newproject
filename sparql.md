

PROJECT STEPS



STEP 1 

RESEARCH ABOUT OUR TOPIC

QUERY 1

The first step is to run a query to check whether there is an entity in ArCo representing the topic we have chosen. 

EXPLANATION of the keywords used:

The keyword DISTINCT serves to eliminate duplicates.

FILTER and REGEX are useful keywords to get more specific information about our topic: the FILTER keyword in SPARQL is used to filter the results based on certain conditions. It allows you to specify a condition that must be met for a result to be included. The REGEX function is used to perform regular expression matching on the specified string.

“cp” stands for Cultural Property. 




 PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
 PREFIX arco: <https://w3id.org/arco/ontology/arco/>
 PREFIX a-cd: <https://w3id.org/arco/ontology/context-description/>

 SELECT DISTINCT ?cp
 WHERE {
 ?cp a arco:HistoricOrArtisticProperty ;
 rdfs:label ?l .
 FILTER(REGEX(?l, "Abbazia di Nonantola", "i"))

 }



RESULTS:

The results confirm that there is an entity in ArCo representing our topic. These IRIs will be useful later on as subjects for the triples we will create with the missing information. 





COPY OF THE RESULTS:











QUERY 2:

We run this query using the keyword OPTIONAL to find depictions or representations of the Abbazia so as to be more precise with our research. We took out DISTINCT and left “*” to find every possible result. 



PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>

PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>

PREFIX arco: <https://w3id.org/arco/ontology/arco/>

PREFIX a-cd: <https://w3id.org/arco/ontology/context-description/>

PREFIX foaf: <http://xmlns.com/foaf/0.1/>

 

SELECT * 

WHERE { 

  ?cp a arco:HistoricOrArtisticProperty ; 

      rdfs:label ?l .

 

  FILTER(REGEX(?l, "Abbazia", "i"))

  FILTER(REGEX(?l, "Nonantola", "i"))

 

  OPTIONAL { ?cp foaf:depiction ?depiction }

}





RESULTS: by running this query we found the same results (duplicated, because we took out DISTINCT) with their corresponding depictions:











QUERY 3:

Then, we used the following query to find more material about the Abbazia di Nonantola. In fact, this query is searching for unique resources that are classified as "Subjects" (according to the ArCo ontology) and have a name or title that includes the words "Abbazia" and “Nonantola”.



PREFIX a-cd: <https://w3id.org/arco/ontology/context-description/>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>

 SELECT DISTINCT ?subject ?label
 WHERE {
  ?subject a a-cd:Subject ;
           rdfs:label ?label .

  FILTER (REGEX(?label, "Abbazia", "i"))
  FILTER (REGEX(?label, "Nonantola", "i"))
 }



RESULTS:

We have discovered that the Abbazia of Nonantola is also called “Abbazia di San Silvestro”. We thought that this other denomination could be a relevant information to enrich the cultural property of the abbey.













Query 4: 

In this query we used the keyword UNION to find all the information regarding the Abbazia of Nonantola o the Abbazia di San Silvestro, even if we knew that the result may indicate the same Abbazia under different names.

EXPLANATION of the keyword used:

The keyword UNION allows us to query for alternative patterns, which means that either one pattern or another (or both) can match.
 

PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX arco: <https://w3id.org/arco/ontology/arco/>
PREFIX a-cd: <https://w3id.org/arco/ontology/context-description/>

 SELECT DISTINCT ?cp
 WHERE {
   {
     ?cp a arco:HistoricOrArtisticProperty ;
         rdfs:label ?l .
     FILTER(REGEX(?l, "Abbazia di Nonantola", "i"))
   }
   UNION
   {
     ?cp a arco:HistoricOrArtisticProperty ;
         rdfs:label ?l .
     FILTER(REGEX(?l, "Abbazia di San Silvestro", "i"))
   }
 }



RESULTS

We see that the results are the same ones of the first query: two IRI about the Abbazia di Nonantola, meaning that “Abbazia di San Silvestro” does not exist as a “cp”, only as “subject”. 





QUERY 5: 

Now that we have gathered all the information related to “Abbazia di Nonantola” we want to see if we can add more information. To do that, we make a comparison between our abbey and other abbeys present in the ArCo Ontology. 

The following is a query used to find “abbazia” as a general entity. Since we already know that we will find many results, we use the keyword LIMIT 30 to limit the number of results.

PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> 

PREFIX arco: <https://w3id.org/arco/ontology/arco/> 

PREFIX a-cd: <https://w3id.org/arco/ontology/context-description/> 

 

SELECT DISTINCT ?cp 

WHERE { 

 

?cp a arco:HistoricOrArtisticProperty ; 

 

rdfs:label ?l . 

 

FILTER(REGEX(?l, "abbazia", "i")) 

 

}

LIMIT 50





RESULTS: 

This query did not help us because 46 out of 50 results are elements referred to the same abbey and were therefore useless. We then decided to make another query searching specifically for the vocabulary of the properties. 

QUERY 6:

We use the following query with PROPERTY and VALUE to find which properties are used to describe the cultural properties labelled “abbazia”. To order our results we built the query using the keyword ORDER BY. 

Afterwards, we used CTRL+F to search for keywords in order to see if there are any properties related to those concepts (e.g., "committent", "style"...), since this information is missing from the IRI of the Abbey of Nonantola and we would like to add it by referring to existing vocabulary.

 

PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> 

PREFIX arco: <https://w3id.org/arco/ontology/arco/> 

PREFIX a-cd: <https://w3id.org/arco/ontology/context-description/>

PREFIX cis: <http://dati.beniculturali.it/cis/> 

 

SELECT DISTINCT ?property ?value 

WHERE { 

 

  ?cp a arco:HistoricOrArtisticProperty ; 

      rdfs:label ?l ; 

      ?property ?value . 

 

  FILTER(REGEX(?l, "abbazia", "i")) 

 

} 

 

ORDER BY DESC(?property)



RESULTS:

Discussion of the results in STEP 2, section ”Identification of the second missing information”

