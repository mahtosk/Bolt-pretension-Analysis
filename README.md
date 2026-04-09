# Bolt-pretension-Analysis deck
*NSET, NSET=pretension_Node
      9855,
*ELSET, ELSET = _PRETENS_SETSEGMENT_S1, GENERATE
6810,6830,1
*Surface, NAME = PRETENS_SETSEGMENT, TYPE = ELEMENT
_PRETENS_SETSEGMENT_S1,S1
** Pre-Tension Section for Bolt Load: pretensionload
**HMNAME GROUPS          1 pretension_group
*PRE-TENSION SECTION, NODE=pretension_Node, SURFACE=PRETENS_SETSEGMENT
**HMNAME LOADSTEP          1 pretension
*STEP, INC =       100000, NAME = pretension, NLGEOM = YES
a step for applying pretension
*STATIC
0.01      ,1.0       ,1.0000E-15,0.1       
**HWNAME LOADCOL          2 HM_Load_Cols_2
**HWCOLOR LOADCOL          2    43
*CLOAD
pretension_Node,1,30000.0        
*OUTPUT, FIELD, VARIABLE = PRESELECT
*OUTPUT, HISTORY, VARIABLE = PRESELECT
*RESTART, WRITE, FREQUENCY =     0
*END STEP
<img width="578" height="431" alt="image" src="https://github.com/user-attachments/assets/c24f8415-f75b-4b1b-8905-6d00f60b67b7" />
<img width="601" height="387" alt="image" src="https://github.com/user-attachments/assets/82ae5ecd-d6d1-49cb-ae3e-812b6d75e9fc" />
<img width="597" height="627" alt="image" src="https://github.com/user-attachments/assets/770aa476-386d-4d26-995a-dfcc4f05587d" />
<img width="547" height="382" alt="image" src="https://github.com/user-attachments/assets/3fdd4f00-fa75-4d6b-aac0-8667cedf171b" />
<img width="546" height="390" alt="image" src="https://github.com/user-attachments/assets/8e55eccc-d079-466f-8218-e55369071ebf" />
# it id dummy node, not belongs to any node of a model.
# In Abaqus CAE
<img width="480" height="502" alt="image" src="https://github.com/user-attachments/assets/f739a774-1e9e-4ca2-b95a-a8c075ca2954" />
<img width="1152" height="413" alt="image" src="https://github.com/user-attachments/assets/d6a5fac1-4cac-49df-93ab-5e0455de9503" />
#pretension section distance from bolt head should be 25% of shank length









