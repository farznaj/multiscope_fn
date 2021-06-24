# multiscope_fn
Codes used for the analysis of Allen Institute Multiscope data used in this paper: https://www.biorxiv.org/content/10.1101/2020.10.06.328294v2

The codes in this repository use the Visual Behavior dataset collected at the Allen Institute using Multiplane Mesoscopes.
Dataset:
https://portal.brain-map.org/explore/circuits/visual-behavior-2p


### Define directories:
define the following directories in def_paths.py:

`dirAna`: directory containing analysis files

`dir0`: directory for saving figures


### Files required to run the scripts (please contact me to send you the files):

**Mouse training history:**

/allen/programs/braintv/workgroups/nc-ophys/Farzaneh/mouse_trainHist_all2_20210216_151651.h5

**Neural responses file (a single file includes all sessions data):**

/allen/programs/braintv/workgroups/nc-ophys/Farzaneh/omit_traces_peaks/all_sess_omit_traces_peaks_np_corr_dff_20210309_152538.h5

**Neural correlations files (130 files; each belongs to a single session):**

this_sess_omit_traces_peaks_corr_m-440631_s-857040020_20210215_214246.pkl
this_sess_omit_traces_peaks_corr_m-485152_s-993738515_20210215_214530.pkl
this_sess_omit_traces_peaks_corr_m-479839_s-990139534_20210215_214050.pkl
this_sess_omit_traces_peaks_corr_m-484627_s-971632311_20210215_214547.pkl
this_sess_omit_traces_peaks_corr_m-449653_s-873247524_20210215_213943.pkl
this_sess_omit_traces_peaks_corr_m-453911_s-904418381_20210215_214335.pkl
this_sess_omit_traces_peaks_corr_m-435431_s-882674040_20210215_213939.pkl
this_sess_omit_traces_peaks_corr_m-453911_s-908441202_20210215_214254.pkl
this_sess_omit_traces_peaks_corr_m-453989_s-937682841_20210215_213932.pkl
this_sess_omit_traces_peaks_corr_m-448366_s-870762788_20210215_213941.pkl
this_sess_omit_traces_peaks_corr_m-485152_s-992393325_20210215_214410.pkl
this_sess_omit_traces_peaks_corr_m-523922_s-1051107431_20210215_213926.pkl
this_sess_omit_traces_peaks_corr_m-485152_s-993420347_20210215_214248.pkl
this_sess_omit_traces_peaks_corr_m-528097_s-1052330675_20210215_213925.pkl
this_sess_omit_traces_peaks_corr_m-453911_s-914161594_20210215_214357.pkl
this_sess_omit_traces_peaks_corr_m-449653_s-875259383_20210215_213946.pkl
this_sess_omit_traces_peaks_corr_m-448366_s-866197765_20210215_213943.pkl
this_sess_omit_traces_peaks_corr_m-438912_s-848401585_20210215_213938.pkl
this_sess_omit_traces_peaks_corr_m-440631_s-855711263_20210215_214247.pkl
this_sess_omit_traces_peaks_corr_m-457841_s-954954402_20210215_213932.pkl
this_sess_omit_traces_peaks_corr_m-457841_s-957020350_20210215_213934.pkl
this_sess_omit_traces_peaks_corr_m-482853_s-986130604_20210215_214247.pkl
this_sess_omit_traces_peaks_corr_m-484627_s-973701907_20210215_214752.pkl
this_sess_omit_traces_peaks_corr_m-449653_s-870352564_20210215_213947.pkl
this_sess_omit_traces_peaks_corr_m-453911_s-903621170_20210215_214345.pkl
this_sess_omit_traces_peaks_corr_m-523922_s-1051319542_20210215_213926.pkl
this_sess_omit_traces_peaks_corr_m-453988_s-939526443_20210215_213936.pkl
this_sess_omit_traces_peaks_corr_m-456915_s-904771513_20210215_214142.pkl
this_sess_omit_traces_peaks_corr_m-453990_s-923705570_20210215_214246.pkl
this_sess_omit_traces_peaks_corr_m-523922_s-1050231786_20210215_213935.pkl
this_sess_omit_traces_peaks_corr_m-479839_s-988768058_20210215_214118.pkl
this_sess_omit_traces_peaks_corr_m-457841_s-952430817_20210215_213928.pkl
this_sess_omit_traces_peaks_corr_m-453989_s-940145217_20210215_213936.pkl
this_sess_omit_traces_peaks_corr_m-456915_s-907991198_20210215_214042.pkl
this_sess_omit_traces_peaks_corr_m-438912_s-850894918_20210215_213939.pkl
this_sess_omit_traces_peaks_corr_m-453911_s-914639324_20210215_214355.pkl
this_sess_omit_traces_peaks_corr_m-435431_s-886130638_20210215_213949.pkl
this_sess_omit_traces_peaks_corr_m-453989_s-946015345_20210215_213931.pkl
this_sess_omit_traces_peaks_corr_m-451787_s-886367984_20210215_214601.pkl
this_sess_omit_traces_peaks_corr_m-453911_s-906299056_20210215_214254.pkl
this_sess_omit_traces_peaks_corr_m-482853_s-976167513_20210215_214242.pkl
this_sess_omit_traces_peaks_corr_m-485152_s-993253587_20210215_214402.pkl
this_sess_omit_traces_peaks_corr_m-453988_s-929686773_20210215_213940.pkl
this_sess_omit_traces_peaks_corr_m-449653_s-871526950_20210215_213948.pkl
this_sess_omit_traces_peaks_corr_m-523922_s-1048363441_20210215_213934.pkl
this_sess_omit_traces_peaks_corr_m-453991_s-947199653_20210215_214001.pkl
this_sess_omit_traces_peaks_corr_m-453911_s-906968227_20210215_214303.pkl
this_sess_omit_traces_peaks_corr_m-453991_s-948042811_20210215_213955.pkl
this_sess_omit_traces_peaks_corr_m-457841_s-955775716_20210215_213927.pkl
this_sess_omit_traces_peaks_corr_m-453990_s-927787876_20210215_214242.pkl
this_sess_omit_traces_peaks_corr_m-528097_s-1056238781_20210215_213931.pkl
this_sess_omit_traces_peaks_corr_m-453990_s-921922878_20210215_214245.pkl
this_sess_omit_traces_peaks_corr_m-440631_s-854060305_20210215_214248.pkl
this_sess_omit_traces_peaks_corr_m-435431_s-881094781_20210215_213952.pkl
this_sess_omit_traces_peaks_corr_m-482853_s-976382032_20210215_214243.pkl
this_sess_omit_traces_peaks_corr_m-482853_s-978201478_20210215_214242.pkl
this_sess_omit_traces_peaks_corr_m-453988_s-931326814_20210215_213924.pkl
this_sess_omit_traces_peaks_corr_m-453990_s-919041767_20210215_214238.pkl
this_sess_omit_traces_peaks_corr_m-453991_s-944888114_20210215_213959.pkl
this_sess_omit_traces_peaks_corr_m-435431_s-888009781_20210215_213940.pkl
this_sess_omit_traces_peaks_corr_m-438912_s-847758278_20210215_213935.pkl
this_sess_omit_traces_peaks_corr_m-484627_s-974486549_20210215_214339.pkl
this_sess_omit_traces_peaks_corr_m-451787_s-887031077_20210215_214422.pkl
this_sess_omit_traces_peaks_corr_m-528097_s-1052512524_20210215_213933.pkl
this_sess_omit_traces_peaks_corr_m-451787_s-888171877_20210215_214423.pkl
this_sess_omit_traces_peaks_corr_m-448366_s-874616920_20210215_213944.pkl
this_sess_omit_traces_peaks_corr_m-482853_s-977760370_20210215_214244.pkl
this_sess_omit_traces_peaks_corr_m-528097_s-1056065360_20210215_213929.pkl
this_sess_omit_traces_peaks_corr_m-453911_s-913564409_20210215_214406.pkl
this_sess_omit_traces_peaks_corr_m-482853_s-983913570_20210215_214242.pkl
this_sess_omit_traces_peaks_corr_m-453911_s-915306390_20210215_214552.pkl
this_sess_omit_traces_peaks_corr_m-453991_s-949217880_20210215_214002.pkl
this_sess_omit_traces_peaks_corr_m-435431_s-889944877_20210215_213943.pkl
this_sess_omit_traces_peaks_corr_m-451787_s-880709154_20210215_214146.pkl
this_sess_omit_traces_peaks_corr_m-453991_s-941676716_20210215_213954.pkl
this_sess_omit_traces_peaks_corr_m-438912_s-853177377_20210215_213940.pkl
this_sess_omit_traces_peaks_corr_m-485152_s-991958444_20210215_214438.pkl
this_sess_omit_traces_peaks_corr_m-453988_s-937162622_20210215_213943.pkl
this_sess_omit_traces_peaks_corr_m-438912_s-848983781_20210215_213943.pkl
this_sess_omit_traces_peaks_corr_m-453988_s-935559843_20210215_213941.pkl
this_sess_omit_traces_peaks_corr_m-440631_s-850667270_20210215_214246.pkl
this_sess_omit_traces_peaks_corr_m-453911_s-907753304_20210215_214310.pkl
this_sess_omit_traces_peaks_corr_m-453911_s-911719666_20210215_214350.pkl
this_sess_omit_traces_peaks_corr_m-482853_s-980062339_20210215_214253.pkl
this_sess_omit_traces_peaks_corr_m-440631_s-853416532_20210215_214249.pkl
this_sess_omit_traces_peaks_corr_m-457841_s-959458018_20210215_213928.pkl
this_sess_omit_traces_peaks_corr_m-479839_s-985609503_20210215_214147.pkl
this_sess_omit_traces_peaks_corr_m-456915_s-907177554_20210215_214124.pkl
this_sess_omit_traces_peaks_corr_m-453990_s-925478114_20210215_214241.pkl
this_sess_omit_traces_peaks_corr_m-485152_s-993962221_20210215_214506.pkl
this_sess_omit_traces_peaks_corr_m-457841_s-958772311_20210215_213934.pkl
this_sess_omit_traces_peaks_corr_m-451787_s-882386411_20210215_214354.pkl
this_sess_omit_traces_peaks_corr_m-435431_s-886806800_20210215_213942.pkl
this_sess_omit_traces_peaks_corr_m-523922_s-1049240847_20210215_213938.pkl
this_sess_omit_traces_peaks_corr_m-479839_s-991639544_20210215_214059.pkl
this_sess_omit_traces_peaks_corr_m-453990_s-916650386_20210215_214236.pkl
this_sess_omit_traces_peaks_corr_m-479839_s-990464099_20210215_214120.pkl
this_sess_omit_traces_peaks_corr_m-528097_s-1052096166_20210215_213928.pkl
this_sess_omit_traces_peaks_corr_m-479839_s-989267296_20210215_214153.pkl
this_sess_omit_traces_peaks_corr_m-440631_s-849304162_20210215_214253.pkl
this_sess_omit_traces_peaks_corr_m-435431_s-884451806_20210215_213940.pkl
this_sess_omit_traces_peaks_corr_m-435431_s-882060185_20210215_213953.pkl
this_sess_omit_traces_peaks_corr_m-453990_s-920695792_20210215_214248.pkl
this_sess_omit_traces_peaks_corr_m-484627_s-973384292_20210215_214500.pkl
this_sess_omit_traces_peaks_corr_m-453989_s-938898514_20210215_213937.pkl
this_sess_omit_traces_peaks_corr_m-456915_s-902884228_20210215_214342.pkl
this_sess_omit_traces_peaks_corr_m-453989_s-948252173_20210215_213937.pkl
this_sess_omit_traces_peaks_corr_m-453990_s-919888953_20210215_214251.pkl
this_sess_omit_traces_peaks_corr_m-438912_s-846871218_20210215_213944.pkl
this_sess_omit_traces_peaks_corr_m-451787_s-885557130_20210215_214251.pkl
this_sess_omit_traces_peaks_corr_m-448366_s-868688430_20210215_213942.pkl
this_sess_omit_traces_peaks_corr_m-484627_s-974167263_20210215_214528.pkl
this_sess_omit_traces_peaks_corr_m-484627_s-971922380_20210215_214548.pkl
this_sess_omit_traces_peaks_corr_m-453988_s-933439847_20210215_213940.pkl
this_sess_omit_traces_peaks_corr_m-482853_s-981845703_20210215_214252.pkl
this_sess_omit_traces_peaks_corr_m-451787_s-883619540_20210215_214135.pkl
this_sess_omit_traces_peaks_corr_m-453990_s-917498735_20210215_214245.pkl
this_sess_omit_traces_peaks_corr_m-453991_s-950031363_20210215_213955.pkl
this_sess_omit_traces_peaks_corr_m-440631_s-852794141_20210215_214255.pkl
this_sess_omit_traces_peaks_corr_m-453988_s-938140092_20210215_213942.pkl
this_sess_omit_traces_peaks_corr_m-457841_s-958105827_20210215_213928.pkl
this_sess_omit_traces_peaks_corr_m-482853_s-975452945_20210215_213950.pkl
this_sess_omit_traces_peaks_corr_m-449653_s-876303107_20210215_213951.pkl
this_sess_omit_traces_peaks_corr_m-435431_s-880498009_20210215_213937.pkl
this_sess_omit_traces_peaks_corr_m-453989_s-940775208_20210215_213939.pkl
this_sess_omit_traces_peaks_corr_m-456915_s-906521029_20210215_214308.pkl
this_sess_omit_traces_peaks_corr_m-451787_s-884613038_20210215_214245.pkl
this_sess_omit_traces_peaks_corr_m-449653_s-872592724_20210215_213944.pkl
this_sess_omit_traces_peaks_corr_m-456915_s-903813946_20210215_214356.pkl
this_sess_omit_traces_peaks_corr_m-448366_s-867027875_20210215_213941.pkl


### Make the population average figures

Run the following script after setting `doCorrs=0` at the beginning of the script:
omissions_traces_peaks_plots_setVars.py

Then run the script:
omissions_traces_peaks_plots_setVars_ave.py

Then run the script:
omissions_traces_peaks_plots_sumMice.py

  

### Make the correlation figures

Run the following script after setting `doCorrs=1` at the beginning of the script:
omissions_traces_peaks_plots_setVars.py

Then run the script:
omissions_traces_peaks_plots_setVars_corr.py

Then run the script:
omissions_traces_peaks_plots_setVars_corr_eachCre.py













