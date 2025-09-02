# Leaf Color Classification Algorithm
This algorithm uses raw RGB values from the APDS-9960 color sensor to classify the plant’s leaf condition


1. Collect Data
Place the sensor close to healthy, yellow, and dry leaves.
Record the R, G, B values in a table.


Condition	  R	    G	   B
Healthy    120	 200	100
Yellow	   200	 220	120
Dry	       150	 100	80


2. Normalize (Optional)
To reduce the effect of light brightness, normalize RGB by total intensity:
- Rnorm = R / (R+G+B)

- Gnorm = G / (R+G+B)

- Bnorm = B / (R+G+B)

3. Define Rules
Based on your measurements, set thresholds. Example:
If Gnorm > 0.4 → Leaf is Healthy 
Else if Rnorm > 0.45 and Gnorm > 0.35 → Leaf is Yellowing 
Else if Rnorm < 0.4 and Gnorm < 0.3 → Leaf is Dry


4. Arduino Example Code
   
   You can use "if, else if, else" to write your coding

# Harder version

