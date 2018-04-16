# API Highways : "Poverty Headcount Ratio at $1.90/day (2011 PPP) (% of Population)
###### xxxx

Following my [1st experience]("https://github.com/mbeveridge/SDG-API_Extreme-Poverty") of using [API Highways]("https://apihighways.org/data-sets"), and some difficulties, I wanted to see whether this was typical (re. "whether the site would be a good source of datasets to practice on").

I hadn't intended the next dataset to be 'the same' as the 1st one (but from "World Bank Group" instead of "Data Development Hub"), but decided it may be an interesting comparison.

As before, I wanted to use R for the analysis, and Python code was listed on the dataset's page.

---

Didn't try an RMarkdown notebook, because last time it felt like **reticulate** may not work in my setup (yet), rather than my code being the issue. (This dataset's page doesn't link to a csv version)

---

Began with `Extreme-Poverty.ipynb` from the '1st experience' and renamed it `Extreme-Poverty_(WorldBank).ipynb`. (With a little more research) I found a way to exclude the "'meta' data at the end", and got the JSON data into a **pandas** dataframe (but still wonder if there's a way to do it 'more directly', with `pd.read_json(data)`).

Compared with the '1st experience', this dataframe has a lot of columns (62), but 57 are the years 1960-2016, and I'd probably want to pivot (to make the 57 into 2 'Year' and 'ratio' columns).

Compared with the '1st experience', I also got the `df` dataframe from Python into R (via **rpy2**), and assumed usable (from very basic testing) by **dplyr** and **ggplot2**. TO BE CONTINUED

