---
title: ScalarQEDAmplitudes
---

# ScalarQEDAmplitudes
A Mathematica code to generate any tree diagram amplitude in the single fermion scalar QED and all possible 1-loop diagrams. After downloading and runnning the code, here some possible commands are listed

 `generategraphs[n]` gives all the graphs with $n$ external points with at most 4 four vertices. Graphs are expressed as lists of legs where positive numbers represent external points and negative numbers internal points. For example `{{1, -1}, {2, -1}, {3, -1}}` is a basic vertex diagram.

 `representgraphs[n]` gives a graphical representation of all the possible graphs with $n$ external points and with at most 4-points vertices.

 `totalamplitude[n,{}]` gives the amplitude of a process with $n$ incoming particles. Both incoming and outcoming particles are listed in the curly brackets. For example `{-1,+1,-1,+1}` gives the Bhabha scattering, while `{-1,+1,0,0}` electron-positron annihilation. The result is given in terms of the least possible number of scalar products of 4-momenta or polarizations, expressed as `SP[p[i],p[j]]` where `p[i]` is the momentum of the $i$-th particle, or with `Epsilon[p[i]]` in case of photons' polarizations. `Mel` is the fermion mass. If the process deos not respect charge conservation the result is plauged of meaningless expressions.

 `squaredamplitude[n,{},amp]` gives the squared amplitude of a process with $n$ incoming particles specified in the curly brackets {}, squaring the corresponding amplitude. Even by applying `FullSimplify`, after more than 5 particles the expressiions are too long.

 `representamplitudes` graphs the amplitudes of the last physical process computed in `totalamplitudes`. Photons are represented by continuos lines while fermions by dash-and-dot lines.

 `wardverify[n,{},amp]` for any of the photons of the given process it tests the Ward identity by susbstituting into the amplitude the photon polarization with its momentum. The identity is sucessfully verified if it gives a list with only 0s, one for any of the photon involved in the process. If the photon is the last particle the result is meaningless since in the amplitudes the last momentum is always replaced by momentum conservation, so the substitution cannot take place.

 `generategraphsloop[n]` gives all the graphs with $n$ external points with at most 4 four vertices and 1 loop. Graphs with tadpoles or corrections to external legs are deleted.

 `representloopgraphs[n]` gives a graphical representation of all the possible graphs with $n$ external points and with at most 4-points vertices and 1 loop. Graphs with tadpoles or corrections to external legs are deleted.


 
