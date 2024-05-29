## Notebooks for all 5 sessions are available here.

### Note: 
If you are following the notebooks, and not running them in real time on a Jupyter Lab engine, please be careful about the unintentional text modfication by GitHub when it parses our notebooks.

For example, the following block:

<img width="692" alt="Screenshot 2024-05-29 at 1 14 41 PM" src="https://github.com/healthdisparities/SISG2024-Module4/assets/14136915/19a5d156-a2a3-4f1b-ac6e-5e583e1b257e">
      
should be

      
    
        ```
        # Appending the 'n' column to our original cohort_raw_prev_df tibble
        cohort_raw_prev_df$n = count_df$n
      
        # Showing the updated tibble
        cohort_raw_prev_df
        ```
