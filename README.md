DRMD-CLASS
==============================================
based on CLASS by Julien Lesgourgues, Thomas Tram, and Nils Schoeneberg; see http://class-code.net and https://github.com/lesgourg/class_public

DRMD stands for "Dark Radiation Matter Decoupling". The model is a simple phenomenological extension of LCDM based on an interaction between dark matter and dark radiation. The dark radiation component features strong self-interactions (SIDR) and is thus implemented as a fluid with vanishing shear. The interaction between both sectors turns off exponentially at some critical redshift. The DRMD component is designed to run alongside all other standard CLASS components (NCDM, iDR, ETHOS, idm, etc.). The crucial modifications of the code come with the tag "_drmd".

The model comes with four paramters which are explained in the DRMD.ini file. A concrete mirophysical implementation is provided by Hot New Early Dark Energy.      

