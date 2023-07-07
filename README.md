# pandas-challenge


For this challenge all of the instructions were pretty straight forward but I think that the tricky part resided in this part of the code: 



spending_bins = [0, 585, 630, 645, 680]
labels = ["<585", "$585-630", "$630-645", "$645-680"]

school_spending_df = per_school_summary.copy()

# Categorize spending based on the bins
school_spending_df['Spending Ranges (Per Student)'] = pd.cut(school_spending_df['Per Student Budget'], bins=spending_bins, labels=labels)

where the instruction pd.cut form pandas library gave me a har time and I had to rewrite the code several times so it transform to :

# Use pd.cut to categorize spending based on the bins
per_school_summary["Spending Ranges (Per Student)"] = pd.cut(
    per_school_summary["Per Student Budget"], bins=spending_bins, labels=labels, right=False
)

# Display the updated DataFrame
per_school_summary

in order to be able to write this last part of the codes https://pandas.pydata.org/docs/reference/api/pandas.cut.html
