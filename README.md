# Spiral Ganglion Cell Type-2 Model (Hossain et al., 2005)

**Author:** Srdjan Antic, University Connecticut Health Center, 22-DEC-2004

---

## Instructions for those who had no previous experience with NEURON!

To run the model described in *Hossain et al., 2005*:

1. Install NEURON from [http://www.neuron.yale.edu/neuron/](http://www.neuron.yale.edu/neuron/)
2. Make a new folder and copy all "*Hossain et al., 2005*" files to it.
3. Run **mknrndll** to compile "mod" files in that new folder.
4. Once the compiler is finished, go to the folder and double click "mosinit.hoc".
5. From the Neuron Main Menu use File → Load Session.
6. Pick any session from the list. The names of the sessions correspond with the figure panels in Hossain et al., 2005.
7. For instance take session "Fig7A".
8. Once the session is loaded you will see the following windows:

   a) Neuron Main Menu

   b) 4 Voltage-Axis graphs (Graph[1] to Graph[4])

   c) RunControl

   d) PointProcessManager

   e) Temperature

   f) Global Ra, *and*

   g) Cell Builder (CellBuild[0])

9. In the "RunControl" window click "Init & Run" button.
10. Graph[3] shows the membrane potential transients obtained in the receptor-neural segment (Receptor[5].v(0.5)) and in the cell body (soma). We are now at "the lower limit of the sensitive range". Both initial segments (ISP and ISC) are supplied with sodium channels, just enough to pass an action potential from the peripheral to the central axon via the cell body. To check the actual density of hh sodium channels, go to CellBuild[0] window → Biophysics → Init_Seg_Per.
11. In the Cell Builder change gNabar_hh from 929 to 928 in both, **Init_Seg_Per** (initial segment of the peripheral axon) and **Init_Seg_Cen** (initial segment of the central axon).
12. Run the simulation again (in "RunControl" window click "Init & Run" button).
13. Action potential (AP) now fails to invade the cell body. The only difference between this and previous trial is the removal of 1 pS/µm² from both initial segments.
14. To create the graph in Figure 7, panel C you need to find the "lower limits of the sensitive range" using four different channel mechanisms. Each bar in the histogram is represented by a session file starting with *Fig7C-*. If you load any of the session files starting with *Fig7C-* and then decrease the sodium conductance by only 1 pS/µm² from any initial segment, the AP would fail to invade the cell body. Note that the session "Fig7C-hh-black_bar.ses" is missing. This session file is identical to "Fig7A.ses", and therefore is omitted from the download.

the end

---

2025-05-27 – Standardized to Markdown.
