The goal of this project is to build a fair-value rental pricing framework using the Apartment
for Rent Classified dataset. The project first standardizes listing prices to a monthly basis,
then uses cleaned and transformed listing information to estimate the expected monthly rent
of each unit. Based on the difference between the actual listed price and model-predicted
price, the system further classifies listings into practical pricing bands such as Deal, Fair, and
Premium. This allows the output to be interpreted not only as a prediction task, but also as a
decision-support tool.

This project belongs mainly to the area of supervised regression with decision support. At a
basic level, the task is to estimate the expected monthly rent of a rental listing from its
observable characteristics, such as housing structure, location, and amenities. However, in
this project, rent prediction is not treated as a purely technical forecasting task. Instead, it is
used to support a practical pricing decision: whether a listing appears underpriced, fairly
priced, or overpriced relative to its estimated fair value.

Overall, this project is designed as an end-to-end data science pipeline that connects data
understanding, preprocessing, exploratory analysis, modeling, and interpretation. Rather than
focusing only on model accuracy, the project emphasizes decision value: whether the
resulting system can provide stakeholders with a more consistent and evidence-based way to
evaluate rental prices.
