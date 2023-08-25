---
title: "Ph Probe Calibration"
date: 2023-08-23T11:55:51Z
description: 'Good calibration of a ph probe could be tricky.'
image: images/elektroda.jpg
draft: false
---
Let's start the blog with a little bit of history🦄.

[SPL Sørensen](https://es.m.wikipedia.org/wiki/S._P._L._S%C3%B8rensen) was a danish chemical known for the invention of the **potential hidrogen scale** or **pH scale** back to 1909. This scale allow anyone to measure the _acidity_ or _alkalinity_ of a solution. This idea is based on the concentration that hidrogen ions \\( H^+ \\) and hidroxide ions \\( OH- \\) regulate the possible interchange of energy between molecules in the solution. With that in mind, Sørensen arrange a equation that permit us to work with complete numbers.

![pH scale](images/ph-scale.webp)

Establish the \\( pH \\) of distiled water as 7, the center of the scale and the neutral point. All above 7 is alkaline and all under seven is acid, with a range between 0 and 14.

Some methods of measurement like the use by the cheaper pH probe sensor was invented by Sørensen too. 

The method of electrodes was invented by him.

## Sensor

The ph sensor probe is built with two electrodes that react with the hidrogens ions. A pH meter and its electrodes require calibrating to produce accurate pH readings.

The glass pH sensing or measuring electrode responds in a linear fashion to the hydrogen ion activity according to the Nernst equation as a very close approximation.

![sensor](images/pH-probe-cross-section-blog-img.webp)

The Nernts equation can be simplified to:

$$
E = E_o + SLOPE * T * pH
$$

Where \\( E \\) is the total electrical potential difference in millivolts (mV), \\(E_o\\) is the electrical potential STD produced by the reference electrode (mV) which is constant, SLOPE, incorporates all the constants of the Nernst equation, \\( T \\)  is the temperature in degrees Kelvin (Ko) and \\( pH \\) is the hydrogen ion activity.


### Temperature considerations

It can be seen from the above equation that the sensing electrode's response to hydrogen ion activity (pH) is temperature dependent and needs to be allowed for.

For this reason pH meters are either:

- fitted with a temperature adjustment control to manually set the pH meter to the temperature of solutions being measured

or

- fitted with a temperature probe (either as a separate entity or incorporated into the electrode arrangement) for automatic adjustments of temperatures involved.


pH buffer and sample solutions' true pH

When using standard pH buffers to calibrate your pH meter, the true pH of the buffer is temperature dependant and needs to be read of a chart or graph for that particular buffer's temperature.

> This is particularly relevant when pH buffers are stored in refrigerators.

Similarly, sample pH measurements are also dependant on temperature, and should be recorded along side the temperature it was measured at.

>  NOTE: the pH meter temperature adjustment caters for the electrode's response to temperature, which is not to be confused with the temperature dependants of true pH values of solutions.

Some automated pH meters accomplish these measurements and calculations automatically. However, you need to ensure yourself that this is the case.

### Reference Electrode

The electrode potential of the reference electrode is dependant on the condition of the porous plug.

Contamination of this porous plug will alter the reference potential as well as slow down the electrode response.

## Standard Hydrogen Electron
The standard hydrogen electron or [SHE](https://en.m.wikipedia.org/wiki/Standard_hydrogen_electrode)
is a mathematical model that simplified the Nersnt equation to normal laboratory condition.

$$
E=-0.0591 pH (volt)
$$

### Calibration

The electric potential of the special glass bulb of the pH electrode also varies through contamination, dehydration surface, abrasions and aging aspects of this glass bulb.

For the above reasons the pH electrode system needs to be calibrated.


1, 2 or 3 point calibrations

#### One point calibration.

As mentioned above, the pH measuring electrode responds in a linear fashion within the normal range of pH values expected close to that predicted by the Nernst equation.

The slope of this curve (line) is calculated to equate to 59mv (millivolts) per pH unit change.

To make sure that this is the case the pH meter may need to be adjusted via the pH 4.00, slope or sensitivity control.

If the pH meter has recently had a 3, or 2 point calibration all that may be required is a one point calibration using a pH buffer close to the expected value of your sample solution to adjust the slope.

A pH 3 or 4 buffer can be chosen for wine production pH measurements.

A two (2) point calibration is normally recommended for each session


#### Two point calibration.

Point one (1)

At a true pH of 7.00 no electrical potential should exist across the pH electrode and read 0.00 millivolts .

The pH meter may have to be adjusted so that this is the case.

This adjustment should be the first calibration point as it will vary least when adjusting the slope with your second calibration point.

A pH buffer close to pH 7.00 is used and the pH readout adjusted to read the true buffer pH.

The adjustment can occur automatically or via the pH 7.00, zero, offset, gain, intercept or buffer adjustment control.

The above adjustment control names or labels have their own logic depending on whether you are talking about the pH, voltage, graph, electronics or buffer aspects of the adjustments.

Point two (2)

To set the slope, as discussed in the 1 point calibration above, use a pH buffer that ensure that the pH range expected is covered.

A pH 4 buffer is usually chosen the buffer chosen to cover the expected pH throughout wine production.

A 2 point calibration is normally recommended for each session


#### Three point calibration.

The third calibration of a three point calibration serves basically as a check that the pH meter has been zeroed correctly and the slope conforms to 57 mv per pH unit.

A pH buffer close to the expected sample pH is usually chosen as the third point.

## Nerst equation
The basic Nernst Equation is written as:

$$
E = E_o - \frac{RT}{nF} lnQ 
$$

and expresses the electrical potential of a electrochemical cell at non-standard state conditions and at any time during the electrochemical cell's reaction.

The Nernst equation is derived from thermodynamic considerations.
The reactants' free energies are expressed as electrical potentials.
The term $E_o$ is the standard electric potential of the reference electrode
The term $lnQ$ represents the natural logarithm (ln) of the reaction quotient (Q) of the species involved. $lnQ$ can be expressed as a logarithm to the base 10 by -2.303 log10Q.
and log10Q, for pH measurements, can be expresses in terms of the hydrogen ion activity by -log10aH+ which is the pH of a solution.

Hence the equation becomes:

$$
E = E_o - \frac{RT}{nF} * 2.303 pH 
$$

The constants of the Nernst equation -

R is the universal gas constant -

R = 8.3145 J/mol.K (Joule per mol and per Kelvin)


n is the number of moles of electrons transferred in the balanced equation or the charge/valency of the ion. Which in the case of the hydrogen ion -

n = 1


$F$ is the Faraday constant which is the electrical charge in coulombs (C) for every mole (mol) of reactant involved in the electrochemical cell $F = 96485.309 C/mol$


At a temperature (T) of 298.15 oK (25o C) the Nernst equation can be rewritten as -


8.3145 J/mol.K * 298.15 K

$$
E = E_o + \frac{8.3145 J/mol.K * 298.15 K}{96485.309 C/mol} * 2.303 pH 
$$

Become:

$$
E = E_o + 0.059 V pH (1 J/C = 1 Volt (V))
$$

That is a change of 56 mV per pH unit.