.. currentmodule:: nilearn

.. include:: names.rst

0.10.2.dev
==========

NEW
---

Fixes
-----

- Fix bug that would prevent loading the confounds of a gifti file in actual fmriprep datasets (:gh:`3819` by `Rémi Gau`_).

- Fix bug in :func:`~glm.first_level.first_level_from_bids` that returned no confound files if the corresponding bold files contained derivatives BIDS entities (:gh:`3742` by `Rémi Gau`_).

- Fix bug in :func:`~glm.first_level.first_level_from_bids` that would throw a warning about ``slice_time_ref`` not being provided even when it was (:gh:`3811` by `Rémi Gau`_).

- :bdg-dark:`Code` Fix bug where the `cv_params_` attribute of fitter Decoder objects sometimes had missing entries if `grid_param` is a sequence of dicts with different keys (:gh:`3733` by `Michelle Wang`_).

- Make the :func:`~nilearn.interfaces.fmriprep.load_confounds` confounds file selection more generic (:gh:`3794` by `Taylor Salo`_).

- Change default figsizes to prevent titles from overlapping figure content (:gh:`3797` by `Yasmin Mzayek`_ and see also :gh:`2804` by `Oliver Warrington`_)

- Relax the :func:`~nilearn.interfaces.fmriprep.load_confounds` confounds selection on `cosine` as not all confound files contained the variables (:gh:`3816` by `Hao-Ting Wang`_).

Enhancements
------------

- Update Decoder objects to use the more efficient ``LogisticRegressionCV`` (:gh:`3736` by `Michelle Wang`_).

- Make return key names in the description file of destrieux surface consistent with :func:`~datasets.fetch_atlas_surf_destrieux` (:gh:`3774` by `Tarun Samanta`_).

Changes
-------

- Removed old files and test code from deprecated datasets COBRE and NYU resting state (:gh:`3743` by `Michelle Wang`_).
- :bdg-secondary:`Maint` PEP8 and isort compliance extended to the whole nilearn codebase. (:gh:`3538`, :gh:`3566`, :gh:`3548`, :gh:`3556`, :gh:`3601`, :gh:`3609`, :gh:`3646`, :gh:`3650`, :gh:`3647`, :gh:`3640`, :gh:`3615`, :gh:`3614`, :gh:`3648`,  :gh:`#3651`  by `Rémi Gau`_).
- :bdg-secondary:`Maint` Finish applying black formatting to most of the codebase. (:gh:`3836`, :gh:`3833`, :gh:`3827`, :gh:`3810`, :gh:`3803`, :gh:`3802`, :gh:`3795`, :gh:`3790`, :gh:`3783`, :gh:`3777` by `Rémi Gau`_).
- :bdg-danger:`Deprecation` Empty region signals resulting from applying `mask_img` in :class:`~maskers.NiftiLabelsMasker` will no longer be kept in release 0.15. Meanwhile, use `keep_masked_labels` parameter when initializing the :class:`~maskers.NiftiLabelsMasker` object to enable/disable this behavior. (:gh:`3722` by `Mohammad Torabi`_).
- :bdg-danger:`Deprecation` Empty region signals resulting from applying `mask_img` in :class:`~maskers.NiftiMapsMasker` will no longer be kept in release 0.15. Meanwhile, use `keep_masked_maps` parameter when initializing the :class:`~maskers.NiftiMapsMasker` object to enable/disable this behavior. (:gh:`3732` by `Mohammad Torabi`_).
- Removed mention of license in "header" (:gh:`3838` by `Czarina Sy`_).
- Configure plots in example gallery for better rendering  (:gh:`3753` by `Yasmin Mzayek`_)
