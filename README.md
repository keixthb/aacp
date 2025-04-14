
# AACP:

This github repository contains the necessary [HFSS](https://www.ansys.com/products/electronics/ansys-hfss) designs for the Lüneberg lens numerical calculations. It is provided as accompaniment to the master's thesis, ["aacp.pdf"](https://github.com/keixthb/aacp/blob/main/aacp.pdf). The thesis depends on [PyEms](https://github.com/matthuszagh/pyems), [NaluCFD](https://github.com/NaluCFD/Nalu) and [Kokkos Kernels](https://github.com/kokkos/kokkos-kernels), among many other open source libraries. 

## Instructions:


- Load the file  ["lens\_with\_plate\_old.aedt"](https://github.com/keixthb/aacp/blob/main/HFSSFiles/lens_with_plate_old.aedt) with Ansys HFSS

- Select the ``HPC Options`` tab and configure so it is set to run all frequency iterations in a single core. This should look similar to the following:

<img src="assets/HPC_Options.png" alt="Alt text" title="HPC_Options.png">

- Click the ``Analyze All`` button. Using a stopwatch or timer, measure the time it takes to compute all 9 frequency steps from start to finish. 


- Validate that the directivity at 2.4GHz is 39.63 dB and has a consistent radiation pattern with the results below:


<img src="assets/directivity.png" alt="Alt text" title="directivity.png">

## Results:

You can compare your performance with a few different processors:

<img src="assets/benchmark.png" alt="Alt text" title="benchmark.png">
