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
