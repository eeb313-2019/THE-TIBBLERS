## Data cleaning

In order to make our data set more manageable and clear, we will employ the following data cleaning plan. First, we will remove any variables in our data set that are repetitive, non-standardized, or have questionable explanations as to how they were determined. Such variables include: Standardized_predator_length, Prey_conversion_to_length_method, and Prey_conversion_to_length_reference. 

We will then get rid of columns that contain mainly N/As such as the Prey_width and Prey_width_unit columns. 

We will also consider the conversion quality of the columns Predator_quality_of_length-mass_conversion, Prey_quality_of_conversion_to_length, Prey_quality_of_conversion_to_mass, and remove data with a quality rating of 4 or 5 (quality is ranked on a scale: 0 = mass measured, 1 = species regression, 2 = genus regression, 3 = family regression, 4 = general shape, 5 = unsatisfactory). 

We will also be selective within the Specific_habitat column; we will likely remove “transitional” habitat since there is only one study that includes it. Instead, we would focus on the habitats that have multiple studies across multiple locations. We also will need to go through the habitat names and ensure that habitats are labelled consistently (ex: is there a difference between “Shelf” and “shelf”?), and research the habitat types to further filter out the ones that are not of interest to us. 

We might also decide to focus on only a few species of predators that are common across studies, and remove those that only appear once. For example, the 4-spot megrim was only caught in one study and would not be suitable for our research questions. We may also remove predators with a low number of observations. 

# Possible analyses

For our initial data analysis, we will likely use PCA to test if correlations between variables exist and condense the number of variables used in further analysis. 

Since our project hypothesis is likely going to revolve around differences across geographic locations, it will be important to conduct Moran’s I tests to see if there exists spatial autocorrelation within our variables of interest. We will also make use of our “Longitude” and “Latitude” columns and generate maps to visualize the distribution of our variables of interest globally, or regionally. 

Once we have a better idea of how our variables relate to each other across space, we will perform model selection. We can use AICc testing to determine what model best represents our variable relationships.

We may also employ permutation tests if we find that our data is not normally distributed.

# Possible results tables

Our PCA test will output a table output that includes PCA columns and coordinates.

Our Moran’s I tests will output p-values which we will use to determine if there is autocorrelation.

From our model selection, we will get a table of AICc values which we will use to determine which model is best (lowest AICc value).

Permuation tests will output tables that give statistical values (t-test, p-values, etc.).

# Possible results figures

From our PCA coordinates we will generate a biplot to visualize the relationships between our variables.

From our spatial analysis, we will generate maps to visualize the distribution of our variables. These maps may be on a global scale, but may also include more specific regional maps depending on our specific question.

ggplot will be used to create graphs to visualize our models (scatterplot, boxplot, barplot, etc.).

We will also generate histograms of permutation test distributions if used.
