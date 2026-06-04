DRMD-CLASS
==========

DRMD-CLASS is a modified version of CLASS implementing the Dark Radiation–Matter Decoupling
(DRMD) model. It is based on CLASS v3.2.5 by Julien Lesgourgues, Thomas Tram,
and Nils Schöneberg; see http://class-code.net and
https://github.com/lesgourg/class_public.

The DRMD model was proposed in arXiv:2508.03795 and arises as a particular limit
of the Hot New Early Dark Energy (Hot NEDE) model.

Version history
---------------

- **DRMD_v1**: Initial release in connection with arXiv:2508.03795; based on CLASS v3.2.5.
- **DRMD_v2**: Rebased to CLASS v3.3.4; added the running-of-running parameter
  `beta_s`; included the dark sound horizon `rs_d_drmd` as a derived parameter.
  This version was used for arXiv:2602.23895 and arXiv:2604.26541.

Model description
-----------------

DRMD stands for **Dark Radiation–Matter Decoupling**. The model is an extension 
of ΛCDM based on an interaction between a fraction of dark matter and a dark 
radiation component.

The dark radiation component features strong self-interactions and is implemented
as a self-interacting dark radiation fluid with vanishing shear. Initially, the
interacting dark matter and dark radiation sectors are tightly coupled. At the
critical redshift `z_stop`, the interaction rate becomes exponentially suppressed,
and the two sectors subsequently decouple at the derived redshift `z_dec_drmd`.

A concrete microphysical realization of this scenario is provided by Hot NEDE.

Code structure
--------------

The main DRMD parameters are:

- `delta_Neff_drmd`: the contribution of the dark radiation component to
    the effective number of relativistic species;
- `f_idm_drmd`: the fraction of dark matter interacting with dark radiation;
    if set to 0, the model reduced to SIDR (produced after BBN);
- `z_stop`: the critical redshift at which the interaction rate starts to become
    exponentially suppressed;
- `G_over_aH_drmd_ini`: Initial interaction rate divided by H. This ratio is 
    constant during rad. domination. Values >> 1 correspond to initial tight coupling. 
    Data has almost no sensitivity to this parameter (see first paper on DRMD) and it 
    can be set to some fiducial value (recommendation: 1e7).

The DRMD component is designed to run alongside the standard CLASS components,
including NCDM, iDR, ETHOS, idm, and others. The main code modifications are
marked with the tag `_drmd`.

The model parameters are documented in the example input file:

```text
DRMD.ini
```

Cobaya examples
---------------

Example Cobaya configuration files are provided in the `cobaya/` folder, together
with covariance matrices, for SIDR with `f_idm_drmd = 0` and for the full DRMD
model. These examples include cases with general running `alpha_s` and
running-of-running `beta_s`.

Installation and usage
----------------------

DRMD-CLASS is compiled and run in the same way as the original CLASS code.
For general installation instructions, see the original CLASS documentation and
GitHub repository:

- http://class-code.net
- https://github.com/lesgourg/class_public

To get started with the DRMD model, inspect and run the example input file:

```bash
./class DRMD.ini
```

Citation
--------

If you use DRMD-CLASS, please cite the relevant DRMD paper:

- arXiv:2508.03795

Please also cite the original CLASS papers and repository.


