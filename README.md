# Youtube thumbnail A/B Testing

## Project Overview

This project demonstrates A/B testing for YouTube video thumbnails to determine which version performs better in terms of Click-Through Rate (CTR).
Two thumbnails (A and B) were compared, and metrics such as CTR, impressions, and cumulative CTR trends were analyzed to reach a conclusion.

## Dataset

Synthetic dataset created to simulate YouTube analytics data for two thumbnails.
Columns include:
- impressions → Number of times the thumbnail was shown
- clicks → Number of times users clicked the thumbnail
- group → Thumbnail version (A or B)

## Methodology

1. Define the Metric:
- Primary metric = Click-Through Rate (CTR) = clicks / impressions.

2. Data Simulation:
- Created random impression and click data for thumbnails A and B.
- Ensured B had slightly higher CTR to test significance.

3. Statistical Testing: To validate whether the difference in click-through rates (CTR) between Thumbnail A and Thumbnail B is statistically significant, we applied multiple testing methods:
    
   1. Two-Proportion Z-Test
      - Used to compare the proportion of clicks (CTR) between the two groups.
      - Null Hypothesis (H₀): CTR_A = CTR_B
      - Alternative Hypothesis (H₁): CTR_A ≠ CTR_B
      - If the p-value < 0.05 → reject H₀, meaning the difference is statistically significant.

   2. 95% Confidence Interval for CTR Difference
      - Constructed a confidence interval around the difference in CTRs.
      - If the interval does not include 0, it supports the conclusion that one thumbnail performs better.

   3. Bootstrap Method
      - Resampled the data thousands of times to estimate the distribution of CTR differences.
      - Provides a non-parametric check, ensuring the result is robust without strong statistical assumptions.
 
4. Visualization:
- CTR comparison bar chart
- Cumulative CTR over impressions plot

## Conclusion
- Thumbnail B achieved a higher and more stable CTR than Thumbnail A.
- The difference was confirmed using a z-test, with p-value < 0.05, indicating statistical significance.
- Decision: Use Thumbnail B for better engagement.
