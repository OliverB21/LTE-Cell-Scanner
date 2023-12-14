# f1866.5_s19.2_b20_0.08s_hackrf.bin 
Was captured during mass pull of signals, contains 1 cell and maybe SIBs? 
This one is more interesting. It shows that something has been found at IDX 16 and decimation 1, although it is not able to output it.
```
SF7 PHICH1 PDCCH1 RNTI: SI-RNTI SI-RNTI 
    PDCCH   No.0  4CCE: Localized VRB from RB51 to RB100 MCS-23 HARQ-0 NEWind-0 RV-2 TPC-1 DAI-
Index in position 2 exceeds array bounds. Index must not exceed 1200.

Error in pdsch_extract (line 44)
syms = tfg( (n_pdcch_symb+1) : end, (sc_sp+1):(sc_ep+1)).';

Error in decode_pdsch (line 7)
[syms, ce] = pdsch_extract(peak, reg_info, dci_info, subframe_idx, tfg, ce);

Error in LTE_DL_receiver (line 250)
                    [sib_info, ~] = decode_pdsch(cell_tmp, reg_info, dci_info, subframe_idx-1, tfg_comp, ce_tfg(:,:,:, subframe_idx), np_ce(subframe_idx,:));
```

# f2142.3_s19.2_bw20_0.08s_hackrf.bin
Targeted capture, contains 3 cells and SIBs (nRB 75, IDX 16, decimation 1)

# regression-test-signal-file
Provided from original git repo 

# f2119.9_s19.2_b20_0.08s_hackrf
Targeted capture, pulls a cell on nRB 50, contains SIB1 data (nRB 50, IDX 16, decimation 1)
