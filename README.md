## Capstone 2 proposal

### Idea 1: Predicting your race results (definitely can get the data)
*High Level Description*: Runners who race multiple distances want to know what times they are theoretically capable of using past race results in different distances.  By using race results for individuals who have run various distances, I can create a model that will predict a person’s time in a distance given their time in other distances.

*Approach*: By using data from 5 years’ worth of New York Road Runners races, I will track thousands of individuals across age groups who have competed in 1 mile, 5k, 13.1mi, and 26.2mi races to build models that will predict a person’s potential race times given their gender, age group, and at least one previous race time in one of those four distances.  A lot of work will have to be done to get the training set in order.  The data will be narrowed down to people who ran all four distances while competing in the same age group (meaning if a person ran 3 of the distances while in the 30-34 age group but the 4th while in the 35-39 age group, they will be excluded).  In the case that a runner ran a distance multiple times (say, the NYC marathon in 2018 and 2019), I will use their best time for a distance.  I will use a random forest regressor to build this model, when the model is used it is not guaranteed which data points (previous race results) the person will provide when they use the model (as I understand it the random forest regressor can handle incomplete data … but I might be wrong!).  
*How will people interact with your work*: Ideally I will build something where people can enter in previous race times and get a prediction.

*How will people interact with your work*: People will be able to use some sort of interface (which I will learn about…) to use their previous race times to predict future ones.

*Data source*: Race results from NYRR.org.  An aside: I am not super psyched about using the same data source but I believe it is the best one for this project because a large number of runners run multiple races with NYRR and therefore it will be easy to find people who have run all 4 distances.  This will be much more challenging than my last project as I will have to scrape much more data and have to to considerable amounts of data wrangling before I can even do any sort of analysis.  I’m not super psyched about using the same data source twice but with what I know of other results sites this is the one that contains the data points I need in a quantity that will be useful in a relatively easy to use format.  I came up with this idea partially out of desperation to come up with something else, but I actually think it’s cool, has a tangible benefit, has a good shot at actually being reasonably accurate, and will result in a product people can use (though this kind of thing exists already, but no one needs to know that).  It will also be challenging because I will have to build something that is flexible for different inputs and outputs (depending on which distances are the datapoints and which distance is the target based on the user’s input).

### Idea 2: Wage growth (Definitely can get the data I am eyeing but maybe will find that it's not good for my purpose)

*High Level Description*:  What contributes to upward mobility?  By studying longitudinal data of a cohort of baby boomers, I will explore the social as well as economic factors that factor into wage growth over a person's lifetime.  It is an established fact that women and people of color earn less on average than white men, often for the exact same work, and the causes of the wage gap has been exhaustively studied with reasons ranging from chosen industry to the “motherhood penalty,” as well as outright discrimination.  Wage growth can be seen as a proxy for career advancement and by studying it I can infer what factors are associated with upward mobility.

*Approach*: The National Longitudinal Study of Youth (1979) provides longitudinal demographic information of people born in the years 1957 - 1964 so I could potentially track hundreds of details about these people's lives over the course of the years 1979 - 2016.  From the data I will pull a large number of factors that I believe could affect someone's wage growth in their life and use linear regression to do inferential analyses, teasing out the factors that most greatly affect wage growth as well testing the predictive power of my model.  I also may use a random forest regressor because of the number of potential interactions within variables that mean that a linear relationship cannot be assumed. There are likely many factors that contribute to wage growth in addition to gender: industry, race, education, geographic region, family structure, attitudes about discrimination, etc and I will study these factors as well as potential interactions as well. 

*How will people interact with your work*: I will present with slides and write up a notebook.

*Data source* [The National Longitudinal Survey of Youth 1979](https://www.nlsinfo.org/investigator/pages/login).  I am confident I can get this data, but I might find that I'm not able to find super insightful results from it just because there are likely other factors that contribute towards wage growth that I won't be able to capture.

### Idea 3: not sure if I can get the data 

*High level description* 

The Bechdel test for movies is a test with simple criteria for passing: there must be two named female characters who have a conversation about something other than a man.  Author Allison Bechdel made it up as part of a comic strip and its darkly comical and dismally low bar for passing purposefully highlights the lack of substantive stories about women in film.  Even as women have grown to have more of a presence in films, often their most important character trait is their relationship to a more significant male character.  Just over half of films in recent years pass the Bechdel test despite its very simple criteria. It is common that the vast majority of Best Picture nominees at the Oscars do not pass.  If we can understand the factors that are associated with the films that pass and fail, inroads can be made to diversify the stories that are told.I will build a model that will provide insight into the facts that lead to a film passing the test, which could have implications for the film industry.

*Approach*  I will perform both a logistic regression and a random forest regression. such as genre, budget, box-office figures, gender composition of the top-billed actors, featured award-winning actresses, directors, and screenwriters, among others.  I would like to study the gender of the cast/crew, but I suspect it will be impossible to perfectly categorize people because it would likely have to be done manually, which has issues.  The only people who I could confidently classify by gender would be people who have won a Best Actress award.

*How people will interact with your work*:  I will present with slides and write up a notebook.


*Data source*
[BechdelTest.com](http://bechdeltest.com) for an exhaustive list of films and whether or not they passed.

[IMDB.com](http://imdb.com) for budget, cast and crew information

Various CSV files that lists of all Emmy and Oscar winners

