DRMD-CLASS
==============================================
based on CLASS (v3.2.5) by Julien Lesgourgues, Thomas Tram, and Nils Schoeneberg; see http://class-code.net and https://github.com/lesgourg/class_public


DRMD-CLASS implements the DRMD model, which arises from the Hot New Early Dark Energy (Hot NEDE) model in a particular limit and has been proposed in arXiv: xxx.xxx 

DRMD stands for "Dark Radiation Matter Decoupling". The model is a simple 3-parameter extension of LCDM based on an interaction between a fraction of dark matter (param1: f_idm_drmd) and dark radiation (param2: delta_Neff_drmd). The dark radiation component features strong self-interactions (SIDR) and is thus implemented as a fluid with vanishing shear. Initially dark matter and dark radiation are tightly coupled, but eventually the interaction rate between both sectors becomes exponentially suppressed at some critical redshift (param3: z_stop) before decoupling occurs later at redshift z_dec_drmd (derived). A concrete mirophysical realization is provided by Hot NEDE.    


The DRMD component is designed to run alongside all other standard CLASS components (NCDM, iDR, ETHOS, idm, etc.). The crucial modifications of the code come with the tag "_drmd".

The model parameters are explained in the DRMD.ini file.   

For performing an MCMC analysis with Montepython, some example xxx.param file can be found in the folder montepython_tree alongside a covariance matrix. 

Further details on installing the code and running CLASS can be found on the original CLASS github page. 

