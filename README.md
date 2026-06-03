# Analysis of Prompt Variation on LLM Generated Data Quality
Introduction:
Data is essential for training LLM’s to accurately predict trends, form solutions, and make a beneficial impact on society through synthesis and experimentation. While certain events have been robustly recorded and measured, other fields lack the transparency, funding, and quantity to create a sufficient basis to train AI systems effectively. This is where the urgent need for synthetic data arises, where data for events such as extreme edge cases in autonomous vehicles, frau detection and even human trafficking are precariously sparse. With the use of emerging artificial intelligence technology, the creation of this synthetic data can be streamlined with statistical methods and validated against reference tabular data. Even further the creation of quality synthetic data with an LLM lies in prompt variation, and how differences in verbosity, orthographical efforts, and specificity affect the output.
Methods:
Study Design 
Investigating how prompt variation reflects:
-	Privacy leakage due to “plagiarizing” real dataset
-	Token Efficiency and Cost-Benefit Analysis
-	Sensitivity to small semantic changes
-	Rare events/ Outliers
-	Natural noise (Not extremely rigid)
Prompt Variation will comprise of:
-	Spelling
-	Verbosity
-	Paraphrasing
-	Professionalism
-	Language*
-	Abbreviations*
-	Guardrails*
Pre-Existing Methods
-	GAN: Two neural networks working against each other to reach a common goal with a generator (generating synthetic data) and a discriminator (differentiates fake data from the reference set) with both improving over time
o	CTGAN (Conditional Generative Adversarial Network)
	Forces models to practice generating rare categories as often as the usual ones to accurately reflect outliers or miniscule data
o	CopulaGAN (Coupla Generative Adversarial Network)
	First learns the distribution of each column individually, then uses the GAN to understand the joint distribution
	More proficient at maintaining the mathematical correlation between column variables
-	TabSyn “Diffusion” 
o	Adds noise to the real data until it is destroyed, then reverses the random static to recover realistic data points
o	More stable to train compared to GANS
-	Simulation Experiments

Materials 
	Reference Data Sets
-	Hantavirus Transmission & Risk Dataset
-	AI Usage & Student Academic Performance Analysis
-	Adult Income (Census) Dataset - Dataset | Agents for Data
-	State of Washington - Electric Vehicle Population Data (>200k rows)
-	City of Los Angeles - Crime Data from 2020 to 2024 (>1,000,000 rows)
-	U.S. Department of Health & Human Services - U.S. Chronic Disease Indicators (>300k rows)
Measures 
•	Polars
•	Python
•	NumPy 
•	SciKit-Learn
•	Matplotlib
•	Parlant
Data analysis
Non Parametric Jensen–Shannon Divergence
Kolmogorov–Smirnov Test for Normality
Total Variation Distance
Prompt Examples:
	Professional: Generate 100,000 new rows of data that follows that same statistical distribution of the previous reference data, but adds a little noise to maintain privacy, and accounts for edge cases. 
Professional with guardrails: Generate 100,000 new rows of data that follows that same statistical distribution of the previous reference data, but adds a little noise to maintain privacy, and accounts for edge cases. Do not memorize or plagiarize the data.  Make this synthetic data as realistic as possible, so small deviations from the distribution are allowed.
Casual and generic: Can you pls make like 100,000 more lines of data that follows the same patterns as the old one but is still good and private?
Spelling Mistakes: Create 100k bew linws of data thst follws that same distrivution of the old refetence data, but adds noire to maintaoin privacy, and acciunts forouitlisdr.
Abbreviations: Gen 100k new lines of data that follows that same stat dist of the prev ref data, but adds some noise to maint priv, and accs for edge cases.
Quantity: Generate 100 new lines of data that follows that same statistical distribution of the previous reference data, but adds a little noise to maintain privacy, and accounts for edge cases.
Verbosity: Generate about 100,000 new rows of accurate data keeping consistent with the column information. These rows should continue to follow the statistical distribution present in the reference dataset. In addition, add small amounts of noise, intentionally, to preserve the confidentiality and privacy of the data. Ensure that you are not memorizing the data or plagiarizing from the original set. Instead follow the statistical distribution and create realistic synthetic data. To ensure it’s accuracy, small deviations from the distribution will be necessary to follow user generated content.
Language: (Spanish) Genera 100,000 nuevas filas de datos que sigan la misma distribución estadística de los datos de referencia anteriores, pero que añadan un poco de ruido para mantener la privacidad y tengan en cuenta los casos límite.
Paraphrasing: Create synthetic data based on the reference set provided, but do not plagiarize any of the information. Make it 100,000 rows, with intentional noise inserted to follow privacy guidelines. Small deviations from the reference data set distribution are necessary for accurate and realistic data.


References:
Evaluating Synthetic Data Generation from User Generated Text
Universal Tabular Data Generator with Large Language Models
A Systematic Review of Synthetic Data Generation Techniques Using Generative AI
Quality Matters: Evaluating Synthetic Data for Tool-Using LLMs
Generating realistic synthetic tabular data with integrated LLM and diffusion models
Why LLMs Are Bad at Synthetic Table Generation (and what to do about it)
Benchmarking synthetic tabular data: A multi dimensional evaluation framework (Sidorenko)
