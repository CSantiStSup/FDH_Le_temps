# FDH_Le_temps
Work on the Le_temps database. Using the RDF graph that was extracting from the last 200 years of publication.

In our to respect the confidentiality agreement, we used store our data locally.

# Extracting the information for pulses
In order to search within the set of pulses, we must disambiguate the functions that are 

Model:
"Adam Smith était économiste en 1780"

And we will cut it into:

"#AdamSmith #in #économiste #when #1789"

## 1.1. Mention treatment
In this part we will use the SPARQL outputs in order to make #mention pulses. The parentheses are showing that it is a generic parameter, meaning that the pulse will contain the information that is inside it. The pulses will be the following:


"#Mention #(Name) #in #(title_articleID_pagenumber)"


## 1.2. Source treatment 
The format is:

"#in #(titre)_(artid)_(page) #in #(titre)_(artid) #in #(issue)  " 

## 1.3. Person's function
The format is:

"#(person) #in #(function) #where #(date)"

## 1.4. Person's nationality
The format is: 

"#(person) #in #(nationality)"

## 2. Dealing with locations
##### Data wrangling
We first deal with the SPARQL outputs and then put it in a format that is more convenient to manipulate.

##### Pulse creation
In this part, we will create pulses indicating places that were mentioned in one article. The format is the following:

"#mention #(lieu) #in #(title_articleID_page)"

## 3. Copresence

Identifying the presence of two persons in the same article.

The format is:

"#copresence #(name)
