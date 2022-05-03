# drb-temp-data-release-v2
A data release to support temperature modeling in the Delaware River Basin (2nd iteration)


## Running pipeline and pushoing the Science base from Caldera: 

* Log into tallgrass (`ssh username@tallgrass.cr.usgs.gov`)
* Navigate to `/caldera/projects/usgs/water/iidd/datasci/data_releases/drb-temp-data-release-v2`
* Run `git pull` to make sure latest changes from the remote repo are in the caldera repo
* Open R using srun 
  * If you are in the repo base dir (as above), then you can run:
  `srun -A pump -t 04:00:00 --pty -c 2 singularity exec ../data-releases-container_latest.sif R` (_note that the container we are using lives in data_releases_)

* You are now running R in tallgrass from the repo directory. 
* Built the pipeline in R: 
  * Load scipiper library (`library(scipiper)`) 
  * Run  `scmake()` on a specific or all targets. 
