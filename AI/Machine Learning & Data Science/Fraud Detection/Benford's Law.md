Benford's Law is a statistical phenomenon about the frequency distribution of leading digits in many naturally occurring datasets. Here's the core idea:
### The Law
Benford’s Law states that in many real-world datasets, the first digit ddd (from 1 to 9) is **not uniformly distributed**. Instead, smaller digits appear as the leading digit more often. Specifically, the probability that the first digit is ddd is:

$$P(D = d) = log_{10} (1 + 1/d)$$
So for example:
$$
\begin{align*}
P(1) &\approx 30.1\% \\
P(2) &\approx 17.6\% \\
P(9) &\approx 4.6\%
\end{align*}
$$
This is counter-intuitive because we might expect each digit to occur roughly 11% of the time if it were uniform.

### Why It Happens
Benford’s Law arises in datasets that span several orders of magnitude and are not artificially constrained. Examples include:
- Financial transaction amounts
- Populations of cities
- Stock prices
- Accounting figures

It **doesn’t apply** to datasets that are capped or artificially rounded (like human heights in cm, which are normally 150–200 cm).

### Application to Fraud Detection
The key idea in fraud detection is that humans are **bad at mimicking Benford’s Law**. If someone invents numbers or manipulates data:
- They tend to pick digits more uniformly or subconsciously favour certain numbers.
- This leads to deviations from the expected Benford distribution.

By analysing the distribution of first digits (or even second digits, which have a variant law), auditors can flag datasets for further investigation. For instance, if an accounting ledger shows 1 as the first digit only 15% of the time instead of 30%, it might indicate manipulation.

### Limitations
- Not all datasets should follow Benford’s Law.
- Small datasets or datasets with limited ranges can naturally deviate.
- It’s a **red flag tool**, not proof of fraud.

