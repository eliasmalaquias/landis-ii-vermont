Beginning with LANDIS-II to study Vermont forests
================
Elias M. Guerra
Fall 2017

*This is a edited version of my senior independent biology project using the landscape simulation model LANDIS-II. It seems to be turning into more of a manual than a lab report.*

#### Introduction

Climate and land use change are having tremendous impact on the natural environment and in turn on humans. In the Northeast, prior to European settlement, the forests were largely untouched. Beginning around 1650, two centuries of logging and agricultural clearing removed or cut almost all forest. In the mid-nineteenth century, agricultural expansion into the midwest and eastern industrialization led to population concentration in urban areas and widespread farm abandonment. This caused two centuries of natural reforestation which has continued until recently. A comparison of pre-colonial and modern forests based on archival, colonial land-survey notes and modern data from the Forest Inventory Analysis database found that while most major tree species remain 1) the relationship between forests composition and the environment has weakened and 2) pre-colonial forests were compositionally more homogenous at short distances and more heterogenous at longer distances.

First, among environmental variables, temperature had the strongest association with forest composition. In the modern forests temperature is still the most important environmental variable but the relationship is much weaker. After temperature, elevation and sand were historically and are still the most important environmental variables. Secondly, pre-colonial forests in the south were dominated by oak and hickory and dissimilar to the spruce-fir forests farther north. In the modern forests, maple is a significant component regardless of location. In general, the modern forest does not represent the original mosaic of forest-types influenced with strong climate-driven compositional gradients. Agricultural land cover continues to decline but the land transition to development now overrides reforestation (Figure 1, Thompson et al. 2013).

![](README_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-1-1.png)

##### Figure 1. Pre-colonial and modern forest of the Northeast U.S. *Thompson et al. (2013)*

First, among environmental variables, temperature had the strongest association with forest composition. In the modern forests temperature is still the most important environmental variable but the relationship is much weaker. After temperature, elevation and sand were historically and are still the most important environmental variables. Secondly, pre-colonial forests in the south were dominated by oak and hickory and dissimilar to the spruce-fir forests farther north. In the modern forests, maple is a significant component regardless of location. In general, the modern forest does not represent the original mosaic of forest-types influenced with strong climate-driven compositional gradients. Agricultural land cover continues to decline but the land transition to development now overrides reforestation (Thompson et al. 2013).

Global circulation models agree that the Northeastern US climate will become warmer. Patterns of precipitation are less clear. Possible effects may be increased growth due to a longer growing season, decreased growth in summer months due to greater respiration and evapotranspiration, and shits in tree species ranges. Different species are expected to react differently depending on the life history traits (eg. shade tolerance, thermal tolerance. Duveneck et al. 2016). Harvesting wil be an additional pressure because of growing demand for renewable energy resources like forest-derived biomass for biofuels (Benjamin et al 2009).

In order to understand how climate change and land development will impact the Northeast in future, simulation models are very useful. Computer models of forest change first developed in the late 1960s and early 1970s as researchers in landscape ecology were confronted with the limitations of empirical studies. Experiments over large spatial and temporal scales are often not feasible, hence simulation models. Since the first models such as JABOWA and FOREST appeared, increasing complexity in ecological sciences and landscape models has necessitated advanced models that are not simple caricatures of well-functioning landscapes. Spatially-dynamic models, such as LANDIS-II, are very useful for studying large landscapes while robustly simulating disturbance and succession (Mladenoff et al. 2004, Scheller et al. 2007).

Thompson et al. (2011) used LANDIS-II to model Massachusetts forests by applying scenarios with different climate and harvesting regimes to a simulation over 50 years (2010—2060). They arrived at a few conclusions: First, the largest change in aboveground biomass (AGB) was simply the result of continued stand growth and succession. Even with a continuation of the trends of greater land use and effects of climate change, the simulation predicted a 65% increase in AGB over 50 years (Figure 2). Whether all forests types will continue to be able to accumulate biomass is uncertain.

![](README_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-2-1.png)

##### Figure 2. Change in aboveground biomass over a fifty-year simulation with LANDIS-II. *Thompson et al. (2011)*

Scenarios A-H are various combinations of the treatments climate change (CC), standard climate (SC), forest conversion (FC), and harvesting (Harv). The inset histogram shows change from year 0 to year 50 for each scenario.

Second, after growth and succession, forest conversion to developed land had the largest (negative) impact on AGB. Forest conversion was more than four times as destructive as timber harvesting even though harvesting occurred over twice as much area. Third, anthropogenic climate change will have a net positive impact on AGB because of increased temperatures and precipitation. Over 50 years, climate change resulted in a 5.5% greater accumulation of AGB. Fourth, the community composition is shifting to dominance by late-successional species (ie. Tsuga canadensis, Fagus grandifolia). Thompson et al. (2011) did not take CO2 fertilization into account. The model also lacked various types of disturbances such as hurricanes, insect pests, disease, etc. Therefore the model is not totally realistic but instead gives some ideas about the importance of different factors like succession, climate change, and harvesting. The authors suggest that their model is not supposed to represent a prediction of the future, but rather a continuation of the current trends of development, timber harvesting, and growth and succession.

Duveneck et al (2016) used LANDIS-II with the PnET extension to simulate the effects of climate change on New England over 100 years. Using several global climate models (GCM), the simulation indicates that climate change will increase biomass of the forests, particularly along the Atlantic coast, in comparison to climate scenarios based on current conditions. Current climate created a 34% increase in AGB by 2110, while the various climate change scenarios on average created at 82% increase in AGB. Specifically, climate change caused increased AGB in already dominant forest types (northern hardwood, spruce-fir, and pine). As proportions of total AGB, northern hardwood decreased while spruce fir and pine increased. Unlike Thompson et al. (2011), which used biomass succession, Duveneck et al. (2016) were able to include climate extremes in the model by making use of the PnET succession extension. Besides direct climate effects, other biological and anthropogenic disturbances were not included in their model.

#### About LANDIS-II

The two studies discussed mades use of LANDIS-II, a physiologically-based, spatially explicit mechanistic model. LANDIS-II is mechanistically simplistic, compared to more complex, fine-scale models like SORTIE which simulates individual trees. This is necessary to simulate large landscape (10-100,000 hectares). Since the original model, LANDIS-II has become more realistic with development of extensions like biomass and PnET, but it still does not model individuals. Succession is based on interactions between species life history attributes (Table 1), site conditions, and disturbance.

| Parameter                              | Units   |
|:---------------------------------------|:--------|
| Longevity                              | years   |
| Sexual maturity                        | years   |
| Shade tolerance                        | meters  |
| Seed dispersal (effective and maximum) | meters  |
| Resprouting age (minumum and maximum)  | years   |
| Resprouting probability                | 0-1     |
| Post-fire regeneration                 | boolean |

##### Table 1. Species life history attributes and units for LANDIS-II.

The landscape is represented by a grid of interacting cells at a user- defined spatial resolution, where each cell represents a different community.

![](README_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-4-1.png)

##### Figure 3. Example initialization map for LANDIS-II. *LANDIS-II Model v6.0 Conceptual Description (2012)*

Within each community, species are represented by age cohorts. Cells are aggregated in ecoregions of homogenous climate and soil conditions. The model can be conceptually represented as a series of repeating cycles that operate on the initial communities.

![](README_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-5-1.png)

##### Figure 4. Conceptual diagram of LANDIS. *Mladenoff (2004)*

First species are filtered based on their ability to exist and reproduce on a site which varies by ecoregion. The species establishment coefficient (previously SEC, now Pest for probability of establishment) determines a species’ success and encapsulates response to nutrients, moisture, and other environmental conditions. Next, succession occurs based on the species life history attributes, such as shade tolerance and longevity. Disturbances such as windthrow, fire, and harvesting follow. These disturbances cause mortality and the cycle begins again. The data input that LANDIS-II requires include the species life history attributes, a raster map of the initial communities, a raster map of ecoregions, and any disturbance or climate data. Based on these LANDIS-II will output raster maps representing various statistics (eg. species median age) which then require analysis (Mladenoff et al. 2004, Scheller et al. 2007).

This project was simply getting LANDIS-II to run. My study area was limited to Vermont. I used a variety of freely available datasets to set up the model. Because the focus of this project was simply to practice using LANDIS-II the model output should not be interpreted as useful for other research or practical purposes.

#### Running LANDIS-II

In order to begin running LANDIS-II we'll need all forms of the input data starting with the species life history attributes...

![gif](https://media.giphy.com/media/y1ZBcOGOOtlpC/giphy.gif)

#### References

1.  Benjamin, J., Lilieholm, R.J. and Damery, D., 2009. Challenges and opportunities for the northeastern forest bioindustry. Journal of Forestry, 107(3), pp.125-131.
2.  Duveneck, M.J., Scheller, R.M., White, M.A., Handler, S.D. and Ravenscroft, C., 2014. Climate change effects on northern Great Lake (USA) forests: a case for preserving diversity. Ecosphere, 5(2), pp.1-26.
3.  Duveneck, M.J., Thompson, J.R., Gustagson, E.J., Liang, Y., and M.G. de Brujin, Arjan. 2016. Recover dynamics and climate change effects to future New England forests. Landscape Ecology 32(7): 1385-1397. <https://doi.org/10.1007/> s10980-016-0415-5.
4.  Duveneck, M.J., Thompson, J.R. and Wilson, B.T., 2015. An imputed forest composition map for New England screened by species range boundaries. Forest Ecology and Management, 347, pp.107-115.
5.  Link to LANDIS-II Github page: <https://github.com/LANDIS-II-Foundation>
6.  Mladenoff, D.J., 2004. LANDIS and forest landscape models. Ecological modelling, 180(1), pp.7-19.
7.  Scheller, R.M. and Mladenoff, D.J., 2004. A forest growth and biomass module for a landscape simulation model, LANDIS: design, validation, and application. Ecological Modelling, 180(1), pp.211-229.
8.  Scheller, R.M., Domingo, J.B., Sturtevant, B.R., Williams, J.S., Rudy, A., Gustafson, E.J. and Mladenoff, D.J., 2007. Design, development, and application of LANDIS-II, a spatial landscape simulation model with flexible temporal and spatial resolution. ecological modelling, 201(3), pp.409-419.
9.  Scheller, R.M., Van Tuyl, S., Clark, K., Hayden, N.G., Hom, J. and Mladenoff, D.J., 2008. Simulation of forest change in the New Jersey Pine Barrens under current and pre-colonial conditions. Forest Ecology and Management, 255(5), pp.1489-1500. 10.Simons-Legaard, E., K. Legaard, A. Weiskittel. 2015. Predicting aboveground biomass with LANDIS-II: a global and temporal analysis of parameter sensitivity. Ecological Modelling 313: 325-332. 11.Thompson, J.R., Foster, D.R., Scheller, R. and Kittredge, D., 2011. The influence of land use and climate change on forest biomass and composition in Massachusetts, USA. Ecological Applications, 21(7), pp.2425-2444. 12.Thompson, J.R., Carpenter, D.N., Cogbill, C.V. and Foster, D.R., 2013. Four centuries of change in northeastern United States forests. PLoS One, 8(9), p.e72540. 13.Xu, C., Gertner, G.Z. and Scheller, R.M., 2007. Potential effects of interaction between CO2 and temperature on forest landscape response to global warming. Global Change Biology, 13(7), pp.1469-1483.
