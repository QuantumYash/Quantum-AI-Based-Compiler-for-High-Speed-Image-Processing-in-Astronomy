# Quantum AI-Based Compiler for Astronomical Image Processing
Overview

This repository contains the implementation of a Quantum AI-Based Compiler designed to optimize high-speed image processing for astronomical data. The project leverages a hybrid approach combining Quantum-Inspired Evolutionary Algorithm (QIEA) and Particle Swarm Optimization (PSO) to enhance telescope images, such as those from the Hubble Space Telescope (HST). The initial focus is on noise reduction, with plans to expand to other tasks like object detection and image enhancement.

Problem Statement

Modern astronomical telescopes, such as the Hubble Space Telescope and upcoming instruments like the Vera C. Rubin Observatory, generate vast amounts of image data (terabytes per night). Traditional image-processing methods struggle to keep up with this data deluge, delaying scientific discoveries due to slow processing times. Tasks like noise reduction, object detection, and feature enhancement are computationally intensive, especially when handling raw FITS files with high dynamic ranges and noise from cosmic rays or detectors. This project aims to address this bottleneck by developing a compiler that:

Optimizes image-processing parameters using quantum-inspired AI.
Accelerates processing to enable near-real-time analysis.
Matches or exceeds the quality of existing pipelines (e.g., Hubble’s drizzling process).
Objective
Build a compiler that uses QIEA and PSO to process raw astronomical images (e.g., FITS files) faster and with high accuracy, using processed science images as benchmarks. The initial goal is to reduce noise in raw Hubble images by at least 50% in under 5 seconds per image, with potential for broader applications.

Data Source

The project uses FITS files from the Hubble Legacy Archive (HLA), a public repository of processed and raw Hubble Space Telescope data hosted by the Space Telescope Science Institute (STScI).

Website: https://hla.stsci.edu/
Sample File Used: hst_mos_0017053_acs_wfc_f555w_sci
A processed science image (mosaic) from the Advanced Camera for Surveys (ACS), Wide Field Channel (WFC), in the F555W filter (visible light).
Used as a benchmark for processed output.
Raw Data (To Be Added): Corresponding raw files (e.g., _raw.fits) will be fetched from HLA to serve as input for optimization.
How to Access:
Visit https://hla.stsci.edu/.
Search for a target (e.g., “M51” for the Whirlpool Galaxy).
Filter by instrument (e.g., ACS), filter (e.g., F555W), and download _raw.fits and _sci/_drz.fits files.
Store in the data/ directory.
Algorithms
The project employs a hybrid optimization approach:

Quantum-Inspired Evolutionary Algorithm (QIEA):
Source: Adapted from rnowotniak/qopt (https://github.com/rnowotniak/qopt).
Purpose: Explores a wide solution space using quantum-inspired principles (e.g., superposition-like population states) to find initial parameter sets for image processing.
Implementation: Python/Cython code from qopt, to be integrated in future phases.
Particle Swarm Optimization (PSO):
Source: pyswarms library.
Purpose: Refines QIEA solutions by simulating a swarm of particles converging on optimal parameters (e.g., filter sigma for noise reduction).
Implementation: Currently used standalone for prototyping.
Hybrid Approach: QIEA will generate initial solutions, which PSO refines, optimizing parameters like filter coefficients for high-speed processing.

Libraries Used

The project relies on the following Python libraries:

astropy: For reading, manipulating, and writing FITS files.
numpy: For numerical operations on image arrays.
matplotlib: For visualizing raw, processed, and benchmark images.
scipy: For image-processing filters (e.g., Gaussian blur).
pyswarms: For PSO implementation.
cython: For potential performance optimization (used in qopt).
