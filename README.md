Problem Set 5: Right 93% of the Time

David Xu · ECON 3916

Notebook: Econ_3916_PS5.ipynb. All loans and dollar outcomes are simulated.

Recommendation to the head of risk

Do not sign on the strength of the 93% figure. Pilot the model with a 16% decline cutoff instead.

The 93% accuracy proves nothing: approving every applicant is right 93.1% of the time and catches no defaults. Our model is only 0.4 points more accurate than that. Its value shows up in money, not accuracy. On 6,000 held-out simulated applications, approving everyone lost $1,051 per application; the model at the recommended cutoff lost $713, a saving of $339 per application. It caught 200 of 413 defaults and wrongly declined 478 of 5,587 good applicants. A random forest did no better (no significant difference), so there is no case for paying for the more complex model.

Recommended cutoff: decline applicants whose calibrated default probability exceeds 16%, not the usual 50%. At 50% the model catches only 49 defaults. The cutoff assumes a defaulted loan costs 60% of principal and a wrongly declined good applicant costs 9% (8% lost interest margin plus 1% lost future business). The general rule: decline when default probability exceeds the decline cost divided by the sum of both costs. Any cutoff between 13% and 19% performs about the same.

What would change my answer: loss given default. The model beats approving everyone as long as defaults cost more than about 21% of principal. If recoveries on this book are high enough to push losses below that, declining stops paying and I would not sign.
