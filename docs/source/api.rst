====================
Python API Reference
====================

.. contents:: Table of Contents
    :local:
    :depth: 2


Reading raw data
================

Raw file reader
---------------

Uniform API to read multiple actigraphy data formats.
Currently, the supported formats are:

* wGT3X-BT, Actigraph (.agd file format only);
* Actiwatch 4 and MotionWatch 8, CamNtech (.awd and .mtn);
* ActTrust 2, Condor Instruments (.txt);
* Daqtometer, Daqtix (.csv);
* Actiwatch 2 and Actiwatch Spectrum Plus, Philips Respironics (.csv)

Associated functions:

.. currentmodule:: pyActigraphy.io

.. autosummary::
   :toctree: _autosummary/
   :template: function.rst

   read_raw_agd
   read_raw_atr
   read_raw_awd
   read_raw_dqt
   read_raw_mtn
   read_raw_rpx

These functions return a `BaseRaw` object. which is the main class in
pyActigraphy: :class:`pyActigraphy.io.BaseRaw`

Batch reader
------------

Reading actigraphy files by batch:

.. currentmodule:: pyActigraphy.io

.. autosummary::
   :toctree: _autosummary/
   :template: function.rst

   read_raw

This function return a `RawReader` object: :class:`pyActigraphy.io.RawReader`

Spurious activity masking
=========================

* Masking: :mod:`pyActigraphy.filters.FiltersMixin`


Log files
=========

* Base log: :mod:`pyActigraphy.log.BaseLog`

* Start/Stop time log: :mod:`pyActigraphy.log.SSTLog`


Rest-Activity Rhythms
=====================

* Non-parametric and transition probability methods: :mod:`pyActigraphy.metrics.MetricsMixin`


Rest-activity scoring and sleep diary
=====================================

* Rest-activity scoring: :mod:`pyActigraphy.sleep.ScoringMixin`

* Sleep diary: :mod:`pyActigraphy.sleep.SleepDiary`

* Sleep bout identification: :mod:`pyActigraphy.sleep.SleepBoutMixin`


Analysis
========

* Cosinor analysis: :mod:`pyActigraphy.analysis.Cosinor`

* Functional linear modeling: :mod:`pyActigraphy.analysis.FLM`

* Fractality analysis: :mod:`pyActigraphy.analysis.Fractal`

* Locomotor inactivity during sleep (LIDS): :mod:`pyActigraphy.analysis.LIDS`

* Singular spectrum analysis : :mod:`pyActigraphy.analysis.SSA`
