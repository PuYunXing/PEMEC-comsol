# A Pulsed Electromagnetic Eddy Current Method for Detecting Broken Strands of ACSR Conductor in Steel/AL Materials 

***Author: Yunxing Pu, Northeastern University.*** 

***The content of this article has been submitted to the ICCSIE 2023 conference.***

***Readers are welcome to engage in discussions with me. Contact email: yunxing_pu@163.com***

***"mph" is the simulation source file, but due to memory constraints during upload, the simulation results has been stripped . Therefore, you need to perform the simulation on your own pc.***

## Ⅰ. Background

&emsp;&emsp;Transmission lines are a crucial component of the power grid. Currently, the majority of high-voltage transmission lines utilize steel-cored aluminum stranded conductors. However, during their operational lifespan, various types of damage can occur. Detecting these types of damages early on is challenging through overall line monitoring of voltage, current, power, and other signals. Nevertheless, the accumulation of these defects can significantly impact the reliability of the transmission system. Currently, there is limited research focused on this specific area, highlighting the urgent need for the development of efficient and reliable methods for detecting internal and external flaws, enabling periodic non-destructive testing of power transmission lines.
<div align=center>
<img src="FIG/fenzhen.jpg" width="500" height="315"><img src="FIG\leiji.jpg" width="500" height="315" />
</div>
<div align = "center">Fig.1. Wind-induced damage & Lightning strike damage</div>

<div align=center>
<img src="FIG\anzhuang.jpg" width="360" height="210"><img src="FIG\fushi.jpg" width="360" height="210"/>
</div>
<div align = "center">Fig.2. Installation damage & Corrosion damage</div>

## Ⅱ. Principle of PEMEC detection

### Ⅱ.1. Detection target

&emsp;&emsp;This study focuses on the LAG240/30 steel-cored aluminum stranded conductor model, which consists of two outer layers of aluminum and an inner steel core.
<div align=center>
<img src="FIG\jiemian.jpg" width="800" height="250" />
</div>
<div align = "center">Fig.3. Photo of the cross-section and schematic diagram of the LGJ-240/30 cable.</div>

### Ⅱ.2. Sensor design

&emsp;&emsp;We propose that the design of the detection probe mainly consists of three parts: the U-shaped yoke, which provides a magnetic circuit and guides magnetic lines into the transmission line; the excitation coil, wound around the arms of the U-shaped yoke, which generates the original excitation magnetic field when an excitation signal is applied to the circuit; the detection section, which includes differential coils beneath the two magnetic poles, capturing the disturbance signals of the eddy current field. The intermediate balance coil and magnetic sensitive elements collect the signals of the leakage magnetic field in the magnetic circuit and the disturbance signals of the magnetic circuit's eddy current field. From a cross-sectional perspective, a complete set of detection modules can be formed by arranging four uniformly spaced sensors in a circular pattern.
<div align=center>
<img src="FIG\zongtu.jpg" width="900" height="350" />
</div>
<div align = "center">Fig.4.  PEMEC detection mechanism and structure. (a) 3D schematic; (b) Cross-sectional view.</div>

### Ⅱ.3. Detection principle

&emsp;&emsp;Due to the symmetry of the model, the analysis can be limited to one-quarter, considering a two-dimensional equivalent of the model.

#### (1) Leakage magnetic field detection

&emsp;&emsp;When there is a defect in the steel core and it is inclined at an angle to the magnetic lines, the magnetic field undergoes magnetic refraction at the defect interface. As a result, some magnetic flux leaks from the surface, forming a leakage magnetic field.

#### (2) Eddy current distortion detection

&emsp;&emsp;When a damage occurs in the transmission line, it disturbs the distribution of the eddy current field.
<div align=center>
<img src="FIG\FIG.1.jpg" width="600" height="300" />
</div>
<div align = "center">Fig.5. Detection mechanism of the 2-D equivalent model.</div>

&emsp;&emsp;In Figure 6, the detailed detecting processes could be divided into two phases: the pulsed phase and the DC phase.
<div align=center>
<img src="FIG\FIG.2.jpg" width="400" height="300" />
</div>
<div align = "center">Fig.6. Time-domain waveform of pulse-excited voltage</div>

- During the pulsed phase, the pulsed signal generates an alternating magnetic field, which passes through the excitation coil and penetrates the composite material along the U-shaped yoke. Firstly, an eddy current field is established near the contact surface, and then in the magnetic circuit. If the ACSR conductors are damaged, it will result in distortions in the axial eddy current field, which could be detected by the receiving coils. Besides, when the steel is damaged, the magnetic line will be refracted at the defective partition interface. Part of the magnetic flux will leak from the ACSR conductors’ surface to generate a magnetic leakage field.
<div align=center>
<img src="FIG\DCphase.jpg" width="600" height="300" />
</div>
<div align = "center">Fig.7. DC phase</div>

- When the excitation signal transitions to the DC phase, the eddy current field will disappear. At this time, the probe will detect the damage of steel strands alone for magnetic flux leakage. Therefore, in both phases, AL/steel broken strands are presented differently. With the differential coils under the magnetic feet and the balanced coil, all signals could be picked up for damaging classification.

#### (3) PEMEC detection step

&emsp;&emsp;Based on the magnetic field distribution characteristics and coils arrangement, this paper proposes three defect features: balanced signal, differential signal, and AC magnetic flux density. A PEMEC detection step is proposed, as illustrated in Figure 8.
<div align=center>
<img src="FIG\FIG.3.jpg" width="500" />
</div>
<div align = "center">Fig.8. PEMEC detection step</div>

&emsp;&emsp;Due to the different magnetic permeability, electrical conductivity and position of AL/steel strands, the damages show different characteristics in pulsed phase and DC phase. Firstly, the shape of the Bx/By at the observation point provides a direct indication of the damage types. Secondly, the damage position is also located based on the shape of the signal detected by the balanced coil and the differential coil. Finally, the width and depth of the damage is quantified based on these signals. The whole detection process is completed.

## Ⅲ. Analysis of simulation results

### Ⅲ.1. Modelling and Simulation

&emsp;&emsp;This paper uses COMSOL Multiphysics software to build an equivalent 2-D simulation model of the ACSR conductors and the probe, as shown in Figure 9.
<div align=center>
<img src="FIG\FIG.4.jpg" width="500" />
</div>
<div align = "center">Fig.9. 2-D finite element mesh partitioning.(Average mesh quality: 0.9062)</div>

&emsp;&emsp;The ACSR conductors in the model comprise of two layers of 4mm-thick AL strands and one layer of 3mm-thick steel strand, with a total length of 150mm. The U-shaped yoke has dimensions of 92mm in length, 47mm in height, 16mm in width, and a pole spacing of 60mm. The excitation coil has an outer diameter of 22mm, an inner diameter of 14mm, and a height of 40mm. The differential flat coils have an outer diameter of 16mm. The balanced coil has an outer diameter of 10mm, an inner diameter of 2mm, and a height of 2mm. The electromagnetic parameters of the model are listed in Table 1.

<div align=center>
<div align = "center">TABLE  I. Electromagnetic parameters of model</div>

|                    **Parameters**                    | **values** |
| :--------------------------------------------------: | :--------: |
| The  relative magnetic permeability of steel strands |    400     |
|       The  conductivity of steel strands/(S/m)       |   5×106    |
|  The  relative magnetic permeability of AL strands   |     1      |
|        The  conductivity of AL strands /(S/m)        | 3.774×107  |
|     The  relative magnetic permeability of yoke      |    2000    |
|           The  conductivity of yoke /(S/m)           |    0.2     |
|           The  conductivity of coils/(S/m)           | 5.998×107  |
</div>
​		
&emsp;&emsp;Notches are placed in the ACSR conductors to simulate damage, as depicted in Figure 10. This paper categorizes the damage into three types: outer damage of AL strand, inner damage of AL strand, and damage of steel strand. The damage widths for each type are set from 2mm-6mm.
<div align=center>
<img src="FIG\FIG.5.jpg" width="500" />
</div>
<div align = "center">Fig.10. Distribution of damage in ACSR. (a) Variation of damage width(w) under different types, (b) Different fracture depths</div>

<div align=center>
<img src="FIG\dianliumidu.png" width="500" /><img src="FIG\FIG.6.gif" width="500" />
</div>
<div align = "center">Fig.11. Pulse stage current density model (unit: A/m²) & Magnetic field distribution in DC phase. (unit: mT)</div>

### Ⅲ.2. Magnetic flux densities at observation point

&emsp;&emsp;With the observation points described in the middle of the magnetic pin line, it is straightforward to compare the magnetic flux density variation for different damage types. As shown in Figure 12, the left portion represents the magnetic flux leakage in the Bx direction, while the right portion represents the magnetic flux leakage in the By direction.
<div align=center>
<img src="FIG\FIG.7.jpg" width="500" />
</div>
<div align = "center">Fig.12. Magnetic flux density of different damage positions</div>

&emsp;&emsp;As demonstrated in the figure 11, the damage types of the AL strand and the steel strand are highly distinguishable in both Bx and By directions. This distinctive signal can be captured by magnetically sensitive elements. For the damage detection of AL strand, the magnetic field changes occur during the pulsed phase. However, like the depths of damage, the variation is small, comparing to the normal. Due to the low relative magnetic permeability of AL strand, it couldn’t be detected in DC phase. On the other hand, because of the high magnetic permeability, the damage of steel stand means it could be detected during both the pulse phase and the DC phase. Therefore, the damage expression of steel strand is more pronounced in the DC phase.

### Ⅲ.2. Comparison of detection voltages

&emsp;&emsp;Figure 16 depicts the signals of various damage widths for different types and damage depths of steel/AL strands. The left section of the diagram presents all the signals detected by the balanced coil, while the right section displays the signals from the differential coils. Since the signal is symmetric about the y-axis in both positive and negative half-periods, the graph only shows up to 0.3s.
<div align=center>
<img src="FIG\dianyatu.png" height="450" />
</div>
<div align = "center">Fig.13. Detection voltages for different damage types</div>

&emsp;&emsp;Based on the analysis of the time-domain response voltage of damages, several viewpoints could be made. Specifically, the following summarizes the findings.

- During the pulsed response phase, the detection voltage for damage of AL strand exhibits a conspicuous overshoot impulse. The voltage response crosses the zero point and then returns. In contrast, when steel strand is damaged, the voltage signal doesn’t cross zero. Instead, it shows a gradual decline.
- Of the three impulse signals examined (i.e., steel strand damage signal, AL strand damage signal, and reference signal), the steel strand damage signal exhibits antiphase behavior with both the other signals.
- In terms of signal amplitude, the intensity of damage signal in the outer layer is higher than that in the inner layer, and the amplitude increases with the damage width. The buffer time for the balanced signal is significantly smaller than that for the differential signal. 

### Ⅲ.3. Quantification analysis

&emsp;&emsp;This subsection presents a further analysis of the simulation results. As previously mentioned, the detection voltage is symmetrical between the positive and negative half-periods and is processed within 0.3s. For the damage’s signals of AL strand, the balanced signal is the algebraic sum of the maximum value and the overshoot minimum value. In contrast, for the steel strand damage signal, the differential signal is the maximum of the algebraic value. The fitting results are presented in Figure 14.
<div align=center>
<img src="FIG\FIG.9.jpg" width="500"/>
</div>
<div align = "center">Fig.14. Fitting results</div>

&emsp;&emsp;The differential signal and the balanced signal show a linear pattern, suggesting that both damage depths and widths could be characterized numerically with a linear model. Moreover, the changing rate of voltage distinguishes both types of damage. Consequently, the changing rate of voltage amplitude is one of the effective distinguishing features.

&emsp;&emsp;It should be noted that the fitting results for AL strand show a negative intercept, which doesn’t indicate a reverse voltage change but rather the existence of a minimum detectable voltage. Based on the present simulation and geometric parameters, the minimum of the balanced coil required to detect outer damage of AL strand is estimated to be 0.64mm, while the minimum for inner damage of AL strand is 1.09mm. The minimum of the differential coils required to detect outer damage of AL strand is estimated to be 1.2mm, while the minimum for inner damage of AL strand is 1.48mm.

&emsp;&emsp;Besides, to enable comparison, the By direction of magnetic flux density in Figure 12 could be quantified using a linear Hall sensor, such as the WCS138 (±20mT, 8.3mV/Gs, 10Gs = 1mT). The fitting results for the Hall sensor output voltage are shown in Figure 15.
<div align=center>
<img src="FIG\FIG.10.jpg" width="250" />
</div>
<div align = "center">Fig.15. Transformed voltage from By</div>

&emsp;&emsp;In contrast, the minimum of the linear Hall sensor required to detect outer damage of AL strand is estimated to be 0.01mm, while the minimum for inner damage of AL strand is 0.99mm. When detecting strand damage, the width of the damage could be straightforwardly quantified based on the voltage and the magnetic flux density in the DC phase.

## Ⅳ. CONCLUSION

&emsp;&emsp;For the lack of effective methods for damages detection of ACSR conductors strand, this paper proposes a PEMEC method. Using COMSOL Multiphysics software to build and simulate a finite element model, the authors develop the damage characterizations from three dimensions: differential signal, balanced signal and magnetic flux density. On this basis, this paper explores the variation in detection characteristics at different locations, widths and depths of damage. An in-depth analysis of the results suggests the following conclusions.

1) The PEMEC method effectively detects damage to steel/AL strands through voltage peaks, that could quantify the width and depth of the damage. The coexistence of multiple damages requires further exploration.
2) Compared to direct EC method of single frequency or PEC method, the PEMEC method expands the detection range, enhances differentiation of steel and AL damage, and improves detection capabilities from three dimensions.
