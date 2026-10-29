# Experiment series — Experiment Summary

## Research question
Can strong observational predictive accuracy coexist with unreliable estimates of intervention effects?

## Identification caveat
S3 and S4 with nonzero measurement error are not identified from the observed covariates under the specified adjustment assumptions.

## Main results (observed numerical outputs)
              config       model  test_rmse  ate_hat  true_ate  ate_abs_error
      S0_baseline__A    additive     1.2510   2.0874    2.0000         0.0874
      S0_baseline__A interaction     1.0144   2.0580    2.0000         0.0580
      S0_baseline__A   nonlinear     1.0148   2.0152    2.0000         0.0152
      S0_baseline__A  speed_only     1.7177   2.8187    2.0000         0.8187
     S1_nonlinear__A    additive     1.7050   2.2681    2.8049         0.5367
     S1_nonlinear__A interaction     1.0992   2.2812    2.8049         0.5237
     S1_nonlinear__A   nonlinear     0.9739   2.7948    2.8049         0.0101
     S1_nonlinear__A  speed_only     2.0856   2.9927    2.8049         0.1878
         S2_shift__A    additive     1.2674   2.0057    2.0000         0.0057
         S2_shift__A interaction     0.9990   2.0009    2.0000         0.0009
         S2_shift__A   nonlinear     1.0003   2.0497    2.0000         0.0497
         S2_shift__A  speed_only     1.7193   2.7567    2.0000         0.7567
         S2_shift__B    additive     1.2817   2.9963    3.0000         0.0037
         S2_shift__B interaction     1.0197   2.9792    3.0000         0.0208
         S2_shift__B   nonlinear     1.0195   2.9435    3.0000         0.0565
         S2_shift__B  speed_only     2.2208   4.0892    3.0000         1.0892
         S2_shift__C    additive     2.7443   2.0297    2.0000         0.0297
         S2_shift__C interaction     1.0035   2.0299    2.0000         0.0299
         S2_shift__C   nonlinear     1.0034   2.0362    2.0000         0.0362
         S2_shift__C  speed_only     3.0904   3.4743    2.0000         1.4743
        S3_hidden__A  speed_only     1.7191   2.7250    2.0000         0.7250
     S4_proxy__A__w0    additive     1.2815   2.0147    2.0000         0.0147
     S4_proxy__A__w0 interaction     1.0168   2.0160    2.0000         0.0160
     S4_proxy__A__w0   nonlinear     1.0168   2.0207    2.0000         0.0207
     S4_proxy__A__w0  speed_only     1.7381   2.7521    2.0000         0.7521
   S4_proxy__A__w0.5    additive     1.4340   2.1987    2.0000         0.1987
   S4_proxy__A__w0.5 interaction     1.2189   2.2037    2.0000         0.2037
   S4_proxy__A__w0.5   nonlinear     1.2148   2.2448    2.0000         0.2448
   S4_proxy__A__w0.5  speed_only     1.7414   2.6726    2.0000         0.6726
   S4_proxy__A__w1.5    additive     1.5646   2.5503    2.0000         0.5503
   S4_proxy__A__w1.5 interaction     1.5296   2.5448    2.0000         0.5448
   S4_proxy__A__w1.5   nonlinear     1.4792   2.7492    2.0000         0.7492
   S4_proxy__A__w1.5  speed_only     1.6616   2.7168    2.0000         0.7168
S5_overlap__A__x0.05    additive     1.1340   1.3648    2.0000         0.6352
S5_overlap__A__x0.05 interaction     0.9910   1.3447    2.0000         0.6553
S5_overlap__A__x0.05   nonlinear     0.9914   1.1046    2.0000         0.8954
S5_overlap__A__x0.05  speed_only     1.1357   3.7622    2.0000         1.7622
 S5_overlap__A__x0.3    additive     1.1368   2.0170    2.0000         0.0170
 S5_overlap__A__x0.3 interaction     0.9988   1.9205    2.0000         0.0795
 S5_overlap__A__x0.3   nonlinear     0.9999   1.9854    2.0000         0.0146
 S5_overlap__A__x0.3  speed_only     1.2715   3.6976    2.0000         1.6976
   S5_overlap__A__x1    additive     1.2463   1.9807    2.0000         0.0193
   S5_overlap__A__x1 interaction     1.0081   1.9979    2.0000         0.0021
   S5_overlap__A__x1   nonlinear     1.0094   1.9682    2.0000         0.0318
   S5_overlap__A__x1  speed_only     1.7243   2.7091    2.0000         0.7091

## Cross-environment results
      model train_env test_env  true_ate  ate_hat  ate_abs_error  predictive_rmse
 speed_only         A        A       2.0   2.7567         0.7567           1.7193
 speed_only         A        B       3.0   2.7567         0.2433           4.3887
 speed_only         A        C       2.0   2.7567         0.7567           3.3884
interaction         A        A       2.0   2.0009         0.0009           0.9990
interaction         A        B       3.0   2.9877         0.0123           1.0202
interaction         A        C       2.0   1.9912         0.0088           1.0002

## Interpretation
These are computational results for a synthetic benchmark, not validation of causal identification in real data. Assess each estimator's assumptions before interpreting a plug-in contrast causally.