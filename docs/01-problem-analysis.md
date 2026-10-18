# 1. Why Existing Cycle & Pregnancy Apps Fail

## The four fundamental problems

### 1. The 28-day calendar myth
Most apps calculate ovulation as `cycle length − 14`.  
This fails for irregular cycles, PCOS, stress, post-partum recovery, and perimenopause. The luteal phase is relatively stable (usually 11–16 days), but the follicular phase is highly variable.

### 2. Pathology blindness
Heavy bleeding, severe pain, cycles >35 days or very short luteal phases are often treated as "normal variation".  
They can be signals for endometriosis, adenomyosis, PCOS, thyroid disorders or luteal phase defect.

### 3. Fragmented life stages
Users are forced to switch between separate apps for cycle tracking, TTC, pregnancy and post-partum. Historical data is lost and the emotional experience is often insensitive (especially after miscarriage).

### 4. Privacy and data exploitation
Many free apps contain tracking SDKs and sell or share intimate health data (including pregnancy status).

## Design principles for this project
- Prefer real biomarkers (BBT, cervical mucus, LH) over pure calendar math
- Support variable luteal and follicular lengths
- Treat pathology as first-class (not an afterthought)
- Keep data local by default
- Allow seamless mode switching without data loss
- Be sensitive to pregnancy loss and fertility treatment
