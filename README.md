# COVID19-CovSyn-Data-Taiwan-Country-AdjustedSecondaryAttackRate-9-2
Repository for synthetic data generated using CovSyn Taiwan with adjusted secondary attack rate, multiplied by 9, 100 simulations.

# contact_data/

## 📌 Description

This folder contains **contact-layer data for every infected individual**, per seed.  
Files are named: contact_data_<seed>.npy


Each file is a list where one entry = one infected case.  
Each entry is a dictionary containing:

### Household layer
- `household_contacts_matrix`
- `household_effective_contacts`
- `household_effective_contacts_infection_time`
- `household_secondary_contact_ages`
- `household_previously_infected_index_list`

### School layer
- (same fields as above)

### Workplace layer  
### Healthcare layer  
### Municipality layer  

Exact structure example:

```python
{
    'household_contacts_matrix': array([...]),
    'household_effective_contacts': [0,1,0,...],
    'household_effective_contacts_infection_time': [...],
    'household_secondary_contact_ages': [...],
    ...
}

### ✔ Example Loader
import numpy as np

data = np.load("contact_data_0.npy", allow_pickle=True)
case0 = data[0]



