# Data Acquisition and Statistical Data Visualization with Seaborn

**Presenter:** Olusola Timothy Ogundepo  
**Institution:** African Institute of Mathematical Sciences, Rwanda  
**Date:** October 6, 2025

![AIMS Rwanda Logo](images/logo.png)

## Overview

This repository contains a comprehensive end-to-end walkthrough covering:
1. **Ethical data acquisition** (including a mini web scraping demonstration)
2. **Quick exploratory data profiling**
3. **Building interpretable statistical graphics with Seaborn**

The presentation demonstrates practical techniques for acquiring, exploring, and visualizing data using Python, with a focus on statistical visualization best practices and ethical data collection methods.

## 📋 Table of Contents

1. [Motivation & Goals](#motivation--goals)
2. [Ways to Obtain Data](#ways-to-obtain-data)
3. [Web Scraping Overview](#web-scraping-overview)
4. [Why Web Scraping Matters (Ethics & Use Cases)](#why-web-scraping-matters)
5. [Python Libraries for Scraping](#python-libraries-for-scraping)
6. [Mini Scraping Demo (Books to Scrape)](#mini-scraping-demo)
7. [Loading Local Datasets](#loading-local-datasets)
8. [Quick Automated EDA](#quick-automated-eda)
9. [Seaborn Fundamentals](#seaborn-fundamentals)
10. [Univariate Distributions](#univariate-distributions)
11. [Bivariate Numeric Relationships](#bivariate-numeric-relationships)
12. [Categorical vs Numeric Visualizations](#categorical-vs-numeric-visualizations)
13. [Multivariate & Matrix Views](#multivariate--matrix-views)
14. [Plot Customization & Annotation](#plot-customization--annotation)
15. [Saving Figures](#saving-figures)
16. [Practice Activities](#practice-activities)
17. [Further Reading & Design Checklist](#further-reading--design-checklist)

## 🎯 Learning Objectives

By the end of this presentation, participants will be able to:

- **Ethically acquire data** from various sources including web scraping, APIs, and public datasets
- **Apply responsible web scraping practices** with proper rate limiting and respect for website policies
- **Perform automated exploratory data analysis** using pandas profiling tools
- **Create effective statistical visualizations** using Seaborn's declarative API
- **Design accessible and interpretable plots** following data visualization best practices
- **Customize and export publication-ready figures**

## 🛠️ Prerequisites

### Required Knowledge
- Basic Python programming
- Familiarity with pandas DataFrames
- Understanding of fundamental statistical concepts

### Required Software
- Python 3.7+
- Jupyter Notebook or JupyterLab
- Internet connection (for web scraping demo)

## 📦 Installation

### 1. Clone the Repository
```bash
git clone https://github.com/comsavvy/Data-Acquisition-and-Statistical-Data-Viz-with-Seaborn-Presentation.git
cd Data-Acquisition-and-Statistical-Data-Viz-with-Seaborn-Presentation
```

### 2. Install Required Packages
```bash
# Core packages for data analysis and visualization
pip install pandas numpy matplotlib seaborn

# Web scraping packages
pip install requests beautifulsoup4

# Optional: Automated profiling (restart kernel after installation)
pip install ydata-profiling[notebook]

# Optional: Enhanced parsing
pip install lxml
```

### 3. Launch Jupyter Notebook
```bash
jupyter notebook olusola_ogundepo_PP_presentation.ipynb
```

## 📁 Dataset Information

### Included Datasets

#### 1. Tips Dataset (`datasets/tips.csv`)
Restaurant tipping behavior data from Nairobi, Kenya:
- **total_bill**: Total meal cost in Kenyan Shillings (KES)
- **tip**: Gratuity amount in KES
- **gender**: Gender of the bill payer
- **smoker**: Whether anyone in the party smoked
- **day**: Day of the week
- **time**: Lunch or dinner service
- **size**: Number of people in the dining party

#### 2. Penguins Dataset (`datasets/penguins.csv`)
Palmer Archipelago penguin morphology data:
- **species**: Adelie, Chinstrap, or Gentoo
- **bill_length_mm/bill_depth_mm**: Bill dimensions
- **flipper_length_mm**: Flipper length
- **body_mass_g**: Body mass
- **sex**: Male or female
- **island**: Biscoe, Dream, or Torgersen

#### 3. Africa COVID-19 Dataset (`datasets/Africa COVID-19 Dec 6, 2020.csv`)
COVID-19 statistics across African regions as of December 6, 2020:
- Regional case counts and trends
- Useful for practicing bar plots and data ordering

## 🕷️ Web Scraping Demo

The notebook includes a responsible web scraping demonstration using the **Books to Scrape** website:

### Key Features:
- **Ethical practices**: Polite delays, proper User-Agent headers
- **Error handling**: Robust request management with timeouts
- **Data extraction**: Title, price, rating, and stock status
- **Data cleaning**: Converting ratings to numeric values

## 📊 Visualization Techniques Covered

### Univariate Analysis
- **Histograms**: Frequency distributions with customizable bins
- **Kernel Density Estimates (KDE)**: Smoothed distribution curves
- **Box plots**: Summary statistics and outlier detection
- **Violin plots**: Distribution shape with density information

### Bivariate Analysis
- **Scatter plots**: Relationship between continuous variables
- **Regression plots**: Linear trends with confidence intervals
- **Joint plots**: Combined bivariate and marginal distributions
- **Correlation heatmaps**: Matrix visualization of relationships

### Categorical Analysis
- **Count plots**: Category frequencies
- **Bar plots**: Group means with confidence intervals
- **Grouped visualizations**: Multi-category comparisons using `hue`
- **Pie charts**: Proportional representations (used sparingly)

### Multivariate Analysis
- **Pair plots**: All pairwise relationships
- **Faceted plots**: Multiple subplots for group comparisons
- **Matrix visualizations**: Correlation and covariance structures

## 🎨 Design Principles

### Visual Design Guidelines
- **Clarity over complexity**: Each plot answers a specific question
- **Accessibility**: Colorblind-friendly palettes
- **Meaningful ordering**: Logical sequence instead of alphabetical
- **Appropriate encoding**: Right visualization for the data type
- **Clean annotation**: Clear axes labels, titles, and units

### Code Quality Standards
- **Reproducible workflows**: Clear, commented code
- **Modular functions**: Reusable components for data processing
- **Error handling**: Robust data acquisition and processing
- **Documentation**: Comprehensive explanations and rationale

## 🏃‍♂️ Quick Start

1. **Open the notebook**: `olusola_ogundepo_PP_presentation.ipynb`
2. **Run the setup cells**: Import libraries and set styling
3. **Follow along sequentially**: Each section builds on previous concepts
4. **Try the practice activities**: Hands-on exercises with provided datasets
5. **Experiment**: Modify parameters and explore different visualizations

## 🔬 Practice Activities

### Activity 1: Africa COVID-19 Analysis
- Load and explore the COVID-19 dataset
- Create horizontal bar plots for readability
- Practice data ordering and interpretation
- **Skills**: Bar plots, data ordering, basic interpretation

### Activity 2: Penguins Basics
- Explore penguin morphology data
- Create univariate distributions
- Practice summary statistics
- **Skills**: Descriptive statistics, box plots, histograms

### Activity 3: Penguins Advanced
- Multi-variable comparisons
- Grouped visualizations with species and sex
- Correlation analysis
- **Skills**: Grouped plots, scatter plots, pairwise analysis

## 📚 Key Seaborn Concepts

### Figure-Level vs Axes-Level Functions
- **Figure-level**: `relplot()`, `displot()`, `catplot()` - return FacetGrid
- **Axes-level**: `scatterplot()`, `histplot()`, `boxplot()` - work with matplotlib axes

### Semantic Mappings
- **x, y**: Position mappings
- **hue**: Color encoding for categories
- **size**: Point size for continuous variables
- **style**: Marker style for categories

### Plot Customization
- **Styling**: `sns.set_style()`, `sns.set_context()`
- **Color palettes**: Built-in and custom color schemes
- **Annotations**: Titles, labels, and interpretive text
- **Export**: High-resolution figure saving

## 🌍 Ethical Considerations

### Web Scraping Ethics
- **Respect robots.txt**: Check website scraping policies
- **Rate limiting**: Implement delays between requests
- **Server load**: Avoid overwhelming target servers
- **Legal compliance**: Understand terms of service and copyright

### Data Usage Ethics
- **Attribution**: Credit data sources appropriately
- **Privacy**: Respect individual privacy in datasets
- **Bias awareness**: Acknowledge limitations and potential biases
- **Transparency**: Document data acquisition and processing methods

## 🔗 Additional Resources

### Documentation & Tutorials
- [Seaborn Official Documentation](https://seaborn.pydata.org/)
- [Matplotlib Gallery](https://matplotlib.org/stable/gallery/)
- [Pandas User Guide](https://pandas.pydata.org/docs/user_guide/)

### Books & References
- "Fundamentals of Data Visualization" by Claus O. Wilke
- "Python for Data Analysis" by Wes McKinney
- "The Grammar of Graphics" by Leland Wilkinson

### Tools & Resources
- [ColorBrewer](https://colorbrewer2.org/) - Color palette selection
- [Data Visualization Catalogue](https://datavizcatalogue.com/) - Chart type reference
- [Python Graph Gallery](https://python-graph-gallery.com/) - Code examples

## 📈 Design Checklist

Before finalizing any visualization, ask:

- **Purpose**: What question does this plot answer?
- **Appropriateness**: Is the chosen mark (point, bar, area) suitable?
- **Clarity**: Are scales clear (units, transformations)?
- **Accessibility**: Are colors distinguishable and colorblind-safe?
- **Order**: Is ordering meaningful rather than arbitrary?
- **Uncertainty**: Is variability represented when relevant?
- **Annotation**: Are key takeaways highlighted appropriately?
- **Simplicity**: Can any elements be removed without losing information?

> **Remember**: Good visualization = maximum insight, minimum noise.

## 🤝 Contributing

Contributions are welcome! Please feel free to:
- Report bugs or issues
- Suggest improvements to code or explanations
- Add new examples or datasets
- Improve documentation

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 📧 Contact

**Olusola Timothy Ogundepo**  
African Institute of Mathematical Sciences, Rwanda  
GitHub: [@comsavvy](https://github.com/comsavvy)

---

*This presentation was developed for educational purposes to demonstrate best practices in data acquisition and statistical visualization using Python.*