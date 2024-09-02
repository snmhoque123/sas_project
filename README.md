

```sas
ods graphics on;
ods noproctitle;
proc freq data=pg1.storm_final order=freq nlevels;
	tables BasinName StartDate / nocum plots=freqplot(orient=horizontal scale=percent);
	format StartDate monname.;
run;
ods proctitle;

```
