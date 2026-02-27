# Lab Entry – 2026-02-26

## Metadata
- Date: 2026-02-26
- Project:Off Grid Solar Battery Charger
- Board / Rev:
- Scope: Design INA240A3 IC 100 (V/V) gain

## Objective
- Choose IC with appropriate gain.
- Select correct Rsense value. 
- Calculate Expected Error 
- Calculated expected power dissipation through Rsense


## Setup
- Use the [Data Sheet](https://www.ti.com/lit/ds/symlink/ina240.pdf?HQS=dis-dk-null-digikeymode-dsf-pf-null-wwe&ts=1772145455780&ref_url=https%253A%252F%252Fwww.ti.com%252Fgeneral%252Fdocs%252Fsuppproductinfo.tsp%253FdistId%253D10%2526gotoUrl%253Dhttps%253A%252F%252Fwww.ti.com%252Flit%252Fgpn%252Fina240) for the INA240 to meet objective. 
- Set Vs to be 3.3V
- Vref = GND
-  Imax is 1A 


## Calculations
$V_{DIFF} = \frac{V_{out}}{Gain} = \frac{3}{100} =.03 V $
$R_{sense} = \frac{V_{DIFF}}{I_{max}} = \frac{.03}{1} = 30 m\Omega $
$P_{RSENSE} = .03 * 1e2 = 30 mW $

Therefore, $I_{LSB} = \frac{1}{2^{12}} \approx .24 mA$


##### Expected error

$V_{OS\_CM} = \frac{1}{10^{85/20}} \times 2 \approx 135 \mu V$

$V_{OS\_ REF} = 5\mu V/V *|3.3/2|\approx 8.25 \mu V $

$ V_{OS\_Total} \approx 135 \mu V$

$ ERROR_{V\_os} \approx .45\% $

total error is approximatly .45% 


If we include the shunt resistor tolerance of 1%, then we can expect an error to be about 1.10% at best. 


## Conclusions / Next Steps
Implement theses parameters into the KIKAD model and look for a close value to the shunt reistor determined above 