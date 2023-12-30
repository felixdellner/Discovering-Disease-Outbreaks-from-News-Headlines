# Discovering Disease Outbreaks Starting Repository

Implementation repository for Manning PBC: Discovering and Tracking Disease Outbreaks with Data Science and Python

## Results
649 headlines found a home in the dataframe in the end, 42 missed (of which some should not have been missed depending on capitalization, read more below)

After comparing to the authors solution - I also notice I did not consider that certain cities will appear more than once (for instance in different countries). Oops 🙈
## Commentary

Few things I would have liked to have solved in the end:

- Matching no matter case (Rio De Janeiro vs Rio de Janeiro), easily solved - but leads to other problems (Tons of "cities" called 'Of' and 'Man' will be found). Decided this is likely easier to adjust in the input data instead for this case. For a real case I'd likely dive deeper into what exactly Man and Of is in the city dataset - unsurprisingly "Man City" does not give great Google results 😅
- My regex implementation required me to sort in descending order in the end to ensure 'Miami Beach' would not be caught as 'Miami', there might be better ways to do this than to sort (and I'm sure sorting brings other problems)

However, I'm not too interested in learning Regex - rather the data science. This in addition to most remaining missed headlines being from states (not included in the task) or certain oddities such as military bases makes me feel fairly okay with the solution in the end.
