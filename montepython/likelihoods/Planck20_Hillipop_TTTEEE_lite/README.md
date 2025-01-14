# Hillipop is a high-l polarized likelihood for Planck PR4 data (lite, i.e. binned version)

Hillipop is a multifrequency CMB likelihood for Planck data. The likelihood is a spectrum-based Gaussian approximation for cross-correlation spectra from Planck 100, 143 and 217GHz split-frequency maps, with semi-analytic estimates of the Cl covariance matrix based on the data. The cross-spectra are debiased from the effects of the mask and the beam leakage using Xpol (a generalization to polarization of the algorithm presented in Tristram et al. 2005) before being compared to the model, which includes CMB and foreground residuals. They cover the multipoles from &ell; = 30 to 2500.

Reference:\
[Tristram et al., A&A, 2023](https://arxiv.org/abs/2309.10034)

The code is available here:\
[https://github.com/planck-npipe/hillipop](https://github.com/planck-npipe/hillipop)\
This is a wrapper for MontePython.

You need to install the code before:
```
git clone https://github.com/planck-npipe/hillipop --branch v4.3
cd hillipop
pip install .
```

Then get the data, untar and set the variable $COBAYA_PACKAGES_PATH to the local directory:
```
wget https://portal.nersc.gov/cfs/cmb/planck2020/likelihoods/planck_2020_hillipop_TTTEEE_lite_v4.2.tar.gz
tar -zxvf planck_2020_hillipop_TTTEEE_lite_v4.2.tar.gz --directory /path/to/data
export COBAYA_PACKAGES_PATH=/path/to/data
```
