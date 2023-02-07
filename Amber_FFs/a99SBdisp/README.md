## Installation

You should copy the [cmd](cmd), [lib](lib) and [parm](parm) files into the standard Amber directories. With one
exception, the [parm99.dat](parm/parm99.dat) file has not been changed (the same as for amber99sb).

```code-block:: bash
    # copy cmd files
    cp cmd/leaprc.protein.ff99SBdisp $AMBERHOME/dat/leap/cmd/.
    cp cmd/leaprc.water.tip4pd_disp $AMBERHOME/dat/leap/cmd/.
  
    # copy parm files 
    cp parm/frcmod.ff99SBdisp $AMBERHOME/dat/leap/parm/.
    cp parm/frcmod.tip4pd_disp $AMBERHOME/dat/leap/parm/.
     
    # copy lib files  
    cp lib/all_amino94disp.lib $AMBERHOME/dat/leap/lib/.
    cp lib/all_aminoct94disp.lib $AMBERHOME/dat/leap/lib/.
    cp lib/all_aminont94disp.lib $AMBERHOME/dat/leap/lib/.
    cp lib/tip4pdbox_disp.off $AMBERHOME/dat/leap/lib/.
```

## Usage

After the files will be copied, you can load the amber99sb-disp force field in tLeap programm as:

```code-block:: bash
   source leaprc.protein.ff99SBdisp
   source leaprc.water.tip4pd_disp
```
